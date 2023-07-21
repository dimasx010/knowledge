# Amazon S3 - Amazon Simple Storage Service

Amazon Simple Storage Service (Amazon S3) es un servicio de almacenamiento de objetos que ofrece escalabilidad, disponibilidad de datos, seguridad y rendimiento líderes del sector. Los clientes de todos los tamaños y sectores pueden utilizar Amazon S3 para almacenar y proteger cualquier cantidad de datos para diversos casos de uso, tales como lagos de datos, sitios web, aplicaciones móviles, copia de seguridad y restauración, archivado, aplicaciones empresariales, dispositivos IoT y análisis de big data. Amazon S3 proporciona funciones de gestión para que pueda optimizar, organizar y configurar el acceso a sus datos para satisfacer sus requisitos empresariales, organizativos y de conformidad específicos.

Amazon S3 ofrece varios tipos de almacenamiento diseñados para distintos casos de uso. Por ejemplo, puede almacenar datos de producción críticos en S3 Standard para obtener acceso frecuente, ahorrar costos al almacenar datos a los que se accede con poca frecuencia en S3 Standard-IA o S3 One Zone-IA, y archivar datos con los costos más bajos en S3 Glacier Instant Retrieval, S3 Glacier Flexible Retrieval y S3 Glacier Deep Archive.

Puede almacenar datos con patrones de acceso cambiantes o desconocidos en S3 Intelligent-Tiering, que optimiza los costos de almacenamiento moviendo automáticamente los datos entre cuatro niveles de acceso cuando cambian los patrones de acceso. Funciona con el almacenamiento de objetos en cuatro capas de acceso: dos de acceso de baja latencia optimizadas para el acceso frecuente y poco frecuente y dos de acceso a archivos opcionales diseñados para el acceso asíncrono, las cuales están optimizadas para accesos inusuales.

Para obtener más información, consulte Uso de las clases de almacenamiento de Amazon S3. Para obtener más información sobre S3 Glacier Flexible Retrieval, consulte la Guía para desarrolladores de Amazon S3 Glacier.

## Administrar el almacenamiento

Amazon S3 cuenta con funciones de gestión del almacenamiento que puede utilizar para gestionar los costes, cumplir los requisitos normativos, reducir la latencia y guardar varias copias distintas de sus datos para cumplir los requisitos de cumplimiento.

- Ciclo de vida de S3: defina la configuración de ciclo de vida para administrar los objetos y almacenarlos de manera económica durante todo su ciclo de vida. Puede realizar la transición de objetos a otras clases de almacenamiento de S3 o caducar objetos que alcancen el final de su vida útil.

- S3 Object Lock: evite que se eliminen o se sobreescriban objetos de Amazon S3 durante un período de tiempo determinado o de manera indefinida. Object Lock se puede utilizar para cumplir con los requisitos normativos que requieren almacenamiento de escritura única y lectura múltiple (WORM) o simplemente para agregar otra capa de protección para evitar cambios y eliminaciones de objetos.

Replicación de S3— Replique objetos y sus respectivos metadatos y etiquetas de objeto en uno o más buckets de destino en el mismo o en diferentesRegiones de AWSpara reducir la latencia, el cumplimiento normativo, la seguridad y otros casos de uso.

Operaciones por lotes de S3: gestione miles de millones de objetos a escala con una sola solicitud de API de S3 o con unos pocos clics en la consola de Amazon S3. Puede utilizar Operaciones Batch para realizar operaciones comoCopy (Copiar),InvocaciónAWSFunción de Lambda, yRestauraren millones o miles de millones de objetos.

## El modelo de funcionamiento sería el siguiente: 

Amazon S3 es un servicio de almacenamiento de objetos que almacena datos como objetos dentro de buckets. Un objeto es un archivo y cualquier metadato que describa ese archivo. Un bucket es un contenedor de objetos.

Para almacenar datos en Amazon S3, primero debe crear un bucket y especificar un nombre de bucket yRegión de AWS. A continuación, cargue datos a ese bucket como objetos en Amazon S3. Cada objeto tiene unclave(oNombre de clave), que es el identificador único del objeto dentro del bucket.

S3 proporciona funciones que puede configurar para admitir su caso de uso específico. Puede utilizar S3 Versioning para mantener varias versiones de un objeto en un bucket y restaurar objetos que se eliminan o sobrescribir accidentalmente.

Los buckets y los objetos que contienen son privados y solo se puede acceder a ellos si se conceden explícitamente permisos de acceso. Puede utilizar políticas de bucket,AWS Identity and Access Management(IAM), listas de control de acceso (ACL) y puntos de acceso S3 para administrar el acceso.

## Casos de uso de Amazon S3

Amazon S3 es un servicio de almacenamiento ampliamente utilizado, con muchos más casos de uso de los que caben en una pantalla. En la siguiente lista, se resumen algunas de las formas más comunes de utilizar Amazon S3:

- Copia de seguridad y almacenamiento: Amazon S3 es un lugar natural para realizar copia de seguridad de los archivos porque es altamente redundante. Como se mencionó en la última unidad, AWS almacena las instantáneas de EBS en S3 para aprovechar la alta disponibilidad.

- Alojamiento multimedia: Debido a que puede almacenar objetos ilimitados y a que cada objeto individual puede tener hasta 5 TB, Amazon S3 es un lugar ideal para alojar cargas de video, fotos y música.

- Entrega de software: Puede utilizar Amazon S3 para alojar las aplicaciones de software que los clientes pueden descargar.

- Lagos de datos: AmazonS3 es la base óptima para un lago de datos por su escalabilidad prácticamente ilimitada. Puede aumentar el almacenamiento de gigabytes a petabytes de contenido y pagar solo por lo que utiliza.
Sitios web estáticos: Puede configurar su bucket de S3 para alojar un sitio web estático de scripts HTML, CSS y del lado del cliente.

Contenido estático: Debido al escalado ilimitado, a la compatibilidad con archivos grandes y al hecho de que puede acceder a cualquier objeto a través de la Web en cualquier momento, Amazon S3 es el lugar perfecto para almacenar contenido estático.

## Elección de la opción de conectividad adecuada para los recursos

Todo lo que se encuentra en Amazon S3 es privado de forma predeterminada. Significa que a solo el usuario o la cuenta de AWS que creó el recurso puede ver todos los recursos de S3, como los buckets, las carpetas y los objetos. Los recursos de Amazon S3 son privados y están protegidos para empezar.

Si decide que quiere que todos los usuarios en Internet vean sus fotos, puede elegir hacer públicos los buckets, las carpetas y los objetos. Un recurso público significa que todos los usuarios en Internet pueden verlo. La mayoría de las veces, no quiere que los permisos sean todo o nada. Normalmente, desea adoptar un enfoque más pormenorizado de la forma en que proporciona acceso a los recursos.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/d38dd44c-3020-4f0b-9bc3-657a006ac0e5">
</p>

## Cifrado de Amazon S3

Amazon S3 refuerza el cifrado en tránsito (a medida que viaja hacia Amazon S3 y desde allí) y en reposo. Para proteger los datos en reposo, puede utilizar el cifrado de la siguiente manera:

- Cifrado del lado del servidor: Permite a Amazon S3 cifrar el objeto antes de guardarlo en los discos de sus centros de datos y, a continuación, descifrarlo al descargar los objetos.

- Cifrado del lado del cliente: Puede cifrar los datos del lado del cliente y, a continuación, subir los datos cifrados a Amazon S3. En este caso, administra el proceso de cifrado, las claves de cifrado y todas las herramientas relacionadas.

Para el cifrado en tránsito, puede utilizar el cifrado del lado del cliente o la Capa de conexión segura (SSL).

## Control de versiones de Amazon S3

Como se describió anteriormente, Amazon S3 identifica los objetos en parte mediante el nombre del objeto. Por ejemplo, cuando sube una foto de un empleado a Amazon S3, podría nombrar el objeto “employee.jpg” y almacenarlo en una carpeta denominada “employees”. Si no utiliza el control de versiones de Amazon S3, cada vez que sube un objeto llamado “employee.jpg” a la carpeta employees, sobrescribirá el archivo original.

Esto puede ser un problema por varios motivos, como los siguientes:

- El nombre del archivo employee.jpg es un nombre común para un objeto de fotos de empleados. Es posible que usted u otra persona que tenga acceso al bucket no haya tenido la intención de sobrescribirlo, pero una vez sobrescrito, no se puede acceder al archivo original.

Es posible que desee conservar diferentes versiones de employee.jpg. Sin el control de versiones, si quisiera crear una nueva versión de employee.jpg, tendría que subir el objeto y elegir otro nombre para él. Tener varios objetos con ligeras diferencias en las variaciones de nomenclatura puede causar confusión y desorden en los buckets de S3.

Para contrarrestar estos problemas, puede utilizar el control de versiones de S3. El control de versiones conserva varias versiones de un único objeto en el mismo bucket. De este modo, se conservan las versiones anteriores de un objeto sin utilizar nombres diferentes, lo que ayuda a recuperar los archivos de eliminaciones accidentales, sobrescrituras accidentales o errores de aplicaciones.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/48bf65b3-3935-47f6-bae4-ec4a388899a2">
</p>

Si habilita el control de versiones para un bucket, Amazon S3 genera automáticamente un ID de versión único para el objeto. En un bucket, por ejemplo, puede tener dos objetos con la misma clave, pero ID de versión diferentes, como employeephoto.gif (versión 111111) y employeephoto.gif (versión 121212).

Los buckets habilitados para el control de versiones le permiten recuperar los objetos de la eliminación o la sobrescritura accidentales.

La eliminación de un objeto no elimina el objeto de forma permanente. En cambio, Amazon S3 coloca un marcador en el objeto que muestra que trató de eliminarlo. Si quiere restaurar el objeto, puede quitar el marcador, y se restablece el objeto.

Si sobrescribe un objeto, da como resultado una nueva versión del objeto en el bucket. Sigue teniendo acceso a las versiones anteriores del objeto.

## Estados del control de versiones

Los buckets pueden presentar uno de los tres estados siguientes:

- Sin versión (predeterminado): Ningún objeto nuevo ni actual en el bucket tiene una versión.

- Control de versiones habilitado: El control de versiones está habilitado para todos los objetos del bucket.

- Control de versiones suspendido: Se suspende el control de versiones para los objetos nuevos. Ninguno de los objetos nuevos del bucket tendrá una versión. Sin embargo, todos los objetos actuales conservan las versiones de objetos.

El estado de control de versiones se aplica a todos los objetos del bucket. Los costos de almacenamiento se generan en todos los objetos del bucket, incluidas todas las versiones. Para reducir el monto de la factura de Amazon S3, es posible que quiera eliminar las versiones anteriores de los objetos cuando ya no sean necesarios.

## Automatización de las transiciones de niveles con la administración del ciclo de vida de los objetos

Si sigue cambiando manualmente los objetos, como las fotos de los empleados, de una capa de almacenamiento a otro, quizá busque automatizar el proceso con una política de ciclo de vida. Al definir una configuración de política de ciclo de vida para un objeto o un grupo de objetos, puede elegir automatizar dos acciones: acciones de transición y de vencimiento.

Las acciones de transición definen cuándo los objetos deben pasar a otra clase de almacenamiento.

Las acciones de vencimiento definen cuándo vencen los objetos y cuándo deben eliminarse de forma permanente.

Por ejemplo, puede hacer una transición de los objetos a la clase de almacenamiento Estándar - Acceso poco frecuente de S3 30 días después de crearlos o archivar los objetos en la clase de almacenamiento de S3 Glacier 1 año después de crearlos.

Los siguientes casos de uso son buenas opciones para la administración del ciclo de vida:

- Registros periódicos: Si sube los registros periódicos a un bucket, es posible que la aplicación los necesite durante 1 semana o 1 mes. Después de ese periodo, quizá quiera eliminarlos.

- Datos con cambios en la frecuencia de acceso: A algunos documentos se accede con frecuencia durante un periodo limitado. Posteriormente, se obtendrá acceso a ellos con poca frecuencia. En algún momento, es posible que no necesite acceso en tiempo real a estos datos, pero la organización o las normativas pueden requerir el archivado durante un periodo específico. Transcurrido dicho periodo, podrá eliminarlos.