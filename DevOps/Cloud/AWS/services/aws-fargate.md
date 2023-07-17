# OpenShift - Service Mesh

La tecnología AWS Fargate se puede utilizar en Amazon ECS para ejecutar contenedores sin tener que administrar servidores, ni clústeres de instancias de Amazon EC2. Con Fargate, ya no tendrá que aprovisionar, configurar ni escalar clústeres de máquinas virtuales para ejecutar los contenedores. De esta manera, se elimina la necesidad de elegir tipos de servidores, decidir cuándo escalar los clústeres u optimizar conjuntos de clústeres.

Al ejecutar las tareas y los servicios de Amazon ECS con el tipo de lanzamiento de Fargate o un proveedor de capacidad de Fargate, la aplicación se empaqueta en contenedores, se especifican los requisitos de sistema operativo, CPU y de memoria, se definen las políticas de IAM y las redes, y se lanza la aplicación. Cada tarea de Fargate tiene su propio límite de aislamiento y no comparte el kernel subyacente, los recursos de CPU, los recursos de memoria ni la interfaz de red elástica con otra tarea.

Para obtener información acerca de la arquitectura de Fargate, consulte Uso del tipo de lanzamiento de Fargate en la Guía para desarrolladores de Amazon Elastic Container Service

En este tema, se describen los diferentes componentes de las tareas y los servicios de Fargate, y se mencionan consideraciones especiales para el uso de Fargate con Amazon ECS.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/b245c481-a508-45ee-88b6-77673cf87412">
</p>

## Componentes

### Clusteres

Un clúster de Amazon ECS es una agrupación lógica de tareas o servicios. Puede utilizar clústeres para aislar las aplicaciones. Cuando las tareas se ejecutan en Fargate, Fargate también administra los recursos del clúster.

### Definiciones de tareas

Una definición de tarea es un archivo de texto que describe uno o varios contenedores que forman la aplicación. Está en formato JSON. Puede utilizarse para describir hasta un máximo de diez contenedores. La definición de tareas funciona como un esquema para su aplicación. Especifica diversos parámetros para la aplicación. Por ejemplo, puede usarla para especificar parámetros para el sistema operativo, qué contenedores utilizar, qué puertos abrir para la aplicación, así como qué volúmenes de datos se van a utilizar con los contenedores en la tarea. Los parámetros específicos disponibles para la definición de tareas dependen de las necesidades de la aplicación específica.

No es necesario que toda la pila de la aplicación esté en una única definición de tareas. De hecho, le recomendamos que extienda su aplicación a varias definiciones de tareas. Para eso, puede combinar contenedores relacionados en sus propias definiciones de tareas, cada una de ellas representando un único componente.

### Tareas

Una tarea es la instancia creada de una definición de tarea dentro de un clúster. Después de crear una definición de tareas para la aplicación dentro de Amazon ECS, puede especificar el número de tareas que se ejecutarán en el clúster. Puede ejecutar una tarea independiente o ejecutar una tarea como parte de un servicio.

### Servicios

Puede utilizar un servicio de Amazon ECS para ejecutar y mantener simultáneamente el número deseado de tareas en un clúster de Amazon ECS. El funcionamiento es que, en caso de que alguna de las tareas falle o se pare por algún motivo, el programador de servicio de Amazon ECS lanza otra instancia en función de la definición de tarea. Lo hace para reemplazarlo y así mantener el número deseado de tareas en el servicio.

## Referencias
- https://aws.amazon.com/es/fargate/