# AWS Simple Notification Service

Amazon Simple Notification Service (Amazon SNS) es un servicio administrado con el que se ofrece la entrega de mensajes de los publicadores a los suscriptores (también conocido como productores y consumidores). Los publicadores se comunican de forma asíncrona con los suscriptores mediante el envío mensajes a un tema, que es un punto de acceso lógico y un canal de comunicación. Los clientes pueden suscribirse al tema de SNS y recibir mensajes publicados mediante un tipo de punto de enlace compatible, como Amazon Kinesis Data Firehose, Amazon SQS, AWS Lambda, HTTP, correo electrónico, notificaciones push móviles y mensajes de texto móviles (SMS).

<p align="center">
  <img width="460" height="300" src="https://github.com/dimasx010/knowledge/assets/105082657/3fc37c2d-0b04-4015-b05f-181bc5483ae3">
</p>

## Características y funciones básicas

En Amazon SNS, se beneficia de las siguientes características y funciones básicas:

Mensajería de aplicación a aplicación

La mensajería de aplicación a aplicación admite suscriptores como flujos de entrega de Amazon Kinesis Data Firehose, funciones de Lambda, colas de Amazon SQS, puntos de enlace HTTP/S y canalizaciones de bifurcación de eventos de AWS. Para obtener más información, consulte Uso de Amazon SNS para la mensajería de aplicación a aplicación (A2A).

Notificaciones de aplicación a persona

Con las notificaciones de aplicación a persona, se ofrecen notificaciones de usuario a los suscriptores, como aplicaciones móviles, números de teléfono móvil y direcciones de correo electrónico. Para obtener más información, consulte Uso de Amazon SNS para mensajería de aplicación a persona (A2P).

Temas estándar y FIFO

Utilice un tema FIFO para garantizar un pedido estricto de mensajes, definir grupos de mensajes y evitar la duplicación de mensajes. Solo las colas FIFO de Amazon SQS pueden suscribirse a un tema FIFO. Para obtener más información, consulte Ordenación y desduplicación de mensajes (temas FIFO).

Utilice un tema estándar cuando el pedido de entrega de mensajes y la posible duplicación de mensajes no sean críticos. Todos los protocolos de entrega admitidos pueden suscribirse a un tema estándar.

Durabilidad de los mensajes

En Amazon SNS, se utiliza una serie de estrategias que funcionan en conjunto para proporcionar durabilidad a los mensajes:

Los mensajes publicados se almacenan en varios servidores y centros de datos separados por zona geográfica.

Si no se dispone de un punto de enlace suscrito, Amazon SNS ejecuta una política de reintentos de entrega.

Para conservar los mensajes que no se entreguen antes de que finalice la política de reintento de entrega, puede crear una cola de mensajes fallidos.

Análisis y archivado de mensajes

Puede suscribir flujos de entrega de Kinesis Data Firehose a temas de SNS, lo que le permite enviar notificaciones otros puntos de enlace de archivado y análisis, como buckets de Amazon Simple Storage Service (Amazon S3), tablas de Amazon Redshift y otros.

Atributos de mensajes

Con los atributos de mensaje, se puede proporcionar cualquier metadato arbitrario sobre el mensaje. Atributos de mensajes de Amazon SNS.

Filtrado de mensajes

De forma predeterminada, cada suscriptor recibe todos los mensajes publicados en el tema. Para recibir un subconjunto de los mensajes, un suscriptor debe asignar una política de filtro a la suscripción del tema. Un suscriptor también puede definir el alcance de la política de filtrado para habilitar el filtrado basado en cargas o en atributos. El valor predeterminado para el alcance de la política de filtrado es MessageAttributes. Cuando los atributos del mensaje entrante coinciden con los atributos de la política de filtro, el mensaje se entrega al punto de enlace suscrito. De lo contrario, el mensaje se filtra. Cuando el alcance de la política de filtrado es MessageBody, los atributos de la política de filtrado se comparan con la carga. Para obtener más información, consulte Filtrado de mensajes en Amazon SNS.

Seguridad de mensajes

Con el cifrado del lado del servidor, se protege el contenido de los mensajes almacenados en temas de Amazon SNS mediante claves de cifrado proporcionadas por AWS KMS. Para obtener más información, consulte Cifrado en reposo.

También puede establecer una conexión privada entre Amazon SNS y Virtual Private Cloud (VPC). Para obtener más información, consulte Privacidad del tráfico entre redes.

## Referencias
- https://docs.aws.amazon.com/es_es/sns/latest/dg/welcome.html
- https://docs.aws.amazon.com/es_es/sns/latest/dg/welcome-features.html
