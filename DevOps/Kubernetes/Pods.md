# Pods

## General
Los pods son los objetos más pequeños y básicos que se pueden implementar en Kubernetes. Un pod representa una instancia única de un proceso en ejecución en tu clúster.

Los pods contienen uno o más contenedores, como los contenedores de Docker. Cuando un pod ejecuta varios contenedores, estos se administran como una sola entidad y comparten los recursos del pod.

Los pods también poseen recursos compartidos de red y almacenamiento para sus contenedores:

### Red

A los pods se les asignan direcciones IP únicas de manera automática. Los contenedores de pod comparten el mismo espacio de nombres de red, incluida la dirección IP y los puertos de red. Los contenedores de un pod se comunican entre sí dentro del pod en localhost.

### Almacenamiento

Los pods pueden especificar un conjunto de volúmenes de almacenamiento compartido que se puede compartir entre los contenedores.

Puedes pensar que un pod es un “host lógico” autónomo y aislado que posee las necesidades sistémicas de la aplicación para la que funciona.

El objetivo de un pod es ejecutar una única instancia de tu aplicación en tu clúster. Sin embargo, no se recomienda crear pods individuales de forma directa.

## Ciclo de vida del Pod

Los pods son efímeros. No están diseñados con el fin de funcionar para siempre y cuando un pod se termina, no se puede recuperar. En general, los pods no desaparecen hasta que un usuario o un controlador los borra.

Los pods no se “curan” ni se reparan por sí mismos. Por ejemplo, si un pod se programa en un nodo que luego falla, el pod se borra. De forma similar, un pod no se reemplaza a sí mismo si se lo expulsa de un nodo por algún motivo.

Cada pod tiene un objeto de la API PodStatus, que se representa mediante el campo status de un pod. Los pods publican su fase en el campo status: phase. La fase de un pod es un resumen de alto nivel del pod en su estado actual.

Cuando ejecutas kubectl get pod para inspeccionar un pod que se ejecuta en tu clúster, el pod puede estar en una de las siguientes fases:

- Pendiente: El clúster creó y aceptó al pod, pero uno o más de sus contenedores aún no se ejecutan. En esta fase, se incluye el tiempo dedicado a la programación en un nodo y la descarga de imágenes.
- En ejecución: el pod se vinculó a un nodo y se crearon todos los contenedores. Al menos un contenedor está en ejecución, está en proceso de iniciarse o se está reiniciando.
- Exitoso: todos los contenedores en el pod terminaron con éxito. Los pods terminados no se reinician.
- Con errores: todos los contenedores en el pod terminaron y al menos un contenedor falló. Un contenedor “falla” si sale con un estado que no es cero.
- Desconocido: El estado del pod no se puede determinar.

Debido a que los pods son efímeros, no es necesario crear pods de forma directa. Del mismo modo, como los pods no pueden repararse o reemplazarse por sí mismos, no se recomienda crear pods directamente.

En su lugar, puedes usar un controlador, como una Implementación, que crea y administra pods por ti. Los controladores también son útiles para implementar actualizaciones, como cambiar la versión de una aplicación que se ejecuta en un contenedor, ya que el controlador administra todo el proceso de actualización por ti.

## Referencias
- https://cloud.google.com/kubernetes-engine/docs/concepts/pod?hl=es-419#:~:text=Google%20Kubernetes%20Engine.-,%C2%BFQu%C3%A9%20es%20un%20pod%3F,como%20los%20contenedores%20de%20Docker.