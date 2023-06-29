# Amazon Machine Image AMI - Amazon EC2
Amazon Elastic Compute Cloud (Amazon EC2) proporciona capacidad de computación escalable en la nube de Amazon Web Services (AWS). El uso de Amazon EC2 elimina la necesidad de invertir inicialmente en hardware, de manera que puede desarrollar e implementar aplicaciones en menos tiempo. Puede usar Amazon EC2 para lanzar tantos servidores virtuales como necesite, configurar la seguridad y las redes, y administrar el almacenamiento. Amazon EC2 le permite escalar hacia arriba o hacia abajo para controlar los cambios en los requisitos o los picos de popularidad, con lo que se reduce la necesidad de prever el tráfico.

Amazon EC2 ofrece las siguientes características:

- Entornos informáticos virtuales, conocidos como instancias

- Plantillas preconfiguradas para las instancias, conocidas como imágenes de máquina de Amazon (AMI), que empaquetan las partes que necesita para el servidor (incluido el sistema operativo y el software adicional)

- Varias configuraciones de CPU, memoria, almacenamiento y capacidad de red de las instancias, conocidos como tipos de instancias

- Información de inicio de sesión segura para las instancias con pares de claves (AWS almacena la clave pública y usted guarda la clave privada en un lugar seguro)

- Volúmenes de almacenamiento para datos temporales que se eliminan cuando una instancia se detiene, se termina o se pone en hibernación, lo que se conoce como volúmenes del almacén de instancias

- Volúmenes de almacenamiento persistente para los datos usando Amazon Elastic Block Store (Amazon EBS), conocidos como volúmenes de Amazon EBS

- Varias ubicaciones físicas para los recursos, como las instancias y los volúmenes de Amazon EBS, conocidas como regiones y zonas de disponibilidad

- Un firewall que permite especificar los protocolos, los puertos y los rangos de direcciones IP que pueden alcanzar las instancias mediante el uso de grupos de seguridad

- Direcciones IPv4 estáticas para informática en la nube dinámica, conocidas como direcciones IP elásticas

- Metadatos, conocidos como etiquetas, que se pueden crear y asignar a los recursos de Amazon EC2

- Redes virtuales que puede crear que están aisladas lógicamente del resto de la nube de AWS y que, opcionalmente, puede conectar a su propia red, conocidas como nubes virtuales privadas (VPC).

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/405e227c-fa26-4ac0-a01f-bc0eabf4625e">
</p>

## Tipos de instancias de Amazon EC2

Las instancias de Amazon EC2 son una combinación de procesadores virtuales (vCPU), memoria, red y, en algunos casos, unidades de procesamiento de gráficos (GPU) y almacenamiento de instancias. Cuando crea una instancia EC2, tiene que elegir cuánto necesita de cada uno de estos componentes.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/90f014e1-0041-4d70-a711-c88d409aca1d">
</p>

AWS ofrece una variedad de instancias que difieren según el rendimiento. Algunas instancias proporcionan más capacidad que otras. Para obtener información general sobre los detalles de capacidad de una instancia concreta, debe consultar el tipo de instancias. Los tipos de instancias consisten en un prefijo que identifica el tipo de cargas de trabajo para las que están optimizadas, seguido de un tamaño. Por ejemplo, el tipo de instancias c5.large se puede desglosar de la siguiente manera:

- c5 define la familia de instancias y el número de generación. En este caso, la instancia pertenece a la quinta generación de instancias de una familia de instancias optimizada para el cálculo genérico.

- large establece la cantidad de capacidad de la instancia.

## Ubicaciones de instancias EC2

De forma predeterminada, las instancias EC2 se colocan en una red denominada “Amazon Virtual Private Cloud (Amazon VPC) predeterminada”. Esta red se creó para que pueda comenzar fácilmente a utilizar Amazon EC2 sin aprender a crear y configurar una VPC.

Cualquier recurso que coloque en la VPC predeterminada será público y accesible a través de Internet, por lo que no debe colocar datos de clientes ni información privada en ella.

Una vez que esté más familiarizado con las redes en AWS, debe cambiar esta configuración predeterminada para elegir sus propias VPC personalizadas y restringir el acceso con mecanismos de enrutamiento y conectividad adicionales.

## Diseño para la alta disponibilidad

En la red, la instancia se encuentra en una zona de disponibilidad de su elección. Como ha aprendido anteriormente, los servicios de AWS que se encuentran en el ámbito del nivel de la zona de disponibilidad deben diseñarse teniendo en cuenta la alta disponibilidad.

Si bien las instancias EC2 suelen ser fiables, dos son mejores que una, y tres son mejores que dos. Especificar el tamaño de la instancia proporciona una ventaja a la hora de diseñar la arquitectura porque puede utilizar una mayor cantidad de instancias más pequeñas en lugar de unas más grandes.

Si su frontend solo tiene una única instancia y ocurre un error en la instancia, la aplicación se desactiva. Por otro lado, si la carga de trabajo se distribuye en 10 instancias y ocurre un error en una, solo pierde el 10 por ciento de su flota, y la disponibilidad de las aplicaciones apenas se ve afectada.

Al diseñar la arquitectura de cualquier aplicación para obtener alta disponibilidad, considere utilizar al menos dos instancias EC2 en dos zonas de disponibilidad independientes.

## Ciclo de vida de la instancia EC2

Una instancia EC2 cambia entre distintos estados desde el momento en que la crea hasta que se termina.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/4cba3a38-f3b5-4e38-93be-d288d776c614">
</p>

## Precio

Una de las formas de reducir los costos con Amazon EC2 es elegir la opción de precio adecuada para la ejecución de sus aplicaciones. AWS ofrece tres opciones de compra principales para las instancias EC2: instancias bajo demanda, reservadas y de spot.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/f6afe37c-abd4-4ce1-9047-e761dada3616">
</p>

### Pago por uso con las instancias bajo demanda

Con las instancias bajo demanda, paga por la capacidad de cómputo sin compromisos a largo plazo. La facturación comienza cuando la instancia se está ejecutando y se detiene cuando la instancia se encuentra en estado detenido o terminado. El precio por segundo de una instancia bajo demanda en ejecución es fijo.

Para las aplicaciones que requieren que los servidores se ejecuten todo el tiempo, es menos probable que se beneficie del modelo de precio bajo demanda, simplemente porque no hay ninguna situación en la que tenga que apagar los servidores. Por ejemplo, es posible que desee que el servidor web que aloja el frontend de su aplicación de directorio corporativo se ejecute las 24 horas, todos los días para que los usuarios puedan acceder al sitio web en cualquier momento. Incluso si no hay usuarios conectados a su sitio web, no querrá apagar los servidores que respaldan el sitio ante la posible actividad del usuario.

Si no pueden detenerse los servidores, considere utilizar una instancia reservada para ahorrar costos.

### Capacidad de reserva con las instancias reservadas (RI)

Las RI le proporcionan un descuento importante en comparación con el precio de las instancias bajo demanda. Las RI ofrecen una tarifa horaria con descuento y una reserva de capacidad opcional para las instancias EC2. Puede elegir entre tres opciones de pago: el pago total anticipado, el pago inicial parcial o sin pago inicial. Puede seleccionar un periodo de 1 año o 3 años para cada una de estas opciones.

Según la opción que elija, recibe un descuento diferente.

Pago total anticipado ofrece un descuento superior al de las instancias de pago inicial parcial.
Las instancias de pago inicial parcial ofrecen un descuento mayor que sin pago inicial.
Sin pago inicial  ofrece un descuento superior al de las instancias bajo demanda.
Las instancias bajo demanda y sin pago inicial son similares, ya que en ninguno de los dos casos se requiere un pago inicial. Sin embargo, hay una diferencia importante. Cuando elige una instancia bajo demanda, deja de pagar por la instancia cuando la detiene o la termina. Cuando detiene una RI, sigue pagando por ella porque se comprometió a cumplir un término de 1 o 3 años.

Las instancias reservadas se asocian a un tipo de instancias y a una zona de disponibilidad en función de cómo las reserve. El descuento aplicado por una compra de instancia reservada no se asocia directamente a un ID de instancia específico, sino a un tipo de instancias.

### Ahorro de costos con las instancias de spot

Otra forma de pagar las instancias EC2 es mediante instancias de spot. Las instancias de spot de Amazon EC2 le permiten aprovechar la capacidad de EC2 sin utilizar en la nube de AWS. Están disponibles hasta con un 90 % de descuento en comparación con los precios bajo demanda.

Con las instancias de spot, establece un límite al pago por la hora de la instancia. Esto se compara con el precio de spot actual que define AWS. Si el monto que paga es superior al precio de spot actual y hay capacidad, recibirá una instancia. Aunque son muy prometedoras desde el punto de vista de la facturación, debe tener en cuenta algunas consideraciones de arquitectura para utilizarlas de manera efectiva.

Una consideración es que la instancia de spot podría interrumpirse. Por ejemplo, si AWS determina que la capacidad ya no está disponible para una instancia de spot concreta o si el precio de spot supera la cantidad que está dispuesto a pagar, AWS le dará una advertencia de 2 minutos antes de interrumpir la instancia. Esto significa que cualquier aplicación o carga de trabajo que se ejecute en una instancia de spot debe poder interrumpirse.

Debido a esta consideración única, las cargas de trabajo inherentemente tolerantes a errores suelen ser buenos candidatos para utilizar con las instancias de spot. Se incluyen big data, las cargas de trabajo en contenedores, la integración y entrega continuas (CI/CD), los servidores web, la informática de alto rendimiento (HPC), el renderizado de imágenes y medios, y otras cargas de trabajo de prueba y desarrollo.