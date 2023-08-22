# AWS NAT Gateway

Un NAT Gateway, también conocida como Network Adress Translation o Servicio de Traducción de Direcciones de Red, se refiere a una herramienta de la VPC de Amazon que se utiliza para que las instancias de una determinada subred privada puedan establecer conexión con servicios externos a la nube privada virtual, pero que estos mismos servicios no inicien conexión con las instancias.

Cabe destacar que, además, cada uno de los NAT Gateway se crea en una determinada zona de disponibilidad y se implementa con redundancia para que pueda cumplir con sus labores de una mejor manera.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/3f715a76-75d0-4dd2-9a3d-88eb9388d0b8">
</p>

La herramienta de NAT Gateway en AWS VPC cuenta con una serie de propiedades y características que permiten su funcionamiento, dentro de las que se incluye que puede crearse y gestionarse mediante la consola de la VPC de Amazon.

Además de esto, NAT Gateway se caracteriza por permitir conectividades tanto de tipo públicas como privadas. De manera que se encarga de reemplazar la IP de fuente de las instancias con la dirección IP de la NAT Gateway, lo que implica que, para las que sean de tipo pública, será la dirección IP elástica; mientras que, para las privadas, corresponderá a la dirección IP privada de la NAT Gateway.

En lo que respecta a la creación de esta herramienta, se deben tener en cuenta los requisitos de un nombre opcional, una subred o subnet y un tipo de conectividad opcional (pública o privada).

También es posible eliminar una NAT Gateway, a través de la consola de Amazon VPC. Esta eliminación implicará que su entrada seguirá siendo visible en la consola por un periodo estimado de una hora, hasta que se termina de eliminar de manera automática.

Otra de las características de la herramienta de NAT Gateway en la VPC de Amazon son:

- Habilita la conexión saliente a internet.
- No permite la conexión entrante de servidores externos.
- Es de gran utilidad para sistemas operativos o paquetes que tengan acceso a servicios web de tipo público.
- Es una herramienta completamente gestionada y administrada por la plataforma de Amazon Web Service (AWS).
- Se caracteriza por su alta disponibilidad, por lo que tiene la capacidad de garantizar la continuidad de sus labores, incluso en situaciones donde se presenten inconvenientes en el sistema.
- Soporta protocolos como el Transmission Control Protocol (TCP), User Datagram Protocol (UDP) y el protocolo Internet Control Message Protocol (ICMP).
- Hasta 5Gbps de ancho de banda que pueden ampliarse de manera automática hasta 45Gbps.
- No es posible dirigir el tráfico a una NAT Gateway usando interconexiones de VPC, conexiones site-to-site VPN, ni a través de la herramienta de AWS Direct Connect.
- Cada una de estas herramientas se crea en una zona de disponibilidad con redundancia. Cabe destacar que el sistema establece una cuota del número de NAT Gateway que se pueden crear en cada zona.
- No es posible asociar una NAT Gateway a un determinado grupo de seguridad; pero sí se pueden asociar estos grupos a las instancias con el objetivo de controlar su tráfico.
- Por defecto, los usuarios de IAM no tienen privilegios que les habilite trabajar con las NAT Gateways.

## References
- https://keepcoding.io/blog/que-es-nat-gateway-en-amazon-vpc/
