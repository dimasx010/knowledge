# AWS Simple Queue Service SQS 

Amazon Simple Queue Service, también conocido como Amazon SQS, es uno de los servicios ofrecidos por la infraestructura de AWS y se enfoca en el manejo de las colas de mensajes.

La herramienta de Amazon SQS destaca como el servicio más antiguo de Amazon Web Service y se caracteriza por estar completamente gestionado por el sistema.

Además, este servicio permite el ajuste y desacople de la escala de los sistemas distribuidos, aplicaciones sin servidor y los microservicios.

<p align="center">
  <img width="460" height="300" src="https://github.com/dimasx010/knowledge/assets/105082657/9733a979-75a7-447a-96cf-eadf094e5d6c">
</p>

​Otras de las características importantes de Amazon SQS son:

## ​Completamente gestionado

Una de las principales características de Amazon Simple Queue Service es que se encuentra totalmente administrada por la infraestructura de nube de AWS, lo que implica que evita la dificultad y los costes generales relacionados con la gestión y el funcionamiento del middelware orientado a mensajes. Esto contribuye a que los desarrolladores que utilicen sus servicios puedan enfocarse en sus actividades y la diferenciación de las labores.

### ​API de Amazon SQS

​Una de las características de Amazon SQS es que incluye la opción de una Interfaz de Programación de Aplicaciones API de servicios web de tipo genérica, permitiendo su acceso a través de cualquiera de los lenguajes de programación admitidos por AWS SDK.

### ​Durabilidad

​El sistema de Amazon SQS almacena los mensajes en múltiples servidores para garantizar su durabilidad y seguridad.

### ​Fiabilidad

​Amazon Simple Queue Service se encarga también de bloquear los mensajes durante el procesamiento con el objetivo de que diferentes productores tengan la posibilidad de realizar el envío de mensajes, al tiempo que varios consumidores puedan recibirlos.

### ​Otras características

​Otras de las propiedades relevantes del servicio de Amazon Simple Queue Service son:

- ​Escala desde 1 mensaje por segundo a 10.000 por segundo.
- ​Retención por defecto: 4 días, máximo de 14 días.
- ​No hay límites acerca de la cantidad de mensajes que pueden existir.
- ​Baja latencia (10ms para publicar y recibir).
- ​Permite escalar horizontalmente con el número de consumidores.
- ​Puede tener mensajes duplicados.
- ​Puede incluir mensajes en desorden.
- Establece un límite de 256 KB por mensaje enviado.


## Referencias
- https://docs.aws.amazon.com/es_es/sns/latest/dg/welcome.html
- https://docs.aws.amazon.com/es_es/sns/latest/dg/welcome-features.html
