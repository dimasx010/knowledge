# AWS QLDB

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/8e8bb98a-2dfb-4776-8653-9b26df0b230d">
</p>

Amazon Quantum Ledger Database (Amazon QLDB) es una base de datos de contabilidad completamente administrada en la que se proporciona un registro de transacciones transparente, inmutable y que se puede verificar mediante criptografía, en la base de datos de contabilidad completamente administrada. Amazon QLDB puede usar Amazon QLDB para hacer un seguimiento de todos los cambios de los datos de la aplicación y mantener un historial de cambios completo y que se pueda verificar mediante criptografía.

Los libros de contabilidad se utilizan normalmente para registrar un historial de la actividad económica y financiera de una organización. Muchas organizaciones crean aplicaciones con una funcionalidad similar a la de un libro mayor porque desean mantener un historial preciso de los datos de sus aplicaciones. Por ejemplo, es posible que deseen rastrear el historial de créditos y débitos en las transacciones bancarias, verificar el linaje de datos de una reclamación de seguro o rastrear el movimiento de un artículo en una red de cadena de suministro. Las aplicaciones de contabilidad suelen implementarse mediante tablas de auditoría personalizadas o registros de auditoría creados en bases de datos relacionales. 

Amazon QLDB es una nueva clase de base de datos que ayuda a eliminar la necesidad de dedicarse al complejo esfuerzo de desarrollo que supone crear sus propias aplicaciones tipo libro de contabilidad. Con QLDB, el historial de cambios en los datos es inmutable: no se puede sobrescribir ni modificar in situ. Además, mediante la criptografía, puede comprobar que no se han producido cambios no deseados en los datos de la aplicación. QLDB utiliza un registro transaccional inmutable, conocido como diario. El diario es solo para anexos y se compone de un conjunto de bloques secuenciados y encadenados que contienen los datos confirmados.

## References
- https://docs.aws.amazon.com/es_es/qldb/latest/developerguide/what-is.html
