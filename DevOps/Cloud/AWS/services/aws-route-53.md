# AWS Route 53

Amazon Route 53 es un servicio web de sistema de nombres de dominio (DNS) escalable y de alta disponibilidad. Puede utilizar Route 53 para realizar tres funciones principales en cualquier combinación: registro de dominio, direccionamiento de DNS y comprobación de estado.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/94f125d7-2935-41e3-ab5d-4d62b21e25f6">
</p>

Si decide utilizar Route 53 para las tres funciones, asegúrese de seguir el orden que se indica a continuación:

### Registro de nombres de dominio
Su sitio web requiere un nombre, como example.com. Route 53 le permite registrar un nombre para su sitio web o aplicación web, conocido como nombre de dominio.

### Direccionamiento del tráfico de Internet a los recursos del dominio
Cuando un usuario abre un navegador web y escribe el nombre del dominio (example.com) o el nombre de un subdominio (acme.example.com) en la barra de direcciones, Route 53 ayuda a conectar el navegador con su sitio web o aplicación web.

### Comprobación del estado de los recursos
Route 53 envía solicitudes automatizadas a través de Internet a un recurso, como un servidor web, para verificar que está accesible, disponible y operativo. También puede elegir recibir notificaciones cuando un recurso deje de estar disponible y sacar el tráfico de Internet de los recursos que están en mal estado.

## References
- https://docs.aws.amazon.com/es_es/Route53/latest/DeveloperGuide/Welcome.html
