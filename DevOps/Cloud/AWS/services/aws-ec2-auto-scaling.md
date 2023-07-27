# Auto-Scaling - Amazon EC2

Amazon EC2 Auto Scaling helps ensure that you have the right number of Amazon EC2 instances available to handle your application load. It creates collections of EC2 instances, called Auto Scaling groups. You can specify the minimum number of instances in each Auto Scaling group, and Amazon EC2 Auto Scaling will ensure that the group never has fewer than those instances. You can specify the maximum number of instances in each Auto Scaling group and Amazon EC2 Auto Scaling will ensure that the group never has more than those instances. If you specify the desired capacity, when you create the group or later, Amazon EC2 Auto Scaling will ensure that the group has that number of instances. If you specify scaling policies, Amazon EC2 Auto Scaling can launch or terminate instances as your application demand increases or decreases.

For example, the following Auto Scaling group has a minimum size of one instance, a desired capacity of two instances, and a maximum size of four instances. The scaling policies you define adjust the number of instances, in minimum and maximum number of instances, based on the criteria you specify.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/a1c3e2ac-b718-43df-a169-01d80445df21">
</p>

## Benefits

Adding Amazon EC2 Auto Scaling to your application architecture is one way to get the maximum benefit from the AWS cloud. When you use Amazon EC2 Auto Scaling, your applications enjoy the following benefits:

- Improved fault tolerance. Amazon EC2 Auto Scaling can detect when an instance is down, terminate it, and launch an instance to replace it. You can also configure Amazon EC2 Auto Scaling to use multiple Availability Zones. If one Availability Zone becomes unavailable, Amazon EC2 Auto Scaling can launch instances in another to compensate.

- Better availability. Amazon EC2 Auto Scaling can help you ensure that your application always has adequate capacity to handle current traffic demand.

- Better cost management. Amazon EC2 Auto Scaling can dynamically scale capacity up and down as needed. Since you pay for the EC2 instances you use, you can save money by launching instances when you need them and terminating them when they are no longer needed.

## Configuración de los componentes de EC2 Auto Scaling

Los tres componentes principales de EC2 Auto Scaling son los siguientes:

Configuración o plantilla de lanzamiento: ¿Qué recurso debe escalarse automáticamente?

Grupo de Auto Scaling EC2: ¿Dónde deben implementarse los recursos?

Políticas de escalado: ¿Cuándo deben añadirse o eliminarse los recursos?

### Plantillas de lanzamiento

Se necesitan varios parámetros para crear instancias EC2: ID de Amazon Machine Image (AMI), tipo de instancias, grupo de seguridad, volúmenes adicionales de Amazon Elastic Block Store (EBS) y más. EC2 Auto Scaling también requiere toda esta información para crear la instancia EC2 en su nombre cuando tenga que escalarse. Esta información se almacena en una plantilla de lanzamiento.

Puede utilizar una plantilla de lanzamiento para lanzar manualmente una instancia EC2. También puede utilizarla con EC2 Auto Scaling. Asimismo, admite el control de versiones, lo que permite hacer rápidamente una restauración si hay un problema o es necesario especificar una versión predeterminada. De esta forma, mientras iteran en una nueva versión, otros usuarios pueden continuar lanzando instancias EC2 por medio de la versión predeterminada hasta que realice los cambios necesarios.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/2a07da81-0375-4fbf-b62c-d524771d495d">
</p>

Puede crear una plantilla de lanzamiento de una de estas tres formas.

La forma más rápida para crear una plantilla es utilizar una instancia EC2 actual. La totalidad de la configuración ya está definida.

Otra opción es crear una plantilla a partir de una actual o de una versión anterior de una plantilla de lanzamiento.

La última opción es crear una plantilla desde cero. Deberán definirse las siguientes opciones: ID de la AMI, tipo de instancias, par de claves, grupo de seguridad, almacenamiento y etiquetas de recursos.

Otra forma de definir lo que Amazon EC2 Auto Scaling tiene que escalar es mediante una configuración de lanzamiento. Es similar a la plantilla de lanzamiento, pero no permite el control de versiones al utilizar una configuración de lanzamiento creada anteriormente como plantilla. Tampoco permite crearla a partir de una instancia EC2 actual. Por estos motivos y para garantizar que obtiene las características más recientes de Amazon EC2, AWS recomienda utilizar una plantilla de lanzamiento en lugar de una configuración de lanzamiento.

### Grupos de EC2 Auto Scaling

El siguiente componente que necesita EC2 Auto Scaling es un grupo de Auto Scaling EC2. Un grupo de Auto Scaling lo ayuda a definir dónde EC2 Auto Scaling implementa sus recursos. Aquí es donde especifica Amazon VPC y las subredes en las que se debe lanzar la instancia EC2. EC2 Auto Scaling se encarga de crear las instancias EC2 en las subredes, así que seleccione al menos dos subredes que se encuentren en distintas zonas de disponibilidad.

Con los grupos de Auto Scaling, puede especificar el tipo de compra para las instancias EC2. Puede utilizar solo bajo demanda, solo spot o una combinación de las dos, lo que le permite aprovechar las instancias de spot con una sobrecarga administrativa mínima.

Para especificar cuántas instancias debe lanzar EC2 Auto Scaling, dispone de tres configuraciones de capacidad para configurar el tamaño del grupo.

Mínima: se refiere al número mínimo de instancias que se ejecutan en el grupo de Auto Scaling, incluso si se alcanza el umbral para reducir la cantidad de instancias.
Máxima: indica el número máximo de instancias que se ejecutan en el grupo de Auto Scaling, incluso si se alcanza el umbral para añadir nuevas instancias.
Capacidad deseada: indica la cantidad de instancias que debe haber en el grupo de Auto Scaling. Este número solo puede acercarse o ser igual al mínimo o al máximo. EC2 Auto Scaling añade o elimina instancias automáticamente para que coincidan con el número de capacidad deseado.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/d5fee1eb-8bb1-4720-98b7-2e7791bfa82e">
</p>

Cuando EC2 Auto Scaling elimina instancias EC2 porque el tráfico es mínimo, sigue eliminando instancias EC2 hasta que alcanza una capacidad mínima. Según la aplicación, utilizar un mínimo de dos es una buena idea para garantizar la alta disponibilidad, pero usted sabe cuántas instancias EC2 requiere su aplicación como mínimo en todo momento. Al alcanzar ese límite, incluso si se indica a EC2 Auto Scaling que elimine una instancia, no lo hace para garantizar que se mantenga el mínimo.

Por otro lado, cuando el tráfico sigue aumentando, EC2 Auto Scaling sigue añadiendo instancias EC2. Significa que el costo de su aplicación también seguirá aumentando. Por eso debe fijar un monto máximo para asegurarse de que no supere el presupuesto.

La capacidad deseada es la cantidad de instancias EC2 que EC2 Auto Scaling crea en el momento de crear el grupo. Si ese número disminuye, EC2 Auto Scaling elimina la instancia más antigua de forma predeterminada. Si ese número aumenta, EC2 Auto Scaling crea nuevas instancias por medio de la plantilla de lanzamiento.

### Disponibilidad con EC2 Auto Scaling

Se utilizan diferentes números de capacidad mínima, máxima y deseada para ajustar dinámicamente la capacidad. Sin embargo, si prefiere utilizar EC2 Auto Scaling para la administración de flotas, puede configurar las tres configuraciones en el mismo número, por ejemplo cuatro, como se muestra en la imagen. EC2 Auto Scaling garantizará que si una instancia EC2 pasa a tener mal estado, la reemplaza para garantizar que siempre haya cuatro instancias EC2 disponibles. De esta forma, se garantiza una alta disponibilidad para sus aplicaciones.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/8ca5ac45-3bcc-40d0-8fd4-91927390a82c">
</p>

Automatización con políticas de escalado

De forma predeterminada, un grupo de Auto Scaling se mantendrá en la capacidad deseada inicial. Si bien es posible cambiar manualmente la capacidad deseada, también puede utilizar políticas de escalado.

En el módulo sobre monitoreo de AWS, aprendió acerca de las métricas y las alarmas de Amazon CloudWatch. Las métricas se utilizan para conservar la información sobre los distintos atributos de la instancia EC2, como el porcentaje de la CPU. Las alarmas se utilizan para especificar una acción cuando se alcanza un umbral. Las métricas y las alarmas son lo que utilizan las políticas de escalado para saber cuándo actuar. Por ejemplo, puede configurar una alarma que indique cuando la utilización de la CPU supera el 70 % en toda la flota de instancias EC2 y desencadenar una política de escalado a fin de añadir una instancia EC2.

Hay tres tipos de políticas de escalado disponibles: escalado simple, de pasos, y de seguimiento de destino.

Política de escalado simple

Una política de escalado sencilla le permite hacer exactamente lo que se describe en este módulo. Utiliza una alarma de CloudWatch y especifica qué hacer cuando se activa. Puede tratarse de un número de instancias EC2 que se deben añadir o quitar, o de un número específico en el que establecer la capacidad deseada. Puede especificar un porcentaje del grupo en lugar de utilizar una cantidad de instancias EC2, lo que hace que el grupo crezca o se reduzca con mayor rapidez.

Una vez activada la política de escalado, espera un periodo de recuperación antes de realizar cualquier otra acción. Es importante porque las instancias EC2 tardan tiempo en iniciarse, y la alarma de CloudWatch podría activarse mientras se inicia la instancia EC2. Por ejemplo, podría decidir añadir una instancia EC2 si la utilización de la CPU en todas las instancias superara el 65 %. No quiere añadir más instancias hasta que la nueva instancia EC2 acepte el tráfico. Sin embargo, ¿qué ocurriría si la utilización de la CPU superara el 85 % en el grupo de Auto Scaling? Es posible que añadir una instancia no sea la decisión correcta. En cambio, es posible que quiera añadir otro paso en la política de escalado. Lamentablemente, una política de escalado simple no puede ayudar con eso.

Política de escalado por pasos

Aquí es donde es útil una política de escalado por pasos. Las políticas de escalado por pasos responden a las alarmas adicionales incluso mientras se está realizando una actividad de escalado o un reemplazo de comprobaciones de estado. Al igual que en el ejemplo anterior, podría decidir añadir dos instancias más cuando la utilización de la CPU sea del 85 % y cuatro instancias más cuando sea del 95 %.

Decidir cuándo añadir y quitar instancias de acuerdo con las alarmas de CloudWatch podría parecer una tarea difícil. Por eso existe el tercer tipo de política de escalado: el seguimiento de destino.

Política de escalado de seguimiento de destino
Si la aplicación se escala según la utilización promedio de la CPU, la utilización de la red promedio (dentro o fuera) o el recuento de solicitudes, este tipo de política de escalado es el que se debe utilizar. Todo lo que tiene que proporcionar es el valor de destino al que se va a dar seguimiento, y se crean automáticamente las alarmas de CloudWatch necesarias.

## References
- https://docs.aws.amazon.com/en_en/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html