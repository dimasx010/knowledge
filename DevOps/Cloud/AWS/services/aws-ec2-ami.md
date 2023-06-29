# Amazon Machine Image AMI - Amazon EC2

En el mundo de la infraestructura tradicional, el proceso de poner en marcha un servidor consiste en instalar un sistema operativo a partir de discos, unidades o asistentes de instalación a través de la red. En la nube de AWS, la instalación del sistema operativo no es responsabilidad suya. En cambio, está integrado en la AMI que elija.

Además, cuando utiliza una AMI, puede seleccionar mapeos de almacenamiento, el tipo de arquitectura (como 32 bits, 64 bits o ARM de 64 bits) y software adicional instalado.


<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/635c8f1a-477b-4299-816c-69439feae6a5">
</p>

## Relación entre las AMI y las instancias EC2

Las instancias EC2 son instancias en directo de lo que se define en una AMI, al igual que un pastel es una instancia en directo de una receta de pastel. Si está familiarizado con el desarrollo de software, también puede ver este tipo de relación entre una clase y un objeto.

Una clase es algo que modela y define, mientras que un objeto es algo con lo que interactúa. En este caso, la AMI es la forma en que modela y define la instancia, mientras que la instancia EC2 es la entidad con la que interactúa, donde puede instalar el servidor web y entregar el contenido a los usuarios.

Cuando lanza una nueva instancia, AWS asigna una máquina virtual que se ejecuta en un hipervisor. A continuación, la AMI que seleccionó se copia en el volumen de dispositivo raíz, que contiene la imagen utilizada para arrancar el volumen. Al final, obtiene un servidor al que puede conectarse y donde puede instalar paquetes y software adicional. En el ejemplo, instala un servidor web junto con el código fuente configurado correctamente de la aplicación de directorio de empleados.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/6c64359a-a1fa-49b8-8aaa-b293a654354e">
</p>

Una ventaja de utilizar las AMI es que son reutilizables. Puede elegir una AMI basada en Linux y configurar el servidor HTTP, los paquetes de aplicaciones y el software adicional que necesita para ejecutar la aplicación. Si quiere crear una segunda instancia EC2 con las mismas configuraciones, podría atravesar todo el proceso de creación y configuración de instancias para que la configuración coincida con la primera instancia. Alternativamente, podría crear una AMI a partir de la instancia en ejecución y utilizar la AMI para iniciar una nueva instancia. De esta forma, la nueva instancia tendría las mismas configuraciones que la instancia actual porque las configuraciones establecidas en las AMI son las mismas.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/c17a6e14-6717-4eaf-b401-c645182e433f">
</p>

