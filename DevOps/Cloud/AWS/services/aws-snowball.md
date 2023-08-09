# AWS Snowball

En la consola de la familia de productos AWS Snow, seleccione su dispositivo preferido, ya sea Snowball Edge Compute Optimized o Snowball Edge Storage Optimized. Cree un trabajo con un bucket de Amazon S3, seleccione Amazon Simple Notification Service (Amazon SNS) para el rastreo, y configure opciones como las AMI de Amazon EC2 y una GPU. AWS prepara y le envía el dispositivo, y usted lo recibe en aproximadamente 4 a 6 días. Una vez que el dispositivo llega, enciéndalo y use AWS OpsHub para desbloquearlo. Conéctese a su LAN. Use AWS OpsHub para administrar el dispositivo, transferir datos o iniciar instancias de EC2. Cuando lo haga, apague y regrese el dispositivo a AWS. La etiqueta de envío aparece automáticamente en la pantalla de tinta electrónica. Cuando llega el dispositivo a la región de AWS, cualquier dato que tenga almacenado en sus buckets a bordo se trasladan a su bucket S3 y se verifica al mismo tiempo que usted carga el dispositivo. Todos los datos se borran de manera segura del dispositivo, y limpian de cualquier información del cliente.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/7ed1de7a-5460-4765-9bf2-918b06f515c7">
</p>

## Casos de uso

### Migre datos a escala de petabytes
Transfiera bases de datos, copias de seguridad, archivos, registros sanitarios, conjuntos de datos de análisis, contenido multimedia y datos de sensores con IoT, especialmente cuando las condiciones de la red son limitadas.

### Procese y analice datos de forma local
Ejecute las imágenes de máquina de Amazon (AMI) en Amazon EC2 e implemente código de AWS Lambda en dispositivos Snowball Edge con machine learning (ML) u otras aplicaciones.

### Optimice los datos de fabricación
Recopile y analice datos de plantas de producción locales para perfeccionar los procesos y mejorar la seguridad, la eficiencia y la productividad.

## References
- https://aws.amazon.com/es/snowball/
