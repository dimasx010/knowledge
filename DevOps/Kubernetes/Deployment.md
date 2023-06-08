# Deployment

## General

La herramienta Deployment se define como un controlador de la plataforma que tiene la labor de ofrecer actualizaciones declarativas enfocados en los ReplicaSets y pods disponibles.

De manera que, cuando se establece un estado deseado en un objeto de esta opción, Deployment se encarga de llevar a cabo, de una manera controlada, la transición entre el estado actual en el que se encuentre el objeto hacia el estado deseado indicado por el usuario. Esto implica que los pods que estén a cargo de este controlador deban alcanzar dicho estado.

Dentro de los principales elementos característicos de Deployment, se encuentra que este también puede definirse para otras labores, como la creación de nuevos recursos de ReplicaSets, o bien eliminar la totalidad de los Deployments que existan en el sistema, al tiempo que adopta todos sus recursos con nuevos controladores de Deployment.

Se recomienda, además, no gestionar de manera directa los recursos de ReplicaSets que forman parte de un Deployment.

Otra de las características de este controlador es que tiene la capacidad de indicarle al sistema de Kubernetes cómo se debe realizar la creación o edición de las instancias de los recursos de pods que incluyan una aplicación contenerizada.

Este controlador también se caracteriza por contar con la posibilidad de escalar la cantidad de los pods de réplica, dependiendo de las necesidades de las infraestructuras del usuario, así como contribuir a que se implemente la actualización del código controladamente.

Del mismo modo, tiene la capacidad de ir a una versión anterior de Deployment en los casos donde sea requerido. Cabe resaltar que cada uno de estos retrocesos actualiza la revisión del elemento.

Esta herramienta también tiene la propiedad de automatizar las labores y funciones manuales que tienden a ser repetitivas y que se encuentran interviniendo en sus procesos de escalado y actualización de las aplicaciones en producción. Esta automatización de los procesos puede ser traducida en Deployments que funcionen de una manera más rápida y que tenga menos errores en sus actividades.

Además, el estado de este controlador puede utilizarse con el objetivo de indicar que un determinado despliegue se ha atascado.

Deployment se caracteriza, además, por permitir una serie de casos de uso diferentes dentro de la plataforma. Todos estos casos deberían cubrirse al usar el objeto de Deployment.

Además de esto, si sucede que el cliente quiere implementar un caso de uso que aparece como no soportado por el sistema, se dispone de la opción de abrir un nuevo incidente en el interior del repositorio principal de la plataforma de Kubernetes.

Algunos de los casos de uso que normalmente lleva a cabo el controlador de Deployment son:

##Despliegue de ReplicaSet
Uno de los casos de uso de este controlador se da cuando el ReplicaSet se encarga de la creación de los recursos de pods que funcionan en un segundo plano. Además de esto, el controlador de Deployment cumple la función de verificar el estado de despliegue del recurso con el objetivo de comprobar que este sea el ideal o no.

##Limpieza de ReplicaSet
Otro de los casos de uso del controlador de Deployment es que permite limpiar los recursos de ReplicaSet que sean más antiguos y que ya no se necesiten en el sistema.

##Escalado
Deployment también se caracteriza por permitir el escalado de tipo horizontal, lo que contribuye a que el controlador aumente su capacidad para soportar las diferentes cargas de trabajo.
