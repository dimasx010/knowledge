# MariaDB vs Mysql

Un sistema de gestión de base de datos relacional (RDBMS) es la versión mejorada de un sistema de gestión de bases de datos (SGBD) o database management system (DBMS). Utiliza un módulo de software conocido como motor de almacenamiento para almacenar, gestionar y modificar los datos.

A diferencia de un SGBD que almacena los datos en forma de archivo, un RDBMS gestiona los datos en formato tabular. El uso de tablas de base de datos elimina la redundancia de datos que experimenta el SGBD debido a su uso de claves e índices.

MySQL y MariaDB pertenecen a la categoría RDBMS. Las siguientes secciones explorarán más a fondo ambos sistemas de gestión de bases de datos relacionales populares y cómo se diferencian entre sí.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/4085b827-53f6-4c82-b698-f77f485ed5e2">
</p>

## Las diferencias entre MariaDB vs MySQL 

A pesar de tener una estructura y funcionalidad similares, hay varias diferencias clave entre MySQL y MariaDB.

MariaDB sigue siendo completamente de código abierto (open-source), mientras que MySQL tiene ahora módulos de código cerrado. En general, MariaDB ofrece un mejor rendimiento, es más rápido y más ligero que MySQL gracias a sus 12 nuevos motores de almacenamiento y a sus más de 200.000 conexiones.

Desde su adquisición por parte de Oracle, MySQL se distribuye bajo licencia dual. La empresa vende licencias a las personas que quieren utilizarlo, pero no quieren que su producto sea de código abierto. Por su parte, MariaDB se publica bajo la licencia pública general GNU (GPL).

MySQL ofrece la capacidad de agrupación de hilos en la Enterprise Edition para soportar hasta 200.000 conexiones, con una mejor estabilidad y rendimiento del sistema. Desafortunadamente, el mismo soporte no está disponible en la Community Edition de MySQL, ya que sólo soporta un número estático limitado de hilos.

Por otro lado, MariaDB ha mejorado esta función en todas las versiones: es capaz de soportar más de 200.000 conexiones. Esto es vital para las plataformas de comercio electrónico, donde es habitual el procesamiento intensivo de transacciones en línea (OLTP). Una alta capacidad de pool de hilos ayuda a optimizar el uso de los recursos del servidor, lo que se traduce en un mayor tiempo de actividad.

En cuanto a las funcionalidades, MySQL ha introducido los objetos sys schema para un mejor mantenimiento de la base de datos y un mejor ajuste del rendimiento, así como la función de superlectura, utilizada para evitar los cambios realizados en el servidor por los Super usuarios.

También soporta el enmascaramiento de datos y las columnas dinámicas. El enmascaramiento de datos protege la información sensible de una exposición involuntaria, minimizando el riesgo de violación de datos. Por su parte, las columnas dinámicas permiten definir múltiples valores en una columna y modificarlos con funciones, una característica de la que carecen las columnas estáticas.

En cambio, MariaDB soporta nuevas características como las columnas invisibles y las vistas de la base de datos. Las columnas invisibles no aparecen cuando la base de datos ejecuta una instrucción SELECT o requiere un valor en una instrucción INSERT. Las vistas de la base de datos simplifican el almacenamiento y la compartición de las consultas entre las aplicaciones.

Cuando se trata de motores de bases de datos, MariaDB ofrece más opciones que MySQL. Algunos de los motores de almacenamiento que MariaDB utiliza y MySQL no son: XtraDB, Memory Storage Engine, MariaDB ColumnsStore, Aria, Cassandra Storage Engine y Connect.

Mientras tanto, MySQL soporta un tipo de datos JSON nativo y proporciona el plugin de autenticación SHA-2 y el plugin validate_password por defecto, mientras que MariaDB no lo hace.

La última diferencia clave entre MariaDB y MySQL radica en la gestión de la organización. Como MySQL está gestionado por Oracle Corporation, la empresa gobierna el proceso de desarrollo y documentación. La comunidad no tiene voz en las decisiones de desarrollo.

Como MariaDB es un software impulsado por la comunidad, está gestionado por la MariaDB Foundation. La licencia GNU GPL permite a las comunidades de código abierto participar en el proceso de desarrollo y documentación y revisar cualquier decisión de desarrollo a través de la lista de correo pública de la fundación.

## MariaDB vs MySQL: Una comparación exhaustiva

En las siguientes secciones, compararemos el rendimiento de MySQL y MariaDB y discutiremos su intercompatibilidad.

### Rendimiento y puntos de referencia

Teniendo en cuenta la similitud de funcionamiento entre MariaDB y MySQL, se realizaron varias pruebas de rendimiento y de referencia para determinar cuál es superior.

Una prueba de rendimiento e impacto de UTF8 realizada por Dimitri Kravtchuk reveló que MySQL 8.0 puede manejar un mayor número de consultas por segundo que MariaDB 10.3.

Del mismo modo, según la prueba de rendimiento y referencia de Minerva DB de InnoDB (que se ejecuta en la versión 8.0 de MySQL) y MyRocks (que se ejecuta en la versión 10.3.7 de MariaDB), InnoDB puede atender más consultas por segundo que MyRocks.

En términos de hardware básico, Axel Schwenke descubrió que MariaDB 10.1 rinde más que MySQL 5.7.9.

Dicho esto, hay que tener en cuenta que el rendimiento y los resultados de las pruebas comparativas dependen de varios factores, como las consultas SQL específicas, el número de usuarios y conexiones, y los casos de uso.

### Compatibilidad

Dado que MariaDB se ha desarrollado como el sustituto binario completo de MySQL, es compatible con su predecesor en varios aspectos.

Por ejemplo, MariaDB ha mantenido las convenciones de nomenclatura, la estructura y los archivos de definición de datos de MySQL. Además, soporta todas las conexiones, conectores y puertos de MySQL. El paquete cliente de MySQL funciona sin cambios con MariaDB.

El cambio de MySQL a MariaDB sigue un procedimiento de instalación estándar. Sólo tienes que ejecutar la herramienta mysql_upgrade para actualizar los privilegios de la base de datos MySQL y las tablas de eventos con los equivalentes de MariaDB.


## ¿Quién utiliza MariaDB vs MySQL?

Como dos de los sistemas de bases de datos relacionales más populares hoy en día, tanto MySQL como MariaDB cuentan con un gran número de seguidores en el mercado internacional.

Algunas de las grandes empresas que utilizan MySQL son YouTube, GitHub, Spotify, Netflix y la NASA. MySQL también está asociada con empresas tecnológicas como Hewlett Packard Enterprise, Amazon Web Services, IBM, Microsoft y Zapier.

Por su parte, Wikipedia, Google, CentOS y Verizon son algunos de los clientes de MariaDB. Entre sus socios se encuentran soluciones informáticas de renombre como Google Cloud, Red Hat, Qualcomm y SanDisk.

Tanto MariaDB como MySQL ofrecen características y capacidades convincentes. Lo único que queda por hacer es determinar cuál se adapta mejor a tus necesidades.

Respaldado por Oracle Corporation, MySQL es una opción ideal para los clientes que buscan mejoras constantes, actualizaciones consistentes y un soporte de nivel empresarial 24/7. A pesar de su coste de 5.000 dólares al año, MySQL Enterprise Edition cuenta con los más altos niveles de escalabilidad, fiabilidad y seguridad.

Dicho esto, la Community Edition de MySQL es lo suficientemente versátil como para acomodar todo tipo de proyectos construidos en plataformas y sistemas operativos populares. Muchos desarrolladores de código abierto utilizan MySQL ya que está considerado como uno de los mejores sistemas de bases de datos del mercado.

## References
- https://www.hostinger.co/tutoriales/mariadb-vs-mysql
