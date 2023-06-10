# AWS Kinesis

Se puede utilizar Amazon Kinesis Data Streams para recopilar y procesar grandes Flujos de registros de datos en tiempo real. Puede crear aplicaciones de procesamiento de datos, conocidas como Aplicaciones de Kinesis Data Streams. Una aplicación de Kinesis Data Streams lee datos de un flujo de datos como registros de datos. Estas aplicaciones pueden utilizar la biblioteca cliente de Kinesis y pueden ejecutarse en instancias de Amazon EC2. Puede enviar los registros procesados a paneles, utilizarlos para generar alertas, cambiar dinámicamente las estrategias de precios y publicidad o enviar datos a una variedad de otras AWSServicios.

<p align="center">
  <img width="460" height="300" src="https://github.com/dimasx010/knowledge/assets/105082657/a6d3ee1b-1a23-4ae6-8ae2-404f1066e0a0">
</p>

Aunque puede utilizar Kinesis Data Streams para resolver diversos problemas relacionados con los datos de streaming, uno de sus usos más habituales es la agregación de datos en tiempo real, seguida de la carga de los datos agregados en un almacén de datos o un clúster de MapReduce.

Los datos se insertan en secuencias de datos de Kinesis, lo que garantiza su durabilidad y elasticidad. El tiempo que transcurre entre el momento en que un registro se inserta en la secuencia y el momento en el que se puede recuperar (put-to-getretraso) es normalmente menor que 1 segundo. En otras palabras, una aplicación de Kinesis Data Streams puede empezar a consumir los datos de la secuencia casi inmediatamente tras agregarlos. El aspecto de servicio administrado de Kinesis Data Streams alivia la carga operativa de crear y ejecutar una canalización de admisión de datos. Puede crear aplicaciones en streaming de tipo MapReduce. La elasticidad de Kinesis Data Streams le permite aumentar o reducir la secuencia de forma que nunca pierda registros de datos antes de su vencimiento.

Varias aplicaciones de Kinesis Data Streams pueden consumir datos de una secuencia, de forma que es posible realizar varias acciones de forma simultánea e independiente, como el archivado y el procesamiento. Por ejemplo, dos aplicaciones pueden leer datos de la misma secuencia. La primera aplicación calcula las agrupaciones en ejecución y actualiza una tabla de Amazon DynamoDB, mientras que la segunda aplicación comprime y archiva datos en un almacén de datos como Amazon Simple Storage Service (Amazon S3). La tabla de DynamoDB con las agrupaciones en ejecución pasa a un panel, que la lee y elabora up-to-the informes de minutos.

La biblioteca cliente de Kinesis Data Streams permite un consumo de datos tolerante a errores a partir de las secuencias y proporciona asistencia al escalado para las aplicaciones de Kinesis Data Streams.

## Referencias
- https://docs.aws.amazon.com/es_es/streams/latest/dev/introduction.html

