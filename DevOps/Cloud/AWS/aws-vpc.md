# AWS Amazon Virtual Private Cloud VPC

Con Amazon Virtual Private Cloud (Amazon VPC), puede lanzar recursos de AWS en una red virtual aislada de manera lógica que haya definido. Esta red virtual es muy similar a la red tradicional que usaría en su propio centro de datos, pero con los beneficios que supone utilizar la infraestructura escalable de AWS.

En el siguiente diagrama se muestra una VPC de ejemplo. La VPC tiene una subred en cada zona de disponibilidad de la región, instancias de EC2 en cada subred y una puerta de enlace de Internet para permitir la comunicación entre los recursos en su VPC y la Internet.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/58a81e7c-b326-4ef9-87b3-d251112db03b">
</p>

## Características
Las siguientes funciones lo ayudan a configurar una VPC para proporcionar la conectividad que necesitan sus aplicaciones:

### Nubes virtuales privadas (VPC)
Una VPC es una red virtual prácticamente idéntica a una red tradicional que podría operar en su propio centro de datos. Una vez creada una VPC, podrá agregar las subredes.

### Subredes
Una subred es un rango de direcciones IP en su VPC. Una subred debe residir en una sola zona de disponibilidad. Después de agregar subredes, puede implementar recursos de AWS de su VPC.

### Direccionamiento IP
Puede asignar direcciones IP, IPv4 y IPv6, a las VPC y las subredes. También puede incorporar sus direcciones GUA IPv4 e IPv6 públicas a AWS y asígnelos a los recursos de su VPC, como las instancias de EC2, las puertas de enlace NAT y los equilibradores de carga de red.

### Enrutamiento
Use las tablas de enrutamiento para determinar dónde se dirige el tráfico de red de su subred o puerta de enlace.

### Puertas de enlace y puntos de conexión
Una puerta de enlace conecta su VPC a otra red. Por ejemplo, use una puerta de enlace de Internet para conectar la VPC a Internet. Use un punto de conexión de VPC para conectarse a Servicios de AWS de forma privada, sin el uso de una puerta de enlace de Internet o un dispositivo NAT.

### Conexiones de emparejamiento
Use una conexión de emparejamiento de VPC para enrutar el tráfico entre los recursos de dos VPC.

### Replicación de tráfico
Copie el tráfico de red desde las interfaces de red y envíelo a dispositivos de seguridad y monitoreo para una inspección profunda de paquetes.

### Puertas de enlace de tránsito
Use una puerta de enlace de tránsito, que actúa como un concentrador central, para enrutar el tráfico entre sus VPC, las conexiones de VPN y las conexiones de AWS Direct Connect.

### Logs de flujo de VPC
Los registros de flujo capturan información acerca del tráfico IP entrante y saliente de las interfaces de red en su VPC.

### Conexiones de VPN
Conecte sus VPC a las redes en las instalaciones mediante AWS Virtual Private Network (AWS VPN).

## Referencias
- https://docs.aws.amazon.com/es_es/vpc/latest/userguide/what-is-amazon-vpc.html
