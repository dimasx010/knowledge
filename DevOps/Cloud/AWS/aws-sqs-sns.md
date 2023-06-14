# AWS Simple Queue Service SQS vs AWS Simple Notification Service

<p align="center">
  <img width="460" height="300" src="https://github.com/dimasx010/knowledge/assets/105082657/8a5adc1b-0f98-4476-bd75-6539c2800d28">
</p>

SNS es un sistema distribuido de publicación y suscripción . Los mensajes se envían a los suscriptores a medida que los editores los envían a SNS.

SQS es un sistema de colas distribuidas . Los mensajes no se envían a los receptores. Los receptores tienen que sondear o extraer mensajes de SQS . Los mensajes no pueden ser recibidos por varios destinatarios al mismo tiempo. Cualquier receptor puede recibir un mensaje, procesarlo y eliminarlo. Otros receptores no reciben el mismo mensaje más tarde. El sondeo introduce inherentemente cierta latencia en la entrega de mensajes en SQS, a diferencia de SNS, donde los mensajes se envían inmediatamente a los suscriptores. SNS admite varios puntos finales, como correo electrónico, SMS, punto final HTTP y SQS. Si desea que un número y tipo de suscriptores desconocidos reciban mensajes, necesita SNS.

No tiene que acoplar SNS y SQS siempre. Puede hacer que SNS envíe mensajes al punto final de correo electrónico, SMS o HTTP además de SQS. Hay ventajas al combinar SNS con SQS. Es posible que no desee que un servicio externo realice conexiones a sus hosts (un firewall puede bloquear todas las conexiones entrantes a su host desde el exterior).

Su punto final puede simplemente morir debido al gran volumen de mensajes. El correo electrónico y los SMS tal vez no sean su elección para procesar mensajes rápidamente. Al combinar SNS con SQS, puede recibir mensajes a su ritmo. Permite que los clientes estén fuera de línea, tolerantes a las fallas de la red y del host. También consigues una entrega garantizada. Si configura SNS para enviar mensajes a un punto final HTTP o correo electrónico o SMS, varias fallas en el envío de mensajes pueden provocar que los mensajes se eliminen.

SQS se utiliza principalmente para desacoplar aplicaciones o integrar aplicaciones. Los mensajes se pueden almacenar en SQS durante un breve período de tiempo (máximo 14 días). SNS distribuye varias copias de mensajes a varios suscriptores. Por ejemplo, supongamos que desea replicar datos generados por una aplicación en varios sistemas de almacenamiento. Puede usar SNS y enviar estos datos a varios suscriptores, cada uno de los cuales replica los mensajes que recibe en diferentes sistemas de almacenamiento ( S3 , disco duro en su host, base de datos, etc.).


## Referencias
- https://stackoverflow.com/questions/13681213/what-is-the-difference-between-amazon-sns-and-amazon-sqs

