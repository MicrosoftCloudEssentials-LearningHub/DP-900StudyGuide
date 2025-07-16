# Relational Data on Azure: Sample Questions and Answers 

Costa Rica

[![GitHub](https://img.shields.io/badge/--181717?logo=github&logoColor=ffffff)](https://github.com/)
[brown9804](https://github.com/brown9804)

Last updated: 2025-01-16

----------

> [!NOTE]
> The questions and answers provided in this study guide are for practice purposes only and are not official practice questions.
> They are intended to help you prepare for the [DP-900 Microsoft certification exam](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/dp-900).
> For additional preparation materials and the most up-to-date information, please refer to the [official Microsoft documentation](https://learn.microsoft.com/en-us/credentials/certifications/azure-data-fundamentals/?practice-assessment-type=certification).

- Identify considerations for relational data on Azure

<details>
<summary><b>List of References </b> (Click to expand)</summary>

- [Describe concepts of relational data](https://learn.microsoft.com/en-us/training/modules/describe-concepts-of-relational-data/)
- [Microsoft Azure Data Fundamentals: Explore relational data in Azure](https://learn.microsoft.com/en-us/training/paths/azure-data-fundamentals-explore-relational-data/)
- [Explore fundamental relational data concepts](https://learn.microsoft.com/en-us/training/modules/explore-relational-data-offerings/)

</details>

<details>
<summary><b>List of questions/answers </b> (Click to expand)</summary>

- [Q1: Understanding Batch Processing Outputs](#q1-understanding-batch-processing-outputs)
- [Q2: Understanding SQL Query Types](#q2-understanding-sql-query-types)
- [Q3: Understanding Database Schemas](#q3-understanding-database-schemas)
- [Q4: Understanding Database Indexes](#q4-understanding-database-indexes)
- [Q5: Understanding SQL Server Features](#q5-understanding-sql-server-features)
- [Q6: Understanding Database Relationships](#q6-understanding-database-relationships)
- [Q7: Understanding Stored Procedures](#q7-understanding-stored-procedures)
- [Q8: Understanding Data Manipulation Language DML](#q8-understanding-data-manipulation-language-dml)
- [Q9: Understanding Data Definition Language DDL](#q9-understanding-data-definition-language-ddl)
- [Q10: Understanding Data Control Language DCL](#q10-understanding-data-control-language-dcl)
- [Q11: Understanding Database Types](#q11-understanding-database-types)
- [Q12: Understanding Transaction Control Language TCL](#q12-understanding-transaction-control-language-tcl)
- [Q13: Understanding Data Query Language DQL](#q13-understanding-data-query-language-dql)
- [Q14: Understanding Database Concepts](#q14-understanding-database-concepts)
- [Q15: Understanding Database Types](#q15-understanding-database-types)
- [Q16: Understanding Database Concepts](#q16-understanding-database-concepts)
- [Q17: Understanding Database Concepts](#q17-understanding-database-concepts)
- [Q18: Understanding Database Concepts](#q18-understanding-database-concepts)
- [Q19: Understanding Database Types](#q19-understanding-database-types)
- [Q20: Understanding Aggregate Functions](#q20-understanding-aggregate-functions)
- [Q21: Understanding Scalar Functions](#q21-understanding-scalar-functions)
- [Q22: Understanding Date Functions](#q22-understanding-date-functions)
- [Q23: Understanding Database Normalization](#q23-understanding-database-normalization)

</details>

> [!TIP]
> Types of functions in SQL:

| Type of Function       | Description                                                                 | Examples                          |
|------------------------|-----------------------------------------------------------------------------|-----------------------------------|
| Aggregate Functions    | Perform a calculation on a set of values and return a single value.         | `MAX`, `MIN`, `SUM`, `AVG`, `COUNT` |
| Scalar Functions       | Return a single value based on the input value.                             | `UPPER`, `LOWER`, `ROUND`, `LEN`  |
| String Functions       | Perform operations on string values and return a string or numeric value.   | `CONCAT`, `SUBSTRING`, `REPLACE`, `TRIM` |
| Date Functions         | Perform operations on date and time values and return a date, time, or numeric value. | `GETDATE`, `DATEADD`, `DATEDIFF`, `FORMAT` |
| Numeric Functions      | Perform operations on numeric values and return a numeric value.            | `ABS`, `CEILING`, `FLOOR`, `POWER` |
| Conversion Functions   | Convert a value from one data type to another.                              | `CAST`, `CONVERT`, `PARSE`        |
| Window Functions       | Perform calculations across a set of table rows that are related to the current row. | `ROW_NUMBER`, `RANK`, `DENSE_RANK`, `NTILE` |
| JSON Functions         | Perform operations on JSON data and return JSON or scalar values.           | `JSON_VALUE`, `JSON_QUERY`, `JSON_MODIFY` |

> [!TIP]
> Database management systems (DBMS) concepts:

| Concept            | Explanation                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| Clustered Index    | A type of database index that sorts and stores the data rows in the table based on their key values. The table is physically ordered according to this index. |
| FileTable          | A feature in SQL Server that allows storing files and documents in special tables where each row represents a file or directory, integrating with the Windows file system. |
| Foreign Key        | A field (or collection of fields) in one table that uniquely identifies a row of another table, creating a relationship between the two tables. It ensures referential integrity within the database. |
| Stored Procedure   | A precompiled collection of one or more SQL statements stored under a name and processed as a unit, which can be executed with parameters to perform specific tasks within the database. |

> [!TIP]
> ACID properties:

| Term        | Description                                                                 |
|-------------|-----------------------------------------------------------------------------|
| Atomicity   | Ensures that all operations within a` transaction are completed successfully`; if not, the transaction is aborted. |
| Isolation   | Ensures that transactions are executed in isolation from one another, `preventing concurrent transactions from interfering with each other`. |
| Durability  | Ensures that `once a transaction is committed, it remains permanent`, even in the event of a system failure. |
| Consistency | Ensures that a transaction brings the `database from one valid state to another`, maintaining database integrity. |

> [!TIP]
> SQL Language types:

| SQL Language Type            | Description                                                                 | Examples                          |
|------------------------------|-----------------------------------------------------------------------------|-----------------------------------|
| Data Definition Language (DDL) | Defines and manages database structures.                                    | `CREATE`, `ALTER`, `DROP`, `TRUNCATE` |
| Data Manipulation Language (DML) | Manipulates data within existing database structures.                      | `INSERT`, `UPDATE`, `DELETE`, `MERGE` |
| Data Control Language (DCL)    | Controls access to data within the database.                                | `GRANT`, `REVOKE`                 |
| Transaction Control Language (TCL) | Manages transactions to ensure data integrity.                            | `COMMIT`, `ROLLBACK`, `SAVEPOINT` |
| Data Query Language (DQL)      | Queries and retrieves data from the database.                               | `SELECT`                          |

## Q1: Understanding Batch Processing Outputs

> For each of the following statements about batch processing, select Yes if the statement is true. Otherwise, select No.

1. Batch processing can output data to a file store.
   - [ ] No ❌: `This is incorrect because batch processing can indeed output data to a file store. File stores are commonly used for storing large volumes of processed data in a structured or unstructured format.`
   - [ ] Yes ✅: `This is correct because batch processing can output data to various storage systems, including file stores. For example, processed data can be written to CSV files, log files, or other file formats stored in a file system or cloud storage service.`
2. Batch processing can output data to a NoSQL database.
   - [ ] No ❌: `This is incorrect because batch processing can indeed output data to a NoSQL database. NoSQL databases are suitable for storing diverse data types and supporting high-speed read/write operations.`
   - [ ] Yes ✅: `This is correct because batch processing can output data to NoSQL databases, such as MongoDB or Cassandra. Batch jobs can write processed data to NoSQL collections or tables, which are designed to handle large volumes of unstructured or semi-structured data.`
3. Batch processing can output data to a relational database.
   - [ ] No ❌: `This is incorrect because batch processing can indeed output data to a relational database. Relational databases are often used to store processed data for further analysis and reporting.`
   - [ ] Yes ✅: `This is correct because batch processing can output data to relational databases, such as SQL Server or MySQL. Batch jobs can insert, update, or delete records in relational tables as part of the data processing workflow.`

## Q2: Understanding SQL Query Types

> For each of the following statements about SQL query types, select if the statement is correct.

- [ ] **A SELECT query can retrieve multiple columns from a table at once.** ✅: `This is correct because a SELECT query can specify multiple columns in its column list to retrieve several pieces of information from a table.`
- [ ] **An INSERT query can add multiple rows to a table in one execution.** ✅: `This is correct because an INSERT query can be used with multiple value sets to add several rows to a table in a single execution.`
- [ ] **A DELETE query removes all rows from a table without deleting its structure.** ❌: `This is incorrect because a DELETE query removes rows based on a condition but does not remove all rows without deleting the table structure; the TRUNCATE query is used for that purpose.`

## Q3: Understanding Database Schemas

> To complete the sentence, select the appropriate option.

A star schema:
- [ ] **is a type of database schema that organizes data into fact and dimension tables, with the fact table at the center connected to dimension tables like a star.** ✅: `This is correct because a star schema organizes data into fact and dimension tables, with the fact table at the center connected to dimension tables like a star.`
- [ ] **is a more complex type of database schema that normalizes dimension tables into multiple related tables.** ❌: `This is incorrect because this describes a snowflake schema, not a star schema.`
- [ ] **is a field in one table that uniquely identifies a row of another table.** ❌: `This is incorrect because this describes a foreign key, not a star schema.`
- [ ] **is a precompiled collection of SQL statements stored under a name.** ❌: `This is incorrect because this describes a stored procedure, not a star schema.`

## Q4: Understanding Database Indexes

> To complete the sentence, select the appropriate option.

A non-clustered index:
- [ ] **is an object associated with a table that sorts and stores the data rows in the table based on their key values.** ❌: `This is incorrect because a non-clustered index does not affect the physical order of the data rows; it creates a separate structure to store the index.`
- [ ] **is a feature that allows storing files and documents in special tables.** ❌: `This is incorrect because this describes a FileTable, which is used for storing files and documents, not a non-clustered index.`
- [ ] **is a precompiled collection of SQL statements stored under a name.** ❌: `This is incorrect because this describes a stored procedure, which is a set of SQL statements stored for repeated execution, not a non-clustered index.`
- [ ] **is an object that creates a separate structure to store the index and includes pointers to the data rows.** ✅: `This is correct because a non-clustered index creates a separate structure that stores the index and includes pointers to the actual data rows in the table.`

## Q5: Understanding SQL Server Features

> To complete the sentence, select the appropriate option.

A FileTable:
- [ ] **is an object associated with a table that sorts and stores the data rows in the table based on their key values.** ❌: `This is incorrect because this describes a clustered index, which organizes data rows based on key values, not a FileTable.`
- [ ] **is a field in one table that uniquely identifies a row of another table.** ❌: `This is incorrect because this describes a foreign key, which establishes relationships between tables, not a FileTable.`
- [ ] **is a precompiled collection of SQL statements stored under a name.** ❌: `This is incorrect because this describes a stored procedure, which is used to execute SQL statements as a unit, not a FileTable.`
- [ ] **is a feature that allows storing files and documents in special tables where each row represents a file or directory.** ✅: `This is correct because a FileTable integrates with the Windows file system to store files and documents in SQL Server tables.`

## Q6: Understanding Database Relationships

> To complete the sentence, select the appropriate option.

A foreign key:
- [ ] **is an object associated with a table that sorts and stores the data rows in the table based on their key values.** ❌: `This is incorrect because this describes a clustered index, which affects the physical order of data rows, not a foreign key.`
- [ ] **is a feature that allows storing files and documents in special tables where each row represents a file or directory.** ❌: `This is incorrect because this describes a FileTable, which is used for file storage, not a foreign key.`
- [ ] **is a precompiled collection of SQL statements stored under a name.** ❌: `This is incorrect because this describes a stored procedure, which is used to execute SQL statements as a unit, not a foreign key.`
- [ ] **is a field in one table that uniquely identifies a row of another table, creating a relationship between the two tables.** ✅: `This is correct because a foreign key ensures referential integrity by linking rows in one table to rows in another table.`

## Q7: Understanding Stored Procedures

> To complete the sentence, select the appropriate option.

A stored procedure:
- [ ] **is an object associated with a table that sorts and stores the data rows in the table based on their key values.** ❌: `This is incorrect because this describes a clustered index, which organizes data rows based on key values, not a stored procedure.`
- [ ] **is a feature that allows storing files and documents in special tables where each row represents a file or directory.** ❌: `This is incorrect because this describes a FileTable, which is used for file storage, not a stored procedure.`
- [ ] **is a field in one table that uniquely identifies a row of another table.** ❌: `This is incorrect because this describes a foreign key, which establishes relationships between tables, not a stored procedure.`
- [ ] **is a precompiled collection of SQL statements stored under a name and processed as a unit.** ✅: `This is correct because a stored procedure allows for the execution of a set of SQL statements as a single unit, improving efficiency and reusability.`

## Q8: Understanding Data Manipulation Language (DML)

> Which statement is an example of Data Manipulation Language (DML)?

- [ ] **REVOKE** ❌: `This is incorrect because REVOKE is a Data Control Language (DCL) statement used to remove permissions.`
- [ ] **DISABLE** ❌: `This is incorrect because DISABLE is not a standard SQL statement.`
- [ ] **GRANT** ❌: `This is incorrect because GRANT is a Data Control Language (DCL) statement used to provide permissions.`
- [ ] **INSERT** ✅: `This is correct because INSERT is a Data Manipulation Language (DML) statement used to add new records to a table.`

## Q9: Understanding Data Definition Language (DDL)

> Which statement is an example of Data Definition Language (DDL)?

- [ ] **SELECT** ❌: `This is incorrect because SELECT is a Data Query Language (DQL) statement used to retrieve data from a database.`
- [ ] **UPDATE** ❌: `This is incorrect because UPDATE is a Data Manipulation Language (DML) statement used to modify existing records in a table.`
- [ ] **COMMIT** ❌: `This is incorrect because COMMIT is a Transaction Control Language (TCL) statement used to save all changes made during the current transaction.`
- [ ] **CREATE** ✅: `This is correct because CREATE is a Data Definition Language (DDL) statement used to create database objects such as tables, indexes, and schemas.`

## Q10: Understanding Data Control Language (DCL)

> Which statement is an example of Data Control Language (DCL)?

- [ ] **INSERT** ❌: `This is incorrect because INSERT is a Data Manipulation Language (DML) statement used to add new records to a table.`
- [ ] **ALTER** ❌: `This is incorrect because ALTER is a Data Definition Language (DDL) statement used to modify existing database objects.`
- [ ] **ROLLBACK** ❌: `This is incorrect because ROLLBACK is a Transaction Control Language (TCL) statement used to undo changes made during the current transaction.`
- [ ] **GRANT** ✅: `This is correct because GRANT is a Data Control Language (DCL) statement used to provide permissions to users.`

## Q11: Understanding Database Types

> For each of the following statements about database types, select if the statement is correct.

- [ ] **Column family databases are suitable for applications requiring complex joins and relationships.** ❌: `This is incorrect because column family databases are not designed for complex joins and relationships; they are optimized for large volumes of structured data.`
- [ ] **Key-value stores are suitable for applications requiring high-speed transactions and real-time analytics.** ❌: `This is incorrect because key-value stores are designed for simple lookups and do not support high-speed transactions and real-time analytics.`
- [ ] **Document databases are suitable for applications requiring flexible schemas and semi-structured data.** ✅: `This is correct because document databases provide flexible schemas and are designed to handle semi-structured data.`
- [ ] **Graph databases are suitable for applications requiring the analysis of social networks and recommendation systems.** ✅: `This is correct because graph databases are ideal for analyzing social networks, recommendation systems, and other applications involving complex relationships.`
      
## Q12: Understanding Transaction Control Language (TCL)

> Which statement is an example of Transaction Control Language (TCL)?

- [ ] **DELETE** ❌: `This is incorrect because DELETE is a Data Manipulation Language (DML) statement used to remove records from a table.`
- [ ] **DROP** ❌: `This is incorrect because DROP is a Data Definition Language (DDL) statement used to delete database objects.`
- [ ] **SELECT** ❌: `This is incorrect because SELECT is a Data Query Language (DQL) statement used to retrieve data from a database.`
- [ ] **SAVEPOINT** ✅: `This is correct because SAVEPOINT is a Transaction Control Language (TCL) statement used to set a point within a transaction to which you can later roll back.`

## Q13: Understanding Data Query Language (DQL)

> Which statement is an example of Data Query Language (DQL)?

- [ ] **UPDATE** ❌: `This is incorrect because UPDATE is a Data Manipulation Language (DML) statement used to modify existing records in a table.`
- [ ] **TRUNCATE** ❌: `This is incorrect because TRUNCATE is a Data Definition Language (DDL) statement used to remove all records from a table without logging individual row deletions.`
- [ ] **COMMIT** ❌: `This is incorrect because COMMIT is a Transaction Control Language (TCL) statement used to save all changes made during the current transaction.`
- [ ] **SELECT** ✅: `This is correct because SELECT is a Data Query Language (DQL) statement used to retrieve data from a database.`

## Q14: Understanding Database Concepts

> Which database object improves the speed of data retrieval operations on a table by providing quick access to rows?

- [ ] **View** ❌: `This is incorrect because a view is a virtual table based on the result set of an SQL query, not an object that improves data retrieval speed.`
- [ ] **Scalar Function** ❌: `This is incorrect because a scalar function returns a single value and is used for calculations or operations on data, not for improving data retrieval speed.`
- [ ] **Table** ❌: `This is incorrect because a table is a database object that stores data in rows and columns, not an object that improves data retrieval speed.`
- [ ] **Index** ✅: `This is correct because an index is a database object that improves the speed of data retrieval operations on a table by providing quick access to rows.`

## Q15: Understanding Database Types

> For each of the following statements about database types, select if the statement is correct.

- [ ] **Key-value stores are optimized for complex queries and transactions.** ❌: `This is incorrect because key-value stores are designed for simple lookups and do not support complex queries and transactions.`
- [ ] **Column family databases are optimized for storing and managing large volumes of structured data.** ✅: `This is correct because column family databases are designed to handle large volumes of structured data efficiently.`
- [ ] **Document databases are optimized for storing and retrieving semi-structured data.** ✅: `This is correct because document databases are designed to store and retrieve semi-structured data, such as JSON or XML documents.`
- [ ] **Graph databases are optimized for storing and analyzing relationships between entities.** ✅: `This is correct because graph databases are specifically designed to store and analyze relationships between entities using nodes and edges.`

## Q16: Understanding Database Concepts

> Which database object is a virtual table based on the result set of an SQL query?

- [ ] **Index** ❌: `This is incorrect because an index is a database object that improves data retrieval speed, not a virtual table.`
- [ ] **Scalar Function** ❌: `This is incorrect because a scalar function returns a single value and is used for calculations or operations on data, not a virtual table.`
- [ ] **Table** ❌: `This is incorrect because a table is a database object that stores data in rows and columns, not a virtual table.`
- [ ] **View** ✅: `This is correct because a view is a virtual table based on the result set of an SQL query.`

## Q17: Understanding Database Concepts

> Which database object returns a single value and is typically used to perform calculations or operations on data?

- [ ] **Index** ❌: `This is incorrect because an index is a database object that improves data retrieval speed, not one that returns a single value.`
- [ ] **View** ❌: `This is incorrect because a view is a virtual table based on the result set of an SQL query, not an object that returns a single value.`
- [ ] **Table** ❌: `This is incorrect because a table is a database object that stores data in rows and columns, not one that returns a single value.`
- [ ] **Scalar Function** ✅: `This is correct because a scalar function returns a single value and is typically used to perform calculations or operations on data.`

## Q18: Understanding Database Concepts

> Which database object stores data in rows and columns, forming the basic structure of a relational database?

- [ ] **Index** ❌: `This is incorrect because an index is a database object that improves data retrieval speed, not one that stores data in rows and columns.`
- [ ] **View** ❌: `This is incorrect because a view is a virtual table based on the result set of an SQL query, not one that stores data in rows and columns.`
- [ ] **Scalar Function** ❌: `This is incorrect because a scalar function returns a single value and is used for calculations or operations on data, not one that stores data in rows and columns.`
- [ ] **Table** ✅: `This is correct because a table is a database object that stores data in rows and columns, forming the basic structure of a relational database.`

## Q19: Understanding Database Types

> For each of the following statements about database types, select if the statement is correct.

- [ ] **Column family databases natively support the analysis of relationships between entities.** ❌: `This is incorrect because column family databases are designed for storing and managing large volumes of structured data, not for analyzing relationships between entities.`
- [ ] **Document databases natively support the analysis of relationships between entities.** ❌: `This is incorrect because document databases are designed for storing and retrieving semi-structured data, not for analyzing relationships between entities.`
- [ ] **Key-value stores natively support the analysis of relationships between entities.** ❌: `This is incorrect because key-value stores are designed for simple lookups and do not natively support the analysis of relationships between entities.`
- [ ] **Graph databases natively support the analysis of relationships between entities.** ✅: `This is correct because graph databases are specifically designed to store and analyze relationships between entities using nodes and edges.`

## Q20: Understanding Aggregate Functions

> For each of the following statements about aggregate functions, select if the statement is correct.

- [ ] **Aggregate functions include functions like UPPER and LOWER.** ❌: `This is incorrect because UPPER and LOWER are scalar functions, not aggregate functions.`
- [ ] **Aggregate functions can be used to concatenate strings.** ❌: `This is incorrect because concatenating strings is typically done using string functions like CONCAT, not aggregate functions.`
- [ ] **Aggregate functions are used to perform operations on date and time values.** ❌: `This is incorrect because operations on date and time values are typically done using date functions, not aggregate functions.`
- [ ] **Aggregate functions perform a calculation on a set of values and return a single value.** ✅: `This is correct because aggregate functions like MAX, MIN, SUM, AVG, and COUNT perform calculations on a set of values and return a single value.`

## Q21: Understanding Scalar Functions

> For each of the following statements about scalar functions, select if the statement is correct.

- [ ] **Scalar functions are used to perform calculations across a set of table rows.** ❌: `This is incorrect because calculations across a set of table rows are typically done using window functions, not scalar functions.`
- [ ] **Scalar functions include functions like SUM and AVG.** ❌: `This is incorrect because SUM and AVG are aggregate functions, not scalar functions.`
- [ ] **Scalar functions return a single value based on the input value.** ✅: `This is correct because scalar functions like UPPER, LOWER, ROUND, and LEN return a single value based on the input value.`
- [ ] **Scalar functions can be used to perform operations on string values.** ✅: `This is correct because scalar functions like UPPER and LOWER perform operations on string values.`

## Q22: Understanding Date Functions

> For each of the following statements about date functions, select if the statement is correct.

- [ ] **Date functions are used to convert a value from one data type to another.** ❌: `This is incorrect because converting a value from one data type to another is typically done using conversion functions like CAST and CONVERT.`
- [ ] **Date functions include functions like CONCAT and SUBSTRING.** ❌: `This is incorrect because CONCAT and SUBSTRING are string functions, not date functions.`
- [ ] **Date functions perform operations on date and time values and return a date, time, or numeric value.** ✅: `This is correct because date functions like GETDATE, DATEADD, DATEDIFF, and FORMAT perform operations on date and time values and return a date, time, or numeric value.`
- [ ] **Date functions can be used to calculate the difference between two dates.** ✅: `This is correct because date functions like DATEDIFF can be used to calculate the difference between two dates.`

## Q23: Understanding Database Normalization

> For each of the following statements about database normalization, select Yes if the statement is true. Otherwise, select No.

1. Normalizing a database increases the throughput of writing transactions.
   - [ ] Yes ❌: `This is incorrect because normalizing a database often involves splitting tables, which can increase the number of write operations and potentially decrease throughput.`
   - [ ] No ✅: `This is correct because normalizing a database can increase the number of write operations, potentially decreasing throughput.`
2. Analytics systems are more normalized than transactional systems.
   - [ ] Yes ❌: `This is incorrect because transactional systems are typically more normalized to ensure data integrity and reduce redundancy, while analytics systems often use denormalized structures for performance.`
   - [ ] No ✅: `This is correct because transactional systems are typically more normalized, while analytics systems often use denormalized structures for performance.`
3. Normalizing a database results in queries that require more joins.
   - [ ] Yes ✅: `This is correct because normalizing a database often involves splitting data into multiple tables, which can result in queries that require more joins to retrieve related data.`
   - [ ] No ❌: `This is incorrect because normalizing a database often results in queries that require more joins.`

<!-- START BADGE -->
<div align="center">
  <img src="https://img.shields.io/badge/Total%20views-268-limegreen" alt="Total views">
  <p>Refresh Date: 2025-07-16</p>
</div>
<!-- END BADGE -->
