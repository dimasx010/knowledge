# AWS Elastic Beanstalk

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/fa28a398-7f4b-4989-a5bf-b1fa111b415e">
</p>

Con Elastic Beanstalk, puede implementar y administrar aplicaciones rápidamente en la nube de AWS sin tener que preocuparse por la infraestructura que las ejecuta. Elastic Beanstalk reduce la complejidad de la administración sin restringir la libertad de elección ni el control. Solo tiene que cargar la aplicación y Elastic Beanstalk gestionará de manera automática los detalles de aprovisionamiento de capacidad, balanceo de carga, escalado y monitorización de estado de la aplicación.

Elastic Beanstalk es compatible con aplicaciones desarrolladas en Go, Java, .NET, Node.js, PHP, Python y Ruby. Cuando implementa su aplicación, Elastic Beanstalk crea la versión de la plataforma compatible seleccionada y aprovisiona uno o varios recursos de AWS, como instancias de Amazon EC2, para ejecutar la aplicación.

Puede interactuar con Elastic Beanstalk a través de la consola de Elastic Beanstalk, la AWS Command Line Interface (AWS CLI) o eb, una CLI de nivel superior diseñada específicamente para Elastic Beanstalk.

Para obtener más información sobre cómo implementar una aplicación web de ejemplo con Elastic Beanstalk, consulte Introducción a AWS: Implementación de una aplicación web.

También puede realizar la mayoría de las tareas de implementación, como cambiar el tamaño de la flota de instancias de Amazon EC2 o monitorizar la aplicación, directamente desde la interfaz web de Elastic Beanstalk (consola).

Para utilizar Elastic Beanstalk, debe crear una aplicación, cargar una versión de la aplicación como un paquete de código fuente (por ejemplo, un archivo Java.war) en Elastic Beanstalk y proporcionar cierta información sobre la aplicación. Elastic Beanstalk lanza automáticamente un entorno y crea y configura los recursos de AWS necesarios para ejecutar el código. Una vez que se lanza el entorno, puede administrarlo e implementar nuevas versiones de la aplicación. En el siguiente diagrama, se ilustra el flujo de trabajo de Elastic Beanstalk.

Después de crear e implementar la aplicación, puede consultar información sobre ella (por ejemplo, métricas, eventos y el estado del entorno) en la consola de Elastic Beanstalk, las API o las interfaces de línea de comandos, como la AWS CLI unificada.

## Referencias
- https://docs.aws.amazon.com/es_es/elasticbeanstalk/latest/dg/Welcome.html


