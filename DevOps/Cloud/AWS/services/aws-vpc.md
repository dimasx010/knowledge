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

## Protección de las subredes con listas de control de acceso a la red

Piense en una lista de control de acceso a la red (ACL de red) como un firewall a nivel de subred. Una ACL de red le permite controlar qué tipo de tráfico puede entrar a la subred o salir de ella. Puede configurarlo al establecer reglas que definan lo que quiere filtrar. A continuación, se muestra un ejemplo.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/dc0cbed3-ad70-467c-9e27-72e32bd2d4c6">
</p>

La ACL de red predeterminada, que se muestra en la tabla anterior, permite que todo el tráfico entre a la subred y salga de ella. Para permitir que los datos fluyan libremente hacia la subred, este es un buen punto de partida.

Sin embargo, es posible que quiera restringir los datos a nivel de subred. Por ejemplo, si tiene una aplicación web, podría restringir la red para permitir tráfico HTTPS y tráfico de protocolo de escritorio remoto (RDP) a los servidores web.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/42907113-4d4e-4e00-a4f3-e6d8e4c87d43">
</p>
<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/4b27767e-34eb-431e-9d51-dad8411059d8">
</p>

Tenga en cuenta que en el ejemplo de ACL de red anterior, se permiten 443 entrantes y el intervalo de salida entre 1025 y 65535. Se debe a que HTTP utiliza el puerto 443 para iniciar una conexión y responderá a un puerto efímero. Las ACL de red se consideran sin estado, por lo que tiene que incluir los puertos de entrada y salida utilizados para el protocolo. Si no incluye el intervalo de salida, el servidor respondería, pero el tráfico nunca saldría de la subred.

Dado que las ACL de red están configuradas de forma predeterminada para permitir el tráfico entrante y saliente, no es necesario cambiar la configuración inicial a menos que necesite capas de seguridad adicionales.

## Protección de instancias EC2 con los grupos de seguridad

La siguiente capa de seguridad es para las instancias EC2. Aquí, puede crear un firewall denominado “grupo de seguridad”. La configuración predeterminada de un grupo de seguridad bloquea todo el tráfico entrante y permite todo el tráfico saliente.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/74e016c5-109e-4fdc-a538-8347877219ea">
</p>

Puede que se pregunte lo siguiente: “¿Esto no impediría que todas las instancias EC2 reciban la respuesta de las solicitudes de los clientes?” Los grupos de seguridad son grupos con estado. Significa que recordarán si una conexión se inicia originalmente por medio de la instancia EC2 o desde el exterior, y permitirán que el tráfico responda de forma temporal sin modificar las reglas de entrada.

Si desea que la instancia EC2 acepte el tráfico de Internet, debe abrir puertos de entrada. Si tiene un servidor web, es posible que deba aceptar solicitudes HTTP y HTTPS para permitir ese tipo de tráfico en su grupo de seguridad. Puede crear una regla de entrada que permita el puerto 80 (HTTP) y el puerto 443 (HTTPS) como se muestra.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/643e53ff-3051-4963-84ef-71bab839d70d">
</p>

En una unidad anterior, aprendió que las subredes se pueden utilizar para segregar el tráfico entre los ordenadores de la red. Los grupos de seguridad se pueden utilizar del mismo modo. Un patrón de diseño común consiste en organizar los recursos en diferentes grupos y crear grupos de seguridad para cada uno de ellos a fin de controlar la comunicación de red entre ellos.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/218f8c36-ab86-49cd-a640-c3393f9b8ffd">
</p>


## References
- https://docs.aws.amazon.com/en_en/vpc/latest/userguide/what-is-amazon-vpc.html
