# AWS QLDB

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/8e8bb98a-2dfb-4776-8653-9b26df0b230d">
</p>

Amazon Quantum Ledger Database (Amazon QLDB) is a fully managed accounting database in which a transparent, immutable, cryptographically verifiable transaction log is provided in the fully managed accounting database. Amazon QLDB can use Amazon QLDB to track all changes to your application data and maintain a complete, cryptographically verifiable change history.

Ledgers are typically used to record a history of an organization's economic and financial activity. Many organizations create applications with functionality similar to that of a general ledger because they want to maintain an accurate history of their application data. For example, they may want to track credit and debit history in banking transactions, verify the data lineage of an insurance claim, or track the movement of an item in a supply chain network. Accounting applications are typically implemented using custom audit tables or audit trails created in relational databases.

Amazon QLDB is a new kind of database that helps eliminate the need to engage in the complex development effort of creating your own ledger-like applications. With QLDB, the history of data changes is immutable: it cannot be overwritten or modified in-place. In addition, using cryptography, you can verify that no unwanted changes to the application data have occurred. QLDB uses an immutable transactional log, known as a journal. The journal is for attachments only and consists of a set of sequenced and chained blocks containing the committed data.

## References
- https://docs.aws.amazon.com/es_es/qldb/latest/developerguide/what-is.html
