# AWS Storage Gateway

AWS Storage Gateway es un servicio de almacenamiento híbrido que permite que las aplicaciones que se encuentran en sitio puedan utilizar almacenamiento prácticamente ilimitado de la nube de AWS, de manera transparente y sin contratiempos. Storage Gateway no requiere cambios en sus aplicaciones y se integra fácilmente ya que utiliza protocolos de comunicación y almacenamiento estándar como HTTPS (HTTP sobre SSL/TLS) para comunicación con la nube, así como SMB (Server Message Block) y NFS (Network File System) para el acceso a los datos almacenados. Mediante Storage Gateway, usted puede ampliar su capacidad local de almacenamiento mientras reduce y simplifica la infraestructura de su centro de datos o de sus oficinas remotas.

Nuestros clientes alrededor del mundo utilizan Storage Gateway para ampliar sus capacidades de respaldo y archivado, así como para reemplazar sistemas de almacenamiento en sitio por almacenamiento localizado en la nube. Muchos clientes también utilizan Storage Gateway para colocar sus datos en la nube y poder analizarlos y transformarlos aprovechando los servicios de Analítica de Datos disponibles en AWS.

En esta publicación usted conocerá acerca del servicio de Storage Gateway y sus diferentes modalidades y aprenderá como configurarlo en su modalidad de File Gateway simulando un Centro de Datos en AWS.

## ¿Cómo funciona?

Las aplicaciones se conectan al servicio de Storage Gateway a través de una máquina virtual o dispositivo de hardware que se instala en sitio y que utiliza protocolos estándar como NFS, SMB e iSCSI. Este dispositivo local se conecta al servicio de Storage Gateway que a su vez se conecta con los servicios de almacenamiento de AWS tales como Amazon S3, Amazon S3 Glacier, Amazon S3 Glacier Deep Archive y Amazon EBS y de esta manera se provee almacenamiento para sus aplicaciones y usuarios que se encuentran en sitio. Este dispositivo también se utiliza como caché local para proveer un acceso de baja latencia a los datos más activos. Como en AWS nuestra prioridad es la seguridad, la conexión al servicio de AWS Storage Gateway se hace por medio de un canal seguro utilizando HTTPS.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/af31b90d-76c3-4f91-9bad-86fed26124b6">
</p>

AWS Storage Gateway existe en tres modalidades:

- File Gateway, para aplicaciones que requieren almacenamiento basado en sistemas de archivos que se presentan como carpetas compartidas (File Share). Storage Gateway provee interfaces SMB y NFS y almacena los archivos como objetos en Amazon S3.

- Volume Gateway, que le permite presentar almacenamiento de bloque a sus servidores por medio de iSCSI. Volume Gateway opera en modo caché, en el cual sus datos se almacenan en Amazon S3 y los datos accedidos con mayor frecuencia se almacenan de forma local para un acceso de baja latencia, y modo almacenado (stored) en el cual sus datos son almacenados localmente en su totalidad y se mantiene una copia asíncrona en Amazon S3.

- Tape Gateway, que presenta una librería de cintas virtual en su red local y es compatible con las principales aplicaciones de respaldos disponibles en el mercado. Bajo esta modalidad, usted puede apalancar servicios de almacenamiento como Amazon S3 Deep Archive para archivar sus respaldos con un costo muy bajo por TB.

## References
- https://aws.amazon.com/es/blogs/aws-spanish/almacenamiento-hibrido-para-el-centro-de-datos-con-aws-storage-gateway/#:~:text=AWS%20Storage%20Gateway%20es%20un,manera%20transparente%20y%20sin%20contratiempos.
