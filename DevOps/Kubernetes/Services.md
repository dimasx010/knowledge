# Services

## General

Primeramente debemos destacar la motivación u objetivo de un servicio. 

Los Pods de Kubernetes son creados y destruidos para coincidir con el estado de tu clúster. Los Pods son recursos no permanentes. Si utilizas un Deployment para correr tu aplicación, puede crear y destruir los Pods dinámicamente.

Cada Pod obtiene su propia dirección IP, sin embargo, en un Deployment, el conjunto de Pods corriendo en un momento dado puede ser diferente al conjunto de Pods corriendo esa aplicación un momento después.

Esto conlleva un problema: si un conjunto de Pods (llamémoslos "backends") provee funcionalidad a otros Pods (llamémoslos "frontends") dentro de tu clúster, ¿de qué manera los frontends encuentran y tienen seguimiento de cuál dirección IP conectarse, para que el frontend pueda usar la parte del backend de la carga de trabajo?

En Kubernetes, un Service es una abstracción que define un conjunto lógico de Pods y una política por la cual acceder a ellos (algunas veces este patrón es llamado micro-servicio). El conjunto de Pods a los que apunta un Servicio se determina usualmente por un Selector. Para aprender más sobre otras maneras de definir Endpoints para un Service, mira Services sin selectores.

Por ejemplo, considera un backend sin estado para procesar imágenes que está corriendo con 3 réplicas. Estas réplicas son fungibles; a los frontends no les importa cuál backend usar. Mientras que los Pods actuales que componen el backend pueden cambiar, los clientes del frontend no deberían estar al tanto de ello, ni deberían llevar un seguimiento del conjunto de backends en sí mismos.

La abstracción del Service habilita este desacoplamiento

Service en Kubernetes es un objeto REST, similar a un Pod. Como todos los objetos REST, puedes hacer un Post a una definición de un Service al servidor API para crear una nueva instancia. EL nombre de un objeto Service debe ser un nombre RFC 1035 válido.

Por ejemplo, supongamos que tienes un conjunto de Pods en el que cada uno escucha el puerto TCP 9376 y contiene la etiqueta app.kubernetes.io/name=MyApp:

```yaml
​apiVersion: v1
kind: Service
metadata:
  name: mi-servicio
spec:
  selector:
    app.kubernetes.io/name: MyApp
  ports:
    - protocol: TCP
      port: 80
      targetPort: 9376

```

Entre los tipos de cluster tenemos: 

## ClusterIP

Cuando creas un servicio de tipo ClusterIP, Kubernetes crea una dirección IP estable a la que se puede acceder desde los nodos del clúster. A continuación, se muestra un manifiesto de un servicio de tipo ClusterIP:

```yaml
apiVersion: v1
kind: Service
metadata:
  name: my-cip-service
spec:
  selector:
    app: metrics
    department: sales
  type: ClusterIP
  ports:
  - protocol: TCP
    port: 80
    targetPort: 8080

```

## NodePort

Cuando creas un servicio del tipo NodePort, Kubernetes proporciona un valor nodePort. Luego, se puede acceder al servicio mediante la dirección IP de cualquier nodo junto con el valor nodePort.

Aquí hay un manifiesto para un servicio de tipo NodePort

```yaml
apiVersion: v1
kind: Service
metadata:
  name: my-np-service
spec:
  selector:
    app: products
    department: sales
  type: NodePort
  ports:
  - protocol: TCP
    port: 80
    targetPort: 8080

```

## LoadBalancer

Un «load balancer» o balanceador de carga permite repartir la carga de trabajo entre los diferentes servidores o aplicaciones y puede instalarse en una infraestructura tanto física como virtual. Así pues, los programas de load balancing adoptan la forma de un controlador de entrega de aplicaciones o ADC (del inglés «aplicación delivery controller»), permitiendo al usuario escalar la carga automáticamente en función de las previsiones de tráfico.

El balanceo de carga, como acabamos de ver, es solo una de las posibles aplicaciones del load balancer. Y es que esta tecnología también resulta especialmente útil para descongestionar un certificado SSL, actualizar grupos de aplicaciones o incluso enrutar sus dominios.

​Existen dos tipos de load balancers:

### ​Load balancers L4 o balanceadores de carga de red

Estos balanceadores tratan los datos de la capa («layer») 4 que están presentes a nivel de red y transporte (TCP/UDP). Así pues, los balanceadores de carga no se centran en la información aplicativa, como el tipo de contenido, las cookies, la localización de los headers, etc., sino que redirigen el tráfico basándose en los datos de la capa de red.

### ​Load balancers L7 o balanceadores de carga de aplicación

​A diferencia de los L4, estos balanceadores redirigen el tráfico basándose en los parámetros de la capa de aplicación, por lo que tratan un volumen de datos superior y utilizan una mayor cantidad de información, incluyendo, por ejemplo, los protocolos HTTP, HTTPS y SSL.

## Referencias
- https://kubernetes.io/es/docs/concepts/services-networking/service/#:~:text=En%20Kubernetes%2C%20un%20Service%20es,determina%20usualmente%20por%20un%20Selector.
- https://www.ovhcloud.com/es/public-cloud/kubernetes/kubernetes-load-balancer/#:~:text=Un%20%C2%ABload%20balancer%C2%BB%20o%20balanceador,infraestructura%20tanto%20f%C3%ADsica%20como%20virtual.
