# Regiones y Zonas de Disponibilidad en AWS

Estas ubicaciones se componen de las llamadas zonas locales, así como de las regiones y zonas de disponibilidad de AWS. De manera que, aunque estos términos suelen trabajarse de manera conjunta, cada uno puede definirse de manera individual de la siguiente forma:

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/c32efc96-f935-4e63-ab99-9ceaf3e24e8c">
</p>

## Regiones de AWS

Las regiones de AWS hacen referencia a áreas geográficas independientes o ubicaciones físicas donde Amazon Web Service agrupa sus centros de datos. Es aquí donde el usuario puede levantar sus servicios.

De modo que cada grupo de estos centros de datos lógicos se conocen como zona de disponibilidad y una misma región de infraestructura de AWS incluye dos o más de estas zonas para proporcionar sus servicios.

Las regiones de AWS hacen referencia a áreas geográficas independientes o ubicaciones físicas donde Amazon Web Service agrupa sus centros de datos. Es aquí donde el usuario puede levantar sus servicios.

De modo que cada grupo de estos centros de datos lógicos se conocen como zona de disponibilidad y una misma región de infraestructura de AWS incluye dos o más de estas zonas para proporcionar sus servicios.

## Zonas de disponibilidad de AWS

Las zonas de disponibilidad de Amazon Web Service AWS se refiere a uno o más data center independientes con su propia seguridad física, refrigeración y conexión mediante redes redundantes con niveles muy bajos de latencia y de alto ancho de banda.

Como ya hemos mencionado, la relación entre las regiones y zonas de disponibilidad de AWS es que es necesario que en una misma región estén dos o más zonas para que pueda funcionar.

Cabe aclarar que estas zonas de disponibilidad de Amazon Web Service se encuentran lo suficientemente aisladas físicamente unas de otras para que, en los casos donde ocurran fallos eléctricos o de funcionamiento en alguna de las zonas, la otra no se vea afectada.

Este aislamiento permite que los usuario puedan construir sus aplicaciones y llevar a cabo sus despliegues de forma que se pueda garantizar que sean altamente disponibles, siempre y cuando se distribuyan las cargas de trabajo en diferentes zonas de disponibilidad.

Además, estas zonas permiten que los usuarios operen bases de datos y múltiples aplicaciones de producción con un nivel alto de tolerancia a errores y escalabilidad y, al tratarse de dos zonas por región o más, se garantiza que estas ventajas sean mayores que las pudiera ofrecer un solo centro de datos.

## Referencias
- https://keepcoding.io/blog/regiones-y-zonas-de-disponibilidad-de-aws/
- https://aws.amazon.com/es/about-aws/global-infrastructure/?p=ngi&loc=1

