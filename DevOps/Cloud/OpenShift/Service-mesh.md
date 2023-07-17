# OpenShift - Service Mesh

Una malla de servicios o service mesh, como el proyecto open source Istio, se utiliza para controlar el intercambio de datos entre las distintas partes de una aplicación. A diferencia de otros sistemas que también administran esta comunicación, la malla de servicios es una capa visible y específica de la infraestructura integrada a la aplicación, la cual puede registrar si las distintas partes interactúan bien o no, a fin de facilitar la optimización de las comunicaciones y evitar el tiempo de inactividad a medida que crece una aplicación.

Las partes de la aplicación se denominan "servicio" y dependen unas de otras para brindar a los usuarios lo que desean. Si alguien utiliza la aplicación de una tienda en línea para comprar un producto, debe saber si el artículo está disponible. Por lo tanto, el servicio que se conecta con la base de datos del inventario de la empresa se debe comunicar con la página web del producto, que a su vez debe comunicarse con el carrito de compras en línea del usuario. Si la tienda quiere ofrecer más beneficios, podría diseñar un servicio que recomiende productos a los usuarios dentro de la aplicación. Este nuevo servicio se comunicará con una base de datos de etiquetas de los productos para ofrecer recomendaciones y, además, debe comunicarse con la misma base de datos del inventario que necesitaba la página del producto; es decir, se trata de una gran cantidad de partes independientes y reutilizables.

Las aplicaciones modernas suelen dividirse de este modo: como una red de servicios en la cual cada uno de ellos desempeña una función comercial específica. Para ello, estos servicios deberían intercambiar datos permanentemente. ¿Pero qué sucede si algunos servicios, como la base de datos del inventario de la tienda minorista, sufren una sobrecarga de solicitudes? Entonces entra en juego la malla de servicios, que dirige las solicitudes de un servicio a otro para optimizar el funcionamiento en conjunto de las partes.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/686934c2-c697-4bae-aca7-22c9e3d24848">
</p>

## Funcionamiento de las mallas de servicios

La malla de servicios no agrega funciones nuevas al entorno de tiempo de ejecución de la aplicación; las aplicaciones siempre necesitan normas que especifiquen cómo se transfieren las solicitudes del punto A al B, independientemente de su arquitectura. Lo que distingue a la malla de servicios es que las normas que rigen la comunicación entre los servicios no se encuentran dentro de cada uno de ellos, sino que se extraen y se colocan en una capa de infraestructura.

Para ello, la malla de servicios se integra a la aplicación como un conjunto de proxies de red. Los proxies son un concepto común en el ámbito de la TI empresarial: si accede a esta página web desde una computadora de trabajo, es muy probable que haya utilizado un proxy.

Cuando se envía la solicitud para esta página, primero la recibe el proxy web de su empresa.

Una vez que la solicitud pasa la medida de seguridad del proxy, se envía al servidor que aloja esta página.

Luego, la página regresa al proxy y se vuelve a verificar en función de las medidas de seguridad.

Finalmente, se envía del proxy a usted.

En una malla de servicios, las solicitudes se envían entre los microservicios por medio de proxies en su propia capa de infraestructura. Por eso, los proxies individuales que forman una malla de servicios a veces se denominan "sidecars", ya que se ejecutan junto a cada uno de los servicios, y no dentro de ellos. En conjunto, estos proxies sidecar, que están separados de cada servicio, forman una red.

Sin una malla de servicios, se debe codificar cada microservicio para que incluya las normas que regirán la comunicación entre los servicios, lo cual distrae a los desarrolladores de los objetivos empresariales. También significa que los errores de comunicación son más difíciles de diagnosticar porque las normas de comunicación entre los servicios están ocultas dentro de cada uno de ellos.

