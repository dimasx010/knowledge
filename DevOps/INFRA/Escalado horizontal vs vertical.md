# ESCAMIENTOS VERTICAL 

El escalado vertical tiene mucho que ver con el hardware del servidor de la aplicación. Se consigue de una manera muy sencilla: aumentando los recursos del servidor. Principalmente, en lo que respecta a la capacidad de procesamiento, memoria y almacenamiento. Este tipo de escalado es bastante sencillo de alcanzar, ya que únicamente requiere una intervención en el hardware del equipo, aumentando los recursos o incluso cambiando completamente de servidor. Sin embargo, el beneficio que se puede llegar a obtener también es limitado.

## Ventajas
- Facilidad de implementación y configuración.
- No requiere un diseño específico en la aplicación y su arquitectura para funcionar.
- Puede ser más económico.

## Desventajas
- Está limitado a la capacidad de un único servidor.
- No aporta beneficios en relación a la alta disponibilidad.

# ESCALADO HORIZONTAL

Por su parte, el escalado horizontal se consigue aumentando el número de servidores que atienden una aplicación. Para ello, un grupo de distintos servidores se configura para atender las peticiones de manera conjunta (es lo que se denomina cluster) y la carga de trabajo se distribuye entre ellos a través de un balanceador. Cada uno de esos servidores se conoce como nodo y el escalado se realiza simplemente agregando un nuevo nodo al clúster.

Este escalado es bastante más potente, pero sin embargo requiere una mayor configuración para poder realizarse, no solamente para crear la red de servidores de un cluster, sino también realizando una arquitectura de aplicación, a nivel de software, capaz de adaptarse a este tipo de funcionamiento.

## Ventajas
- El escalado es prácticamente infinito.
- Permite alta disponibilidad.
- Permite un correcto balance de carga entre los servidores.

## Desventajas
- Requiere mayor configuración, que puede llegar a ser difícil de realizar.
- Necesita que la aplicación esté construida de modo que soporte escalamiento vertical.
- Aunque más potente y de mejor rendimiento, suele ser una opción menos económica, ya que requiere de varios servidores.

