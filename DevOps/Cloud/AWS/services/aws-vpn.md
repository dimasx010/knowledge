# AWS VPN

Las soluciones de red privada virtual de AWS establecen conexiones seguras entre sus redes en las instalaciones, las oficinas remotas, los dispositivos cliente y la red global de AWS. AWS VPN se compone de dos servicios: AWS Site-to-Site VPN y AWS Client VPN. Juntos, ofrecen una solución de VPN en la nube de alta disponibilidad, administrada y elástica para proteger su tráfico de red.

AWS Site-to-Site VPN crea túneles cifrados entre su red y sus instancias de Amazon Virtual Private Cloud o AWS Transit Gateway. Para administrar el acceso remoto, AWS Client VPN conecta sus usuarios a recursos de AWS o en las instalaciones mediante un cliente de software de VPN.

AWS Client VPN es un servicio de VPN completamente administrado y elástico que aumenta o disminuye automáticamente en función de sus requisitos. Debido a que es una solución de VPN en la nube, no necesita instalar y administrar soluciones basadas en hardware o software, ni intentar estimar cuántos usuarios remotos puede admitir a la vez.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/7413dc58-3b60-4015-803d-9697d69b62aa">
</p>

## Beneficios

### Completamente administrado
AWS Client VPN se encarga automáticamente de la implementación, el aprovisionamiento de capacidad y las actualizaciones del servicio, mientras usted monitorea todas las conexiones desde una única consola.

### Autenticación avanzada
Muchas organizaciones requieren Multi-Factor Authentication (MFA) y autenticación federada para su solución de VPN.

### Elasticidad
Los servicios de VPN tradicionales en las instalaciones están limitados por la capacidad del hardware que los ejecuta. AWS Client VPN es un servicio de VPN en la nube de pago por uso que aumenta o disminuye elásticamente en función de la demanda de usuarios. 

### Acceso remoto
A diferencia de los servicios de VPN en las instalaciones, AWS Client VPN permite a los usuarios conectarse a AWS y redes en las instalaciones mediante una única conexión de VPN.

## Casos de uso

### Escale rápidamente el acceso remoto
Circunstancias inesperadas pueden requerir que muchos de sus empleados deban trabajar de forma remota. Esto crea un aumento en las conexiones y el tráfico de VPN que puede reducir el rendimiento o la disponibilidad para sus usuarios. AWS Client VPN es elástico y aumenta automáticamente para gestionar los picos de demanda. Cuando ha pasado el pico, disminuye para que no pague por capacidad que no usa.

### Implemente y elimine fácilmente el acceso a VPN para trabajadores temporales
Con AWS Client VPN, puede otorgar fácilmente acceso a nuevos usuarios a redes específicas de AWS y de las instalaciones. Para otorgar acceso, agréguelos a un grupo de Active Directory y configure las normas de acceso de ese grupo. Eliminar el acceso cuando su contrato finalice es igual de sencillo.

### Acceda fácilmente a sus aplicaciones en la nube o en las instalaciones
AWS Client VPN brinda a los usuarios acceso seguro a las aplicaciones, tanto en las instalaciones, como en AWS. Esto es especialmente útil durante una migración de la nube, cuando las aplicaciones se trasladan de ubicaciones en las instalaciones a la nube. Con AWS Client VPN, los usuarios no necesitan cambiar la forma en la que acceden a sus aplicaciones durante o después de la migración.

## References
- https://aws.amazon.com/es/vpn/
