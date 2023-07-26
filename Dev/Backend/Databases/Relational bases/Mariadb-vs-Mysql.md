# MariaDB vs Mysql

A relational database management system (RDBMS) is the enhanced version of a database management system (DBMS). It uses a software module known as a storage engine to store, manage and modify data.

Unlike a DBMS that stores data in file form, an RDBMS manages data in tabular format. The use of database tables eliminates the data redundancy experienced by the DBMS due to its use of keys and indexes.

MySQL and MariaDB belong to the RDBMS category. The following sections will further explore both of these popular relational database management systems and how they differ from each other.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/4085b827-53f6-4c82-b698-f77f485ed5e2">
</p>

## The differences between MariaDB vs MySQL

Despite having a similar structure and functionality, there are several key differences between MySQL and MariaDB.

MariaDB is still completely open-source, while MySQL now has closed-source modules. In general, MariaDB offers better performance, is faster and lighter than MySQL thanks to its 12 new storage engines and more than 200,000 connections.

Since its acquisition by Oracle, MySQL has been distributed under a dual license. The company sells licenses to people who want to use it, but do not want its product to be open source. MariaDB is released under the GNU General Public License (GPL).

MySQL offers thread pooling capability in the Enterprise Edition to support up to 200,000 connections, with improved system stability and performance. Unfortunately, the same support is not available in MySQL Community Edition, as it only supports a limited static number of threads.

On the other hand, MariaDB has improved this feature in all versions: it is able to support more than 200,000 connections. This is vital for e-commerce platforms, where intensive online transaction processing (OLTP) is common. A high thread pooling capacity helps to optimize the use of server resources, which translates into increased uptime.

In terms of functionality, MySQL has introduced sys schema objects for better database maintenance and performance tuning, as well as the super read feature, used to prevent changes made to the server by Super users.

It also supports data masking and dynamic columns. Data masking protects sensitive information from unintentional exposure, minimizing the risk of data breaches. Dynamic columns allow multiple values to be defined in a column and modified with functions, a feature that static columns lack.

In contrast, MariaDB supports new features such as invisible columns and database views. Invisible columns do not appear when the database executes a SELECT statement or requires a value in an INSERT statement. Database views simplify the storage and sharing of queries between applications.

When it comes to database engines, MariaDB offers more options than MySQL. Some of the storage engines that MariaDB uses and MySQL does not are: XtraDB, Memory Storage Engine, MariaDB ColumnsStore, Aria, Cassandra Storage Engine and Connect.

Meanwhile, MySQL supports a native JSON data type and provides the SHA-2 authentication plugin and the validate_password plugin by default, while MariaDB does not.

The last key difference between MariaDB and MySQL lies in the organization management. Since MySQL is managed by Oracle Corporation, the company governs the development and documentation process. The community has no say in development decisions.

Since MariaDB is community-driven software, it is managed by the MariaDB Foundation. The GNU GPL license allows the open source communities to participate in the development and documentation process and to review any development decisions through the foundation's public mailing list.

## MariaDB vs MySQL: A Comprehensive Comparison

In the following sections, we will compare the performance of MySQL and MariaDB and discuss their intercompatibility.

### Performance and benchmarks

Given the similarity in performance between MariaDB and MySQL, several performance and benchmark tests were conducted to determine which is superior.

A UTF8 performance and impact test by Dimitri Kravtchuk revealed that MySQL 8.0 can handle a higher number of queries per second than MariaDB 10.3.

Similarly, according to Minerva DB's performance and benchmark test of InnoDB (running on MySQL version 8.0) and MyRocks (running on MariaDB version 10.3.7), InnoDB can handle more queries per second than MyRocks.

In terms of basic hardware, Axel Schwenke found that MariaDB 10.1 performs better than MySQL 5.7.9.

That said, it should be noted that performance and benchmark results depend on several factors, such as specific SQL queries, number of users and connections, and use cases.

### Compatibility

Since MariaDB has been developed as the full binary replacement for MySQL, it is compatible with its predecessor in several respects.

For example, MariaDB has retained the naming conventions, structure and data definition files of MySQL. In addition, it supports all MySQL connections, connectors and ports. The MySQL client package works unchanged with MariaDB.

Switching from MySQL to MariaDB follows a standard installation procedure. Just run the mysql_upgrade tool to update the MySQL database privileges and event tables to MariaDB equivalents.


## Who uses MariaDB vs MySQL?

As two of the most popular relational database systems today, both MySQL and MariaDB have a large following in the international market.

Some of the large companies that use MySQL include YouTube, GitHub, Spotify, Netflix and NASA. MySQL is also associated with technology companies such as Hewlett Packard Enterprise, Amazon Web Services, IBM, Microsoft and Zapier.

Wikipedia, Google, CentOS and Verizon are among MariaDB's customers. Among its partners are renowned IT solutions such as Google Cloud, Red Hat, Qualcomm and SanDisk.

Both MariaDB and MySQL offer compelling features and capabilities. The only thing left to do is determine which one best suits your needs.

Backed by Oracle Corporation, MySQL is an ideal choice for customers looking for constant enhancements, consistent upgrades and 24/7 enterprise-level support. Despite its cost of $5,000 per year, MySQL Enterprise Edition boasts the highest levels of scalability, reliability and security.

That said, MySQL Community Edition is versatile enough to accommodate all types of projects built on popular platforms and operating systems. Many open source developers use MySQL as it is considered one of the best database systems on the market.

## References
- https://www.hostinger.co/tutoriales/mariadb-vs-mysql
