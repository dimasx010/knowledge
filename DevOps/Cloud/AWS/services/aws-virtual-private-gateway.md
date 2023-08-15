# AWS Virtual Private Gateway

Para acceder a los recursos privados de una VPC, puedes utilizar una puerta de enlace privada virtual. 

A continuación se muestra un ejemplo de cómo funciona una puerta de enlace privada virtual. Puedes imaginarte que Internet es como el camino entre tu casa y la cafetería. Supongamos que viajas por esta carretera con un guardaespaldas que te protege. Sigues utilizando la misma carretera que otros clientes, pero con una capa adicional de protección. 

El guardaespaldas es como una conexión de red privada virtual (VPN) que cifra (o protege) tu tráfico de Internet de todas las demás peticiones que lo rodean. 

La puerta de enlace privada virtual es el componente que permite que el tráfico de Internet protegido entre en la VPC. Aunque tu conexión a la cafetería tiene protección adicional, es posible que se produzcan atascos porque estás utilizando la misma carretera que otros clientes.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/89bbcf2e-4faf-4bcc-92a8-0bcf3c06d5f5">
</p>

Una puerta de enlace privada virtual permite establecer una conexión de red privada virtual (VPN) entre la VPC y una red privada, como un centro de datos en las instalaciones o una red corporativa interna. Una puerta de enlace privada virtual permite el tráfico en la VPC solo si procede de una red aprobada.
