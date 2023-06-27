# Auto-Scaling - Amazon EC2

Amazon EC2 Auto Scaling lo ayuda a garantizar que cuenta con la cantidad correcta de instancias de Amazon EC2 disponibles para gestionar la carga de su aplicación. Crea colecciones de instancias EC2, denominadas grupos de Auto Scaling. Puede especificar el número mínimo de instancias en cada grupo de escalado automático y Amazon EC2 Auto Scaling garantizará que el grupo nunca tenga menos de esas instancias. Puede especificar el número máximo de instancias en cada grupo de escalado automático y Amazon EC2 Auto Scaling garantizará que el grupo nunca tenga más de esas instancias. Si especifica la capacidad deseada, cuando crea el grupo o con posterioridad, Amazon EC2 Auto Scaling garantizará que el grupo tenga ese número de instancias. Si especifica políticas de escalado, Amazon EC2 Auto Scaling puede lanzar o terminar instancias conforme aumente o disminuya la demanda de su aplicación.

Por ejemplo, el siguiente grupo de escalado automático tiene un tamaño mínimo de una instancia, una capacidad deseada de dos instancias y un tamaño máximo de cuatro instancias. Las políticas de escalado que defina ajustan el número de instancias, en el número mínimo y máximo de instancias, en función de los criterios que especifique.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/a1c3e2ac-b718-43df-a169-01d80445df21">
</p>

## Beneficios

Al añadir Adding Amazon EC2 Auto Scaling a su arquitectura de aplicaciones es una forma de obtener el máximo beneficio de la nube de AWS. Cuando se utiliza Amazon EC2 Auto Scaling, sus aplicaciones disfrutan de los siguientes beneficios:

- Mejor tolerancia a errores. Amazon EC2 Auto Scaling puede detectar cuándo una instancia está en mal estado, terminarla y lanzar una instancia para reemplazarla. También puede configurar Amazon EC2 Auto Scaling para que use varias zonas de disponibilidad. Si una zona de disponibilidad deja de estar disponible, Amazon EC2 Auto Scaling puede lanzar instancias en otra para compensar.

- Mejor disponibilidad. Amazon EC2 Auto Scaling puede ayudarle a garantizar que la aplicación tiene siempre la capacidad adecuada para gestionar la demanda de tráfico actual.

- Mejor administración de costes. Amazon EC2 Auto Scaling puede aumentar y reducir de forma dinámica la capacidad según sea necesario. Dado que se paga por las instancias EC2 que se utilizan, es posible ahorrar dinero lanzando instancias cuando se necesitan y terminándolas cuando ya no son necesarias.

## References
- https://docs.aws.amazon.com/es_es/autoscaling/ec2/userguide/what-is-amazon-ec2-auto-scaling.html