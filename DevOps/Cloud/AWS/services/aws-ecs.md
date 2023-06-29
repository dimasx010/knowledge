#  Amazon Elastic Container Service ECS

Amazon ECS es un servicio de orquestación de contenedores integral que ayuda a activar nuevos contenedores y administrarlos en un clúster de instancias EC2.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/dcf88406-bccb-4f30-bed4-93482a931f80">
</p>

Para ejecutar y administrar los contenedores, tiene que instalar el agente de contenedores de Amazon ECS en las instancias EC2. Este agente es de código abierto y es responsable de comunicar al servicio ECS de Amazon los detalles de administración de clústeres. Puede ejecutar el agente en AMI de Linux y Windows. Una instancia con el agente de contenedores instalado a menudo se denomina “instancia de contenedor”


<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/ca997b5b-4cb3-41cb-adfe-00d641a8cd39">
</p>

​Una vez que las instancias de contenedor de Amazon ECS estén en funcionamiento, puede realizar acciones que incluyen, entre otras, lanzar y detener contenedores, obtener el estado del clúster, reducir y escalar horizontalmente, programar la ubicación de contenedores en el clúster, asignar permisos y cumplir los requisitos de disponibilidad.

Para preparar la aplicación a fin de que se ejecute en Amazon ECS, crea una definición de tarea. La definición de tarea es un archivo de texto en formato JSON que describe uno o más contenedores. Una definición de tarea es similar a un proyecto donde se describen los recursos necesarios para ejecutar un contenedor, como la información sobre las redes, la CPU, la memoria, los puertos, las imágenes y el almacenamiento.

