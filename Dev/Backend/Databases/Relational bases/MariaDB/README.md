# MariaDB

MariaDB is a fork of MySQL. The developers built the RDBMS to retain the structure and features of MySQL. They feared that the acquisition of the system by Oracle, the corporation behind Oracle Database, which was MySQL's biggest competitor at the time, would jeopardize the database.

MariaDB developers make sure that each version is compatible with the corresponding version of MySQL. MariaDB not only adopts MySQL's data definition files and tables, but also uses identical client protocols, client APIs, ports and sockets. The goal is to allow MySQL users to switch to MariaDB seamlessly.

Like MySQL, MariaDB is modifiable via SQL statements.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/26c3ec5a-e1b0-4964-9cec-c6ca3f7e386f">
</p>

These are the advantages and disadvantages of MySQL versus MariaDB.

## Pros and cons of MariaDB

Now that you know how MariaDB differs from MySQL, let's examine the advantages and disadvantages of the two database systems.

### Pros:

First of all, MariaDB is backward compatible. This is an important feature, considering that it is an open source software constantly updated by the community.

MariaDB has a dynamic thread pool, which allows the server to optimize its resources by removing inactive threads. Combined with a large connection pool, this feature results in significantly improved speed, improved replication and faster updates.

The built-in advanced Galera clustering technology eliminates slaves lag and lost transactions, reduces client latencies, and improves node read scalability.

In addition, MariaDB supports more storage engines than MySQL, some of which are compatible with other RDBMSs. Each storage engine has a specific purpose. For example, MariaDB ColumnStore is designed for big data scaling and linear scalability.

Since MariaDB is distributed under the GPL license, you get full access to all its features after installation. In addition, the software is available free of charge.

### Cons:

MariaDB only supports JSON data types as of version 10.2. Even then, it is only an alias for LONGTEXT, introduced for compatibility reasons. To replicate JSON data when moving from MySQL to MariaDB, it is necessary to change the JSON column type first.

Some features that are only available in MySQL Enterprise Edition are absent in MariaDB. However, as part of its enterprise database solution, MariaDB offers alternative open source plugins, such as MaxScale for data masking.

That said, expert support and enterprise-level features are available by purchasing a MariaDB Platform subscription. Users of MariaDB Community, the community-developed version, must rely on the knowledge base and forums for technical assistance.

## References
- https://www.hostinger.co/tutoriales/mariadb-vs-mysql
