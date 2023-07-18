# AWS Amazon Virtual Private Cloud VPC

With Amazon Virtual Private Cloud (Amazon VPC), you can launch AWS resources in a logically isolated virtual network that you have defined. This virtual network is very similar to the traditional network you would use in your own data center, but with the benefits of using the scalable AWS infrastructure.

An example VPC is shown in the diagram below. The VPC has a subnet in each availability zone of the region, EC2 instances in each subnet, and an Internet gateway to enable communication between the resources in your VPC and the Internet.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/58a81e7c-b326-4ef9-87b3-d251112db03b">
</p>

## Features
The following features help you configure a VPC to provide the connectivity your applications need:

### Virtual private clouds (VPC)
A VPC is a virtual network virtually identical to a traditional network that could operate in your own data center. Once you have created a VPC, you can add subnets.

### Subnetworks
A subnet is a range of IP addresses in your VPC. A subnet must reside in a single Availability Zone. After adding subnets, you can deploy AWS resources from your VPC.

### IP Addressing
You can assign IP addresses, IPv4 and IPv6, to VPCs and subnets. You can also incorporate your public IPv4 and IPv6 GUA addresses into AWS and assign them to your VPC resources, such as EC2 instances, NAT gateways, and network load balancers.

### Routing
Use the routing tables to determine where network traffic is routed from your subnet or gateway.

### Gateways and connection points
A gateway connects your VPC to another network. For example, use an Internet gateway to connect your VPC to the Internet. Use a VPC connection point to connect to AWS Services privately, without the use of an Internet gateway or NAT device.

### Pairing connections
Use a VPC peering connection to route traffic between the resources of two VPCs.

### Traffic replication
Copy network traffic from network interfaces and send it to security and monitoring devices for deep packet inspection.

### Transit gateways
Use a transit gateway, which acts as a central hub, to route traffic between your VPCs, VPN connections and AWS Direct Connect connections.

### VPC flow logs
Flow logs capture information about incoming and outgoing IP traffic to and from network interfaces in your VPC.

### VPN connections
Connect your VPCs to on-premises networks using AWS Virtual Private Network (AWS VPN).

## Creación de una subred

Después de crear la VPC, debe crear subredes en la red. Piense en las subredes como redes más pequeñas dentro de la red base o bien redes de área local virtual (VLAN) en una red en las instalaciones tradicional. En una red en las instalaciones, el caso de uso típico de las subredes es aislar u optimizar el tráfico de red. En AWS, las subredes se utilizan para proporcionar opciones de altas disponibilidad y conectividad para los recursos.

Al crear una subred, debe especificar lo siguiente:

La VPC en la que desea que se encuentre la subred; en este caso: VPC (10.0.0.0/16)
La zona de disponibilidad en la que quiere que se encuentre la subred; en este caso: AZ1
E bloque de CIDR para la subred, que debe ser un subconjunto del bloque de CIDR de la VPC; en este caso: 10.0.0.0/24
Cuando lanza una instancia EC2, la lanza en una subred, que se ubicará en la zona de disponibilidad que elija.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/59249558-b1fe-42f7-97e2-cb36a2bab6a2">
</p>

## Alta disponibilidad con una VPC

Cuando cree las subredes, tenga en cuenta la alta disponibilidad. Para mantener la redundancia y la tolerancia a errores, cree al menos dos subredes configuradas en dos zonas de disponibilidad.

Como se mencionó antes, recuerde que “todo falla en todo momento”. Con la red de ejemplo, si ocurre un error en una de las AZ, seguirá teniendo los recursos disponibles en otra AZ como copia de seguridad.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/bac4d887-9414-4465-abbb-f05aa3c573b1">
</p>

## IP reservadas

Para que AWS configure adecuadamente su VPC, AWS reserva cinco direcciones IP en cada subred. Estas direcciones IP se utilizan para el enrutamiento, el sistema de nombres de dominio (DNS) y la administración de redes.

Por ejemplo, considere una VPC con el intervalo de IP 10.0.0.0/22. La VPC incluye 1024 direcciones IP en total. Se divide en cuatro subredes de igual tamaño, cada una con un intervalo de IP de /24 con 256 direcciones IP. De cada uno de esos intervalos de IP, solo hay 251 direcciones IP que se pueden utilizar porque AWS reserva cinco.

Las cinco direcciones IP reservadas pueden afectar el diseño de la red. Un punto de partida común para aquellos que son nuevos en la nube es crear una VPC con un intervalo de IP de /16 y crear subredes con un intervalo de IP de /24. Esto proporciona una gran cantidad de direcciones IP con las que trabajar tanto a nivel de la VPC como de la subred.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/5f842fca-7c4d-479c-adea-09dda5d8e24d">
</p>

## References
- https://docs.aws.amazon.com/en_en/vpc/latest/userguide/what-is-amazon-vpc.html
