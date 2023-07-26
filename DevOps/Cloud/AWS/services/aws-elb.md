# AWS Elastic Load Balancing

Elastic Load Balancing distribuye automáticamente el tráfico entrante entre varios destinos, por ejemplo, instancias EC2, contenedores y direcciones IP en una o varias zonas de disponibilidad. Monitorea el estado de los destinos registrados y enruta el tráfico solamente a destinos en buen estado. Elastic Load Balancing escala la capacidad del balanceador de carga de forma automática en respuesta a cambios en el tráfico entrante.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/aff38836-897f-4c8e-83ef-638564c95fc3">
</p>

## Características de ELB

El servicio ELB proporciona una gran ventaja sobre el uso de su propia solución para equilibrar la carga; principalmente, no tiene que administrarlo ni operarlo. Puede distribuir el tráfico de las aplicaciones entrantes en las instancias EC2, los contenedores, las direcciones IP y las funciones de AWS Lambda. Otras características clave incluyen las siguientes:

Dado que ELB puede equilibrar la carga en direcciones IP, puede funcionar en modo híbrido, lo que significa que también equilibra la carga de los servidores en las instalaciones.
ELB ofrece alta disponibilidad. La única opción que debe garantizar es que el equilibrador de carga se implemente en varias zonas de disponibilidad.
En términos de escalabilidad, ELB se escala automáticamente para satisfacer la demanda del tráfico entrante. Gestiona el tráfico entrante y lo envía a su aplicación de backend

## Tipos de ELB

### Equilibrador de carga de aplicaciones (ALB)

Estas son algunas de las características principales del Equilibrador de carga de aplicaciones.

ALB dirige el tráfico en función de los datos de las solicitudes. ALB toma decisiones de enrutamiento basadas en el protocolo HTTP, como la ruta URL (/upload) y el host, los encabezados y el método HTTP, y la dirección IP de origen del cliente. De este modo, se habilita el enrutamiento pormenorizado a los grupos de destino.

ALB envía respuestas directamente al cliente. ALB tiene la capacidad de responder directamente al cliente con una respuesta fija, como una página HTML personalizada. También puede enviar un redireccionamiento al cliente, lo que resulta útil cuando debe redirigir a un sitio web específico o redirigir una solicitud de HTTP a HTTPS, de modo que se elimina ese trabajo de los servidores de backend.

ALB utiliza la descarga TLS. Al hablar de HTTPS y evitar el trabajo de los servidores de backend, ALB entiende el tráfico HTTPS. Para que pase el tráfico HTTPS a través de ALB, se proporciona un certificado SSL al importar un certificado mediante los servicios de IAM o AWS Certificate Manager (ACM) o al crear uno de forma gratuita con ACM. Esto garantiza que el tráfico entre el cliente y ALB esté cifrado.

ALB autentica a los usuarios. Con respecto al tema de la seguridad, ALB puede autenticar a los usuarios antes de que se les permita atravesar el equilibrador de carga. ALB utiliza el protocolo OpenID Connect y se integra en otros servicios de AWS para admitir los protocolos, como SAML, LDAP, Microsoft Active Directory, etc.

ALB protege el tráfico. A fin de evitar que el tráfico llegue al equilibrador de carga, puede configurar un grupo de seguridad para especificar los intervalos de direcciones IP admitidos.

ALB utiliza el algoritmo de enrutamiento de turno rotativo. ALB garantiza que cada servidor reciba el mismo número de solicitudes en general. Este tipo de enrutamiento funciona para la mayoría de las aplicaciones.

ALB utiliza el algoritmo de enrutamiento de solicitudes menos pendiente. Si las solicitudes al backend varían en complejidad donde una solicitud puede necesitar mucho más tiempo de CPU que otra, el algoritmo de solicitud menos pendiente es más adecuado. También es el algoritmo de enrutamiento adecuado para utilizar si los destinos varían en las capacidades de procesamiento. Una solicitud pendiente se produce cuando se envía una solicitud al servidor de backend y aún no se ha recibido una respuesta.

Por ejemplo, si las instancias EC2 de un grupo de destino no tienen el mismo tamaño, la utilización de la CPU de un servidor será mayor que la otra si se envía el mismo número de solicitudes a cada servidor mediante el algoritmo de enrutamiento de turno rotativo. Ese mismo servidor también tendrá más solicitudes pendientes. El uso del algoritmo de enrutamiento de solicitudes menos pendiente garantizaría un uso equitativo en todos los destinos.

ALB utiliza sesiones rápidas. Si las solicitudes deben enviarse al mismo servidor de backend porque la aplicación funciona con estado, utilice la característica de sesión rápida. Esta característica utiliza una cookie HTTP para recordar en las conexiones a qué servidor enviar el tráfico.

Por último, ALB es específico para el tráfico HTTP y HTTPS. Si la aplicación utiliza un protocolo diferente, considere el equilibrador de carga de red.

### Equilibrador de carga de red (NLB)

Estas son algunas de las características principales del equilibrador de carga de red.

El equilibrador de carga de red admite los protocolos TCP, UDP y TLS. HTTPS utiliza TCP y TLS como protocolos. Sin embargo, NLB funciona en la capa de conexión, por lo que no entiende qué es una solicitud HTTPS. Significa que todas las características necesarias para comprender el protocolo HTTP y HTTPS, como las reglas de enrutamiento basadas en ese protocolo, la autenticación y el algoritmo de enrutamiento de la solicitud menos pendiente, no están disponibles con NLB.

NLB utiliza un algoritmo de enrutamiento hash de flujo. El algoritmo se basa en lo siguiente:

- Protocolo
- Dirección IP de origen y puerto de origen
- Dirección IP de destino y puerto de destino
- Número de secuencia TCP

Si todos los parámetros son iguales, los paquetes se envían exactamente al mismo destino. Si alguno de ellos es diferente en los siguientes paquetes, la solicitud podría enviarse a otro destino.

NLB ofrece sesiones rápidas. A diferencia de ALB, estas sesiones se basan en la dirección IP de origen del cliente, en lugar de en una cookie.

NLB admite la reasignación de TLS. NLB entiende el protocolo TLS. También puede reasignar TLS desde los servidores backend, de forma similar al funcionamiento de ALB.

NLB gestiona millones de solicitudes por segundo. Si bien ALB también puede admitir este número de solicitudes, tiene que escalarse para alcanzar ese número. Eso lleva tiempo. NLB puede gestionar instantáneamente millones de solicitudes por segundo.

NLB admite las direcciones IP estáticas y elásticas. En algunas situaciones, un cliente de aplicación tiene que enviar solicitudes directamente a la dirección IP del equilibrador de carga en lugar de utilizar DNS. Por ejemplo, esto resulta útil si la aplicación no puede utilizar DNS o si los clientes que se conectan requieren reglas de firewall basadas en direcciones IP. En este caso, NLB es el tipo correcto de equilibrador de carga que se debe utilizar.

El procesamiento de lenguaje natural conserva la dirección IP de origen. NLB conserva la dirección IP de origen del cliente al enviar el tráfico al backend. Con ALB, si observa la dirección IP de origen de las solicitudes, encontrará la dirección IP del equilibrador de carga. Mientras esté con NLB, vería la dirección IP real del cliente, requerida por la aplicación de backend en algunos casos.

### Selección entre los tipos de ELB

La selección entre los tipos de servicio ELB se realiza al definir qué característica es necesaria para la aplicación. En la tabla, se presenta una lista de las características principales de los equilibradores de carga.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/93f53569-20c8-4716-89c8-aa4b9618671f">
</p>

## References
- https://aws.amazon.com/es/elasticloadbalancing/
