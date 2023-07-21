# Amazon Elastic Block Store - Amazon EBS

Amazon Elastic Block Store (Amazon EBS) es un servicio de almacenamiento en bloque fácil de usar, escalable y de alto rendimiento diseñado para Amazon Elastic Compute Cloud (Amazon EC2).

En la siguiente imagen podremos analizar el esquema del servicio mencionado

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/b9bad3e9-834a-4ed6-ab2b-d6997b3dbb98">
</p>

Amazon EBS también se encarga de la creación de volúmenes de almacenamiento para que puedan adjuntarse a las instancias de Amazon EC2. Después de este proceso, se pueden desarrollar sistemas de archivos sobre los volúmenes, ejecutar alguna base de datos o bien asignarle alguno de los usos disponibles para el almacenamiento en bloque, como, por ejemplo, en un disco duro.

El sistema de Amazon EBS incluye una serie de propiedades y características que permiten su funcionamiento, dentro de los que se pueden incluir su utilidad para trabajar en situaciones donde los datos deben mantenerse accesibles de manera rápida y donde se requiera persistencia a largo plazo.

Cabe resaltar también que esta herramienta ofrece diferentes tipos de volúmenes, que se ubican en una determinada zona de disponibilidad, donde se replican de manera automática con el objetivo de garantizar su protección frente a errores de componentes individuales. Estos volúmenes también se encuentran diseñados para ofrecer una alta disponibilidad.

La facturación de Amazon EBS se lleva a cabo teniendo en cuenta únicamente lo que se aprovisiona con la herramienta. En lo que respecta al almacenamiento de volumen, vale aclarar que estos se facturan de acuerdo con la cantidad de GN que se aprovisionan al mes hasta liberar la capacidad almacenada. Estos costes pueden aumentar para los volúmenes con funciones especiales, como un rendimiento mayor al de referencia o que admitan IOPS.


## Tipos de volúmenes de Amazon EBS

Los volúmenes de Amazon EBS se organizan en dos categorías principales: discos de estado sólido (SSD) y discos duros (HDD). Las SSD proporcionan un alto rendimiento para la entrada y salida (E/S) aleatorias, mientras que las HDD proporcionan un alto rendimiento para la E/S secuenciales. AWS ofrece dos tipos de cada una.

El siguiente gráfico puede ayudarlo a decidir qué volumen de EBS es la opción correcta para su carga de trabajo.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/b9bad3e9-834a-4ed6-ab2b-d6997b3dbb98">
</p>

## Ventajas de Amazon EBS

Estas son las ventajas de utilizar Amazon EBS.

- Alta disponibilidad: cuando crea un volumen de EBS, se replica automáticamente en su zona de disponibilidad para evitar la pérdida de datos por puntos únicos de error.

- Persistencia de datos: el almacenamiento persiste incluso cuando la instancia no lo hace.

- Cifrado de datos: Todos los volúmenes de EBS admiten el cifrado.

- Flexibilidad: los volúmenes de EBS admiten cambios sobre la marcha. Puede modificar el tipo de volumen, el tamaño del volumen y la capacidad de las operaciones de entrada/salida por segundo (IOPS) sin detener la instancia.

- Copias de seguridad: Amazon EBS proporciona la capacidad de crear copias de seguridad de cualquier volumen de EBS.

## Instantáneas de Amazon EBS

Los errores ocurren. Un error es no hacer copias de seguridad de los datos y luego perderlos inevitablemente. Para evitar que esto le ocurra, realice siempre copia de seguridad de los datos, incluso en AWS.

Dado que los volúmenes de EBS se componen de los datos de su instancia de Amazon EC2, debe realizar copias de seguridad de estos volúmenes, denominadas “instantáneas”.

Las instantáneas de EBS son copias de seguridad progresivas que solo guardan los bloques del volumen que han cambiado después de la instantánea más reciente. Por ejemplo, si tiene 10 GB de datos en un volumen y solo se han modificado 2 GB de datos desde la última instantánea, solo los 2 GB que se han modificado se escriben en Amazon Simple Storage Service (Amazon S3).

Cuando realiza una instantánea de cualquiera de los volúmenes de EBS, las copias de seguridad se almacenan de forma redundante en varias zonas de disponibilidad mediante Amazon S3. AWS gestiona este aspecto del almacenamiento de la copia de seguridad en Amazon S3, por lo que no tendrá que interactuar con Amazon S3 para trabajar con sus instantáneas de EBS. Las administra en la consola de Amazon EBS, que forma parte de la consola Amazon EC2.

Las instantáneas de EBS se pueden utilizar para crear varios volúmenes nuevos, tanto si se encuentran en la misma zona de disponibilidad como en otra. Cuando crea un nuevo volumen a partir de una instantánea, es una copia exacta del volumen original en el momento en que se tomó la instantánea.

## Referencias
- https://aws.amazon.com/es/ebs/
- https://keepcoding.io/blog/que-es-amazon-ebs/
