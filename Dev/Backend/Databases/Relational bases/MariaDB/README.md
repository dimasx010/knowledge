# MariaDB

MariaDB es un fork de MySQL. Los desarrolladores construyeron el RDBMS para conservar la estructura y las características de MySQL. Temían que la adquisición del sistema por parte de Oracle, la corporación detrás de la base de datos Oracle, que era el mayor competidor de MySQL en ese momento, pusiera en peligro la base de datos.

Los desarrolladores de MariaDB se aseguran de que cada versión sea compatible con la versión correspondiente de MySQL. MariaDB no sólo adopta los archivos de definición de datos y tablas de MySQL, sino que también utiliza protocolos de cliente, API de cliente, puertos y sockets idénticos. El objetivo es que los usuarios de MySQL puedan cambiar a MariaDB sin problemas.

Al igual que MySQL, MariaDB es modificable mediante instrucciones SQL.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/26c3ec5a-e1b0-4964-9cec-c6ca3f7e386f">
</p>

Estas son las ventajas y desventajas de MySQL frente a MariaDB.

## Pros y contras de MariaDB

Ahora que sabes en qué se diferencia MariaDB de MySQL, vamos a examinar las ventajas y desventajas de los dos sistemas de bases de datos.

### Pros:

En primer lugar, MariaDB es compatible con versiones anteriores. Esta es una característica importante, teniendo en cuenta que es un software de código abierto constantemente actualizado por la comunidad.

MariaDB cuenta con un thread pool dinámico, que permite al servidor optimizar sus recursos retirando los hilos inactivos. Combinado con un gran pool de conexiones, esta característica da como resultado una velocidad considerablemente mejorada, una replicación mejorada y actualizaciones más rápidas.

La tecnología avanzada de cluster Galera incorporada elimina el retraso de los slaves y las transacciones perdidas, reduce las latencias de los clientes y mejora la escalabilidad de lectura de los nodos.

Además, MariaDB soporta más motores de almacenamiento que MySQL, algunos de los cuales son compatibles con otros RDBMS. Cada motor de almacenamiento tiene un propósito específico. Por ejemplo, MariaDB ColumnStore está diseñado para el escalado de big data y la escalabilidad lineal.

Dado que MariaDB se distribuye bajo la licencia GPL, se obtiene acceso completo a todas sus características tras la instalación. Además, el software está disponible de forma gratuita.

### Contras:

MariaDB sólo soporta tipos de datos JSON a partir de la versión 10.2. Incluso entonces, es sólo un alias para LONGTEXT, presentado por razones de compatibilidad. Para replicar los datos JSON al pasar de MySQL a MariaDB, es necesario cambiar primero el tipo de columna JSON.

Algunas características que sólo están disponibles en la Enterprise Edition de MySQL están ausentes en MariaDB. Sin embargo, como parte de su solución de base de datos para empresas, MariaDB ofrece plugins alternativos de código abierto, como MaxScale para el enmascaramiento de datos.

Eso sí, se puede acceder a un soporte experto y a funciones de nivel empresarial si se adquiere una suscripción a MariaDB Platform. Los usuarios de MariaDB Community, la versión desarrollada por la comunidad, deben recurrir a la base de conocimientos y a los foros para obtener asistencia técnica.

## References
- https://www.hostinger.co/tutoriales/mariadb-vs-mysql
