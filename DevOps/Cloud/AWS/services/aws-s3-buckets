# Buckets - Amazon S3

En Amazon S3, almacena los objetos en contenedores denominados “buckets”. No puede subir ningún objeto, ni siquiera una sola foto, a Amazon S3 sin crear primero un bucket. Al crear un bucket, especifica, como mínimo, dos detalles: la región de AWS en la que desea que se ubique el bucket y el nombre del bucket.

Para elegir una región, por lo general seleccionará una región que haya utilizado para otros recursos, como el cómputo. Cuando elige una región para el bucket, todos los objetos que coloque en el bucket se almacenarán de forma redundante en varios dispositivos, en varias zonas de disponibilidad. Este nivel de redundancia está diseñado para proporcionar a los clientes de Amazon S3 una durabilidad del 99,999999999 % y una disponibilidad del 99,99 % para los objetos durante un año determinado.

Cuando elige un nombre de bucket, debe ser único en todas las cuentas de AWS. AWS le impide elegir un nombre de bucket ya elegido por otra persona en otra cuenta de AWS. Una vez que elija un nombre, ese nombre es suyo, y ninguna otra persona puede reclamarlo a menos que elimine el bucket, con lo que luego se libera el nombre para que lo utilicen otras personas.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/d045922e-5251-4f9b-8074-4687c734695c">
</p>

AWS utiliza el nombre de bucket como parte del identificador de objeto. En S3, cada objeto se identifica mediante una URL como se muestra.

Después de http://, puede ver el nombre de bucket. En este ejemplo, el bucket se denomina doc. A continuación, el identificador utiliza el proveedor de servicios y el nombre del servicio s3, amazonaws. Después de eso, habrá una carpeta implícita dentro del bucket llamada 2006-03-01 y el objeto dentro de la carpeta que se denomina AmazonS3.html. El nombre del objeto se conoce a menudo como “nombre de clave”.

Puede haber carpetas dentro de los buckets para ayudarlo a organizar los objetos. Sin embargo, recuerde que ninguna jerarquía de archivos real lo admite en el backend. En cambio, es una estructura plana en la que todos los archivos y las carpetas se encuentran en el mismo nivel. El uso de buckets y carpetas implica una jerarquía, que crea una organización comprensible para los usuarios.

## Políticas de bucket de S3

Al igual que las políticas de IAM, las políticas de bucket S3 de Amazon se definen en formato JSON. La diferencia es que las políticas de IAM se adjuntan a los usuarios, los grupos y los roles, mientras que las políticas de bucket de S3 solo se adjuntan a los buckets de S3. Las políticas de bucket de S3 especifican qué acciones se permiten o deniegan en el bucket.

Por ejemplo, si tiene un bucket llamado “employeebucket”, puede adjuntarle una política de bucket de S3 que permita a otra cuenta de AWS colocar objetos en ese bucket.

Alternativamente, si quiere permitir que los lectores anónimos lean los objetos de employeebucket, puede aplicar una política a ese bucket que permita a cualquier persona leer los objetos del bucket por medio de "Effect":Allow on the "Action:["s3:GetObject"]".

Este es un ejemplo de cómo se vería la política de bucket de S3.

```json
{
"Version":"2012-10-17",
"Statement":[{
"Sid":"PublicRead",
"Effect":"Allow",
"Principal": "*",
"Action":["s3:GetObject"],
"Resource":["arn:aws:s3:::employeebucket/*"]
}]
}
```
Las políticas de bucket de S3 solo se pueden colocar en buckets y no se pueden utilizar para carpetas u objetos. Sin embargo, la política que se coloca en el bucket se aplica a todos los objetos de ese bucket.

Debe utilizar las políticas de bucket de S3 en las siguientes situaciones:

Necesita una forma sencilla de acceder a S3 entre cuentas, sin utilizar roles de IAM.

Sus políticas de IAM se topan con el límite de tamaño definido. Las políticas de bucket de S3 tienen un límite de tamaño mayor.

