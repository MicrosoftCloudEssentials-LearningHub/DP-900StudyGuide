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

</details>

<details>
<summary><b>List of questions/answers </b> (Click to expand)</summary>

</details>


> [!TIP]
> Database management systems (DBMS) concepts:

| Concept            | Explanation                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| Clustered Index    | A type of database index that sorts and stores the data rows in the table based on their key values. The table is physically ordered according to this index. |
| FileTable          | A feature in SQL Server that allows storing files and documents in special tables where each row represents a file or directory, integrating with the Windows file system. |
| Foreign Key        | A field (or collection of fields) in one table that uniquely identifies a row of another table, creating a relationship between the two tables. It ensures referential integrity within the database. |
| Stored Procedure   | A precompiled collection of one or more SQL statements stored under a name and processed as a unit, which can be executed with parameters to perform specific tasks within the database. |

## Q: Understanding Batch Processing Outputs

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

  
## Q: Understanding SQL Query Types

> For each of the following statements about SQL query types, select if the statement is correct.

- [ ] **A SELECT query can retrieve multiple columns from a table at once.** ✅: `This is correct because a SELECT query can specify multiple columns in its column list to retrieve several pieces of information from a table.`
- [ ] **An INSERT query can add multiple rows to a table in one execution.** ✅: `This is correct because an INSERT query can be used with multiple value sets to add several rows to a table in a single execution.`
- [ ] **A DELETE query removes all rows from a table without deleting its structure.** ❌: `This is incorrect because a DELETE query removes rows based on a condition but does not remove all rows without deleting the table structure; the TRUNCATE query is used for that purpose.`

## Q: Understanding Database Schemas

> To complete the sentence, select the appropriate option.

A star schema:
- [ ] **is a type of database schema that organizes data into fact and dimension tables, with the fact table at the center connected to dimension tables like a star.** ✅: `This is correct because a star schema organizes data into fact and dimension tables, with the fact table at the center connected to dimension tables like a star.`
- [ ] **is a more complex type of database schema that normalizes dimension tables into multiple related tables.** ❌: `This is incorrect because this describes a snowflake schema, not a star schema.`
- [ ] **is a field in one table that uniquely identifies a row of another table.** ❌: `This is incorrect because this describes a foreign key, not a star schema.`
- [ ] **is a precompiled collection of SQL statements stored under a name.** ❌: `This is incorrect because this describes a stored procedure, not a star schema.`

## Q: Understanding Database Indexes

> To complete the sentence, select the appropriate option.

A non-clustered index:
- [ ] **is an object associated with a table that sorts and stores the data rows in the table based on their key values.** ❌: `This is incorrect because a non-clustered index does not affect the physical order of the data rows; it creates a separate structure to store the index.`
- [ ] **is a feature that allows storing files and documents in special tables.** ❌: `This is incorrect because this describes a FileTable, which is used for storing files and documents, not a non-clustered index.`
- [ ] **is a precompiled collection of SQL statements stored under a name.** ❌: `This is incorrect because this describes a stored procedure, which is a set of SQL statements stored for repeated execution, not a non-clustered index.`
- [ ] **is an object that creates a separate structure to store the index and includes pointers to the data rows.** ✅: `This is correct because a non-clustered index creates a separate structure that stores the index and includes pointers to the actual data rows in the table.`

## Q: Understanding SQL Server Features

> To complete the sentence, select the appropriate option.

A FileTable:
- [ ] **is an object associated with a table that sorts and stores the data rows in the table based on their key values.** ❌: `This is incorrect because this describes a clustered index, which organizes data rows based on key values, not a FileTable.`
- [ ] **is a field in one table that uniquely identifies a row of another table.** ❌: `This is incorrect because this describes a foreign key, which establishes relationships between tables, not a FileTable.`
- [ ] **is a precompiled collection of SQL statements stored under a name.** ❌: `This is incorrect because this describes a stored procedure, which is used to execute SQL statements as a unit, not a FileTable.`
- [ ] **is a feature that allows storing files and documents in special tables where each row represents a file or directory.** ✅: `This is correct because a FileTable integrates with the Windows file system to store files and documents in SQL Server tables.`

## Q: Understanding Database Relationships

> To complete the sentence, select the appropriate option.

A foreign key:
- [ ] **is an object associated with a table that sorts and stores the data rows in the table based on their key values.** ❌: `This is incorrect because this describes a clustered index, which affects the physical order of data rows, not a foreign key.`
- [ ] **is a feature that allows storing files and documents in special tables where each row represents a file or directory.** ❌: `This is incorrect because this describes a FileTable, which is used for file storage, not a foreign key.`
- [ ] **is a precompiled collection of SQL statements stored under a name.** ❌: `This is incorrect because this describes a stored procedure, which is used to execute SQL statements as a unit, not a foreign key.`
- [ ] **is a field in one table that uniquely identifies a row of another table, creating a relationship between the two tables.** ✅: `This is correct because a foreign key ensures referential integrity by linking rows in one table to rows in another table.`

## Q: Understanding Stored Procedures

> To complete the sentence, select the appropriate option.

A stored procedure:
- [ ] **is an object associated with a table that sorts and stores the data rows in the table based on their key values.** ❌: `This is incorrect because this describes a clustered index, which organizes data rows based on key values, not a stored procedure.`
- [ ] **is a feature that allows storing files and documents in special tables where each row represents a file or directory.** ❌: `This is incorrect because this describes a FileTable, which is used for file storage, not a stored procedure.`
- [ ] **is a field in one table that uniquely identifies a row of another table.** ❌: `This is incorrect because this describes a foreign key, which establishes relationships between tables, not a stored procedure.`
- [ ] **is a precompiled collection of SQL statements stored under a name and processed as a unit.** ✅: `This is correct because a stored procedure allows for the execution of a set of SQL statements as a single unit, improving efficiency and reusability.`


<div align="center">
  <h3 style="color: #4CAF50;">Total Visitors</h3>
  <img src="https://profile-counter.glitch.me/brown9804/count.svg" alt="Visitor Count" style="border: 2px solid #4CAF50; border-radius: 5px; padding: 5px;"/>
</div>
