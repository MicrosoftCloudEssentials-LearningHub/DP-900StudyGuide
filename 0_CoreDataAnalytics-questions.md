# Core Data Concepts and Analytics Workload on Azure: Sample Questions and Answers 

Costa Rica

[![GitHub](https://img.shields.io/badge/--181717?logo=github&logoColor=ffffff)](https://github.com/)
[brown9804](https://github.com/brown9804)

Last updated: 2025-01-16

----------

> [!NOTE]
> The questions and answers provided in this study guide are for practice purposes only and are not official practice questions.
> They are intended to help you prepare for the [DP-900 Microsoft certification exam](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/dp-900).
> For additional preparation materials and the most up-to-date information, please refer to the [official Microsoft documentation](https://learn.microsoft.com/en-us/credentials/certifications/azure-data-fundamentals/?practice-assessment-type=certification).

- Describe core data concepts
- Describe an analytics workload on Azure

<details>
<summary><b>List of References </b> (Click to expand)</summary>

- [Describe core concepts of data modeling](https://learn.microsoft.com/en-us/training/modules/explore-fundamentals-data-visualization/3-data-modeling)
- [Dedicated SQL pool (formerly SQL DW) architecture in Azure Synapse Analytics](https://learn.microsoft.com/en-us/azure/synapse-analytics/sql-data-warehouse/massively-parallel-processing-mpp-architecture)
- [Extract, transform, and load (ETL)](https://learn.microsoft.com/en-us/azure/architecture/data-guide/relational-data/etl)

</details>

<details>
<summary><b>List of questions/answers </b> (Click to expand)</summary>

</details>

> [!TIP]
> Types and descriptions:

| Type of Analytics | Description |
|-------------------|-------------|
| Descriptive       | Summarizes past data to understand `what has happened`. → `What happened?` |
| Diagnostic        | Analyzes data to understand `why something happened`. → `Why did it happen?`|
| Prescriptive      | Provides `recommendations` for actions based on data analysis. → `What should I do?`|
| Predictive        | Uses historical data to `predict future outcomes`. |
| Real-time         | Analyzes data as it is generated to provide `immediate insights`. |
| Cognitive         | Uses AI and machine learning to `simulate human` thought processes in data analysis. |

> [!TIP]
> Data Schema and Terms:

| Term                | Description                                                                 |
|---------------------|-----------------------------------------------------------------------------|
| Transactional Model | A database model designed to manage transactions, ensuring data integrity and consistency. |
| Star Schema         | A type of database schema that organizes data into fact and dimension tables, with the fact table at the center connected to dimension tables like a star. |
| Snowflake Schema    | A more complex type of database schema that normalizes dimension tables into multiple related tables, resembling a snowflake shape. |
| Fact                | A table in a database schema that contains quantitative data for analysis, often linked to dimension tables. |
| Dimension           | A table in a database schema that contains descriptive attributes related to the facts, used for filtering and grouping data. |
| Bridge              | A table used to handle many-to-many relationships between fact and dimension tables in a database schema. |

> [!TIP]
> Nested structures:

```json
{
  "employee": {
    "first_name": "Jane",
    "last_name": "Doe",
    "address": {
      "line_1": "123 Main St",
      "line_2": "Suite 400",
      "city": "Los Angeles",
      "state": "CA",
      "ZIP_code": "90001"
    },
    "contacts": [
      {
        "type": "email",
        "value": "jane.doe@example.com"
      },
      {
        "type": "phone",
        "value": "555-123-4567"
      }
    ],
    "projects": [
      {
        "name": "Project Alpha",
        "role": "Lead Developer"
      },
      {
        "name": "Project Beta",
        "role": "Consultant"
      }
    ]
  }
}
```

| Term            | Description                                                                 | Example                                                                 |
|-----------------|-----------------------------------------------------------------------------|-------------------------------------------------------------------------|
| Root Object     | The top-level object in a hierarchy, not contained within any other object. | `{ "employee": { ... } }`                                               |
| Nested Object   | An object that is contained within another object.                          | `"address": { "line_1": "123 Main St", "line_2": "Suite 400", "city": "Los Angeles", "state": "CA", "ZIP_code": "90001" }` |
| Nested Array    | An array that is contained within another array or object.                  | `"contacts": [ { "type": "email", "value": "jane.doe@example.com" }, { "type": "phone", "value": "555-123-4567" } ]` ➡️ [ ] |

> [!TIP]
> Synapse SQL architecture components, from [official Microsoft documentation](https://learn.microsoft.com/en-us/azure/synapse-analytics/sql-data-warehouse/massively-parallel-processing-mpp-architecture#synapse-sql-architecture-components)

<div align="center">
  <img src="https://github.com/user-attachments/assets/a0cf4ab0-3cb9-439d-be45-8525567240e4" alt="Centered Image" style="border: 2px solid #4CAF50; border-radius: 4px; padding: 4px; width: 500px; height: auto;"/>
</div>


> [!TIP]
> Relational and Non Relational critieria:

Relational Databases:
- When you need strong data integrity and ACID compliance.
- When your data structure is well-defined and unlikely to change frequently.
- When you need to perform complex queries and transactions.
- When your application requires strong relationships between data entities.

Non-Relational Databases:
- When you need to handle large volumes of unstructured or semi-structured data.
- When your data schema is flexible and may change frequently.
- When you need high-speed read/write operations and horizontal scalability.
- When your application involves real-time analytics, content management, or IoT data.


| Criteria                        | Relational Databases (SQL)                                      | Non-Relational Databases (NoSQL)                                  |
|---------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------|
| **Data Structure**              | Structured data with predefined schema                         | Unstructured or semi-structured data                              |
| **Schema Flexibility**          | Fixed schema, requires schema changes for modifications        | Flexible schema, easily accommodates changes                      |
| **Data Relationships**          | Strong relationships with foreign keys and joins               | Limited or no support for complex relationships                   |
| **Query Language**              | SQL (Structured Query Language)                                | Varies (e.g., JSON, XML, key-value pairs, graph queries)          |
| **Transaction Support**         | ACID (Atomicity, Consistency, Isolation, Durability) compliant | May support BASE (Basically Available, Soft state, Eventual consistency) |
| **Use Case Examples**           | Financial systems, ERP, CRM, inventory management              | Social networks, content management, IoT data, real-time analytics|
| **Scalability**                 | Vertical scaling (adding more power to existing hardware)      | Horizontal scaling (adding more servers)                          |
| **Performance**                 | Optimized for complex queries and transactions                 | Optimized for large volumes of data and high-speed read/write operations |
| **Consistency**                 | Strong consistency                                             | Eventual consistency (in some cases)                              |
| **Examples**                    | MySQL, PostgreSQL, Oracle, SQL Server                          | MongoDB, Cassandra, Redis, Couchbase, Neo4j                       |

## Q: Understanding Descriptive Analytics

> Descriptive analytics tells you:

- [ ] what is most likely to occur in the future.
- [ ] what occurred in the past. ✅
- [ ] which actions you can perform to affect outcomes.
- [ ] why something occurred in the past.

## Q: Understanding Batch Processing

> To complete the sentence, choose the correct option from the answer area.

In batch processing:
- [ ] **data is inserted one record at a time.** ❌: `This is incorrect because batch processing typically involves processing multiple records at once, not one at a time.`
- [ ] **data is handled immediately as it arrives.** ❌: `This is incorrect because batch processing involves handling data in groups or batches, not in real-time.`
- [ ] **delays in processing results are acceptable.** ✅: `This is correct because batch processing can tolerate some delay in delivering results, as it processes data in batches rather than immediately.`
- [ ] **tasks must be executed sequentially.** ❌: `This is incorrect because batch processing can be parallelized to improve efficiency, rather than being limited to sequential execution.`


## Q: Understanding Predictive Analytics

> Predictive analytics helps you:

- [ ] understand why something happened.
- [ ] summarize past data.
- [ ] predict future outcomes. ✅
- [ ] recommend actions to take.

## Q: Understanding Types of Analytics

> To complete the sentence, select the appropriate option.

Analyzing customer feedback to determine the reasons for a drop in sales is an example of ______ analytics.

Options:
- [ ] **cognitive** ❌: `This is incorrect because cognitive analytics involves using AI and machine learning to simulate human thought processes.`
- [ ] **descriptive** ❌: `This is incorrect because descriptive analytics summarizes past data to understand what has happened.`
- [ ] **predictive** ❌: `This is incorrect because predictive analytics uses historical data to predict future outcomes.`
- [ ] **diagnostic** ✅: `This is correct because diagnostic analytics analyzes data to understand why something happened.`


## Q: Understanding Diagnostic Analytics

> Diagnostic analytics is used to:

- [ ] summarize past data.
- [ ] understand why something happened. ✅
- [ ] predict future outcomes.
- [ ] recommend actions to take.

## Q: Understanding Cognitive Analytics

> To complete the sentence, select the appropriate option.

Analyzing customer service chat logs to provide real-time sentiment analysis is an example of ______ analytics.

- [ ] **descriptive** ❌: `This is incorrect because descriptive analytics summarizes past data to understand what has happened.`
- [ ] **predictive** ❌: `This is incorrect because predictive analytics uses historical data to predict future outcomes.`
- [ ] **prescriptive** ❌: `This is incorrect because prescriptive analytics provides recommendations for actions based on data analysis.`
- [ ] **cognitive** ✅: `This is correct because cognitive analytics involves using AI and machine learning to simulate human thought processes and analyze unstructured data.`

## Q: Understanding Prescriptive Analytics

> Prescriptive analytics provides:

- [ ] summaries of past data.
- [ ] reasons why something happened.
- [ ] predictions of future outcomes.
- [ ] recommendations for actions. ✅

## Q: Understanding Types of Analytics

> You are working on a data project and need to choose the appropriate type of analytics for different scenarios. Match each scenario with the correct type of analytics: <br/>
> - Summarizing past sales data to understand trends. <br/>
> - Analyzing customer feedback to determine why sales dropped. <br/>
> - Predicting future sales based on historical data. <br/>
> - Recommending actions to increase future sales. <br/>

Which type of analytics should you use for each scenario?

- [ ] Descriptive, Diagnostic, Predictive, Prescriptive ❌: `This is incorrect because the order of analytics types does not match the scenarios provided.`
- [ ] Diagnostic, Descriptive, Predictive, Prescriptive ❌: `This is incorrect because the first two analytics types are not correctly matched with the scenarios.`
- [ ] Descriptive, Diagnostic, Prescriptive, Predictive ❌: `This is incorrect because the last two analytics types are not correctly matched with the scenarios.`
- [ ] Descriptive, Diagnostic, Predictive, Prescriptive ✅: `This is correct because Descriptive analytics summarizes past data, Diagnostic analytics analyzes reasons for past events, Predictive analytics forecasts future outcomes, and Prescriptive analytics recommends actions.`

## Q: Understanding Database Normalization

> For each of the following statements about database normalization, select if the statement is correct.

- [ ] **Normalization involves organizing data to reduce redundancy.** ✅: `This is correct because one of the primary goals of normalization is to reduce data redundancy by organizing data into related tables.`
- [ ] **Normalizing a database can improve data integrity.** ✅: `This is correct because normalization helps maintain consistency and accuracy in the database, thereby improving data integrity.`
- [ ] **Normalization eliminates the need for relationships between tables.** ❌: `This is incorrect because normalization does not eliminate the need for relationships between tables; instead, it organizes data into related tables with defined relationships.`

## Q: Understanding ETL Process Requirements

```mermaid
graph LR
    A[Data Source] -->|Extract| B[Extract]
    B -->|Transform| C[Transform]
    C -->|Load| D[Target Data Store]
    style A fill:#1f77b4,stroke:#fff,stroke-width:2px;
    style B fill:#ff7f0e,stroke:#fff,stroke-width:2px;
    style C fill:#2ca02c,stroke:#fff,stroke-width:2px;
    style D fill:#d62728,stroke:#fff,stroke-width:2px;
```

> To complete the sentence, select the appropriate option.

An extract, transform, and load (ETL) process requires:

- [ ] **a matching schema in the data source and the data target.** ❌: `This is incorrect because ETL processes do not necessarily require matching schemas between the source and target.`
- [ ] **a target data store powerful enough to transform data.** ❌: `This is incorrect because the transformation typically occurs in an intermediate staging area, not necessarily in the target data store.`
- [ ] **data that is fully processed before being loaded to the target data store.** ✅: `This is correct because ETL processes involve extracting data, transforming it as needed, and then loading the fully processed data into the target data store.`
- [ ] **that the data target be a relational database.** ❌: `This is incorrect because ETL processes can load data into various types of data stores, not just relational databases.`

## Q: Understanding ELT Process Requirements

```mermaid
graph LR
    A[Data Source] -->|Extract| B[Extract]
    B -->|Load| C[Target Data Store]
    C -->|Transform| D[Transform]
    style A fill:#1f77b4,stroke:#fff,stroke-width:2px;
    style B fill:#ff7f0e,stroke:#fff,stroke-width:2px;
    style C fill:#d62728,stroke:#fff,stroke-width:2px;
    style D fill:#2ca02c,stroke:#fff,stroke-width:2px;
```

> To complete the sentence, select the appropriate option.

An extract, load, and transform (ELT) process requires:
- [ ] **a matching schema in the data source and the data target.** ❌: `This is incorrect because ELT processes do not necessarily require matching schemas between the source and target.`
- [ ] **a target data store powerful enough to transform data.** ✅: `This is correct because in ELT processes, the transformation occurs after the data is loaded into the target data store, which needs to be powerful enough to handle the transformation.`
- [ ] **data that is fully processed before being loaded to the target data store.** ❌: `This is incorrect because in ELT processes, data is loaded into the target data store before being transformed.`
- [ ] **that the data target be a relational database.** ❌: `This is incorrect because ELT processes can load data into various types of data stores, not just relational databases.`

## Q: Understanding JSON Structure

```json
{
  "product": {
    "product_id": "P12345",
    "name": "Smartphone",
    "specifications": {
      "brand": "TechBrand",
      "model": "X100",
      "features": [
        "5G",
        "128GB Storage",
        "6GB RAM"
      ]
    },
    "price": 699.99,
    "availability": [
      {
        "store": "Online",
        "stock": 50
      },
      {
        "store": "Retail",
        "stock": 30
      }
    ]
  }
}
```

> For each of the following statements about the JSON structure, select if the statement is correct.

- [ ] **The root object in the JSON structure is "product".** ✅: `This is correct because "product" is the top-level object in the hierarchy, not contained within any other object.`
- [ ] **The `specifications` field is an example of a nested array.** ❌: `This is incorrect because "specifications" is an example of a nested object, not an array.`
- [ ] **The `features` field contains a nested array.** ✅: `This is correct because "features" is an array that is contained within the "specifications" object.`
- [ ] **The `availability` field is a root object.** ❌: `This is incorrect because "availability" is a nested array within the "product" object, not a root object.`


## Q: Understanding Azure Synapse Analytics MPP Engine

> To complete the sentence, select the appropriate option.

The massively parallel processing (MPP) engine of Azure Synapse Analytics:

- [ ] **distributes processing across control nodes.** ❌: `This is incorrect because the control node is responsible for coordinating the processing, not for distributing it across multiple nodes.`
- [ ] **redirects client connections across compute nodes.** ❌: `This is incorrect because client connections are managed by the control node, not distributed across compute nodes.`
- [ ] **redirects client connections across control nodes.** ❌: `This is incorrect because there is typically a single control node that manages client connections and coordinates processing.`
- [ ] **distributes processing across compute nodes.** ✅: `This is correct because the MPP engine distributes data processing tasks across multiple compute nodes to handle large-scale data workloads efficiently.`

## Q: Understanding Database Types

> Which type of database is best suited for handling large volumes of unstructured or semi-structured data?

- [ ] Relational Database ❌: `This is incorrect because relational databases are best suited for structured data with predefined schemas.`
- [ ] Non-Relational Database ✅: `This is correct because non-relational databases are designed to handle large volumes of unstructured or semi-structured data.`

## Q: Understanding Database Scalability

> Which type of database typically supports horizontal scaling by adding more servers?

- [ ] Relational Database ❌: `This is incorrect because relational databases typically support vertical scaling by adding more power to existing hardware.`
- [ ] Non-Relational Database ✅: `This is correct because non-relational databases are designed to support horizontal scaling by adding more servers.`

## Q: Understanding Database Schema Flexibility

> Which type of database offers a flexible schema that can easily accommodate changes?

- [ ] Relational Database ❌: `This is incorrect because relational databases have fixed schemas that require changes for modifications.`
- [ ] Non-Relational Database ✅: `This is correct because non-relational databases offer flexible schemas that can easily accommodate changes.`

## Q: Understanding Transaction Support

> Which type of database is typically ACID compliant, ensuring strong data integrity and consistency?

- [ ] Relational Database ✅: `This is correct because relational databases are typically ACID compliant, ensuring strong data integrity and consistency.`
- [ ] Non-Relational Database ❌: `This is incorrect because non-relational databases may support BASE (Basically Available, Soft state, Eventual consistency) instead of ACID.`

## Q: Understanding Use Cases

> Which type of database is best suited for applications involving real-time analytics, content management, or IoT data?

- [ ] Relational Database ❌: `This is incorrect because relational databases are best suited for structured data and complex queries.`
- [ ] Non-Relational Database ✅: `This is correct because non-relational databases are optimized for applications involving real-time analytics, content management, or IoT data.`

## Q: Understanding ELT Process Stages

> Your company plans to load data from a customer relationship management (CRM) system to a data warehouse by using an extract, load, and transform (ELT) process. Where does data processing occur for each stage of the ELT process? Select the appropriate answer.

1. **Extract:**
   - [ ] **An in-memory data integration tool** ❌: `This is incorrect because the extraction stage typically involves pulling data directly from the source system, such as the CRM system.`
   - [ ] **The data warehouse** ❌: `This is incorrect because the data warehouse is typically the target for loading data, not the source for extraction.`
   - [ ] **The CRM system** ✅: `This is correct because the extraction stage involves pulling data from the CRM system.`
2. **Load:**
   - [ ] **An in-memory data integration tool** ❌: `This is incorrect because the loading stage involves moving data to the target system, such as the data warehouse.`
   - [ ] **The CRM system** ❌: `This is incorrect because the CRM system is the source for extraction, not the target for loading.`
   - [ ] **The data warehouse** ✅: `This is correct because the loading stage involves moving data to the data warehouse.`
3. **Transform:**
   - [ ] **An in-memory data integration tool** ❌: `This is incorrect because while in-memory tools can be used, the transformation stage is typically associated with the data warehouse in an ELT process.`
   - [ ] **The CRM system** ❌: `This is incorrect because the transformation stage does not typically occur in the source system.`
   - [ ] **The data warehouse** ✅: `This is correct because the transformation stage can occur within the data warehouse after the data has been loaded.`

## Q: Understanding ELT Process Stages

> In an ELT process, where does the transformation of data typically occur?

- [ ] **In the source system** ❌: `This is incorrect because in an ELT process, the transformation typically occurs after the data has been loaded into the target system.`
- [ ] **In an external ETL tool** ❌: `This is incorrect because ELT processes perform transformations within the target data store, not in an external ETL tool.`
- [ ] **In the target data store** ✅: `This is correct because in an ELT process, the transformation of data typically occurs within the target data store, such as a data warehouse, after the data has been loaded.`

## Q: Understanding ELT Process Stages

> Which stage of the ELT process involves moving data to the target data store?

- [ ] **Extract** ❌: `This is incorrect because the extract stage involves pulling data from the source system.`
- [ ] **Transform** ❌: `This is incorrect because the transform stage involves processing and transforming the data after it has been loaded into the target data store.`
- [ ] **Load** ✅: `This is correct because the load stage involves moving data to the target data store, such as a data warehouse.`

## Q: Understanding ELT Process Stages

> In an ELT process, which stage is responsible for pulling data from the source system?

- [ ] **Load** ❌: `This is incorrect because the load stage involves moving data to the target data store.`
- [ ] **Transform** ❌: `This is incorrect because the transform stage involves processing and transforming the data after it has been loaded into the target data store.`
- [ ] **Extract** ✅: `This is correct because the extract stage is responsible for pulling data from the source system, such as a CRM system.`

## Q: Understanding ELT Process Stages

> Which stage of the ELT process typically occurs within the data warehouse?

- [ ] **Extract** ❌: `This is incorrect because the extract stage involves pulling data from the source system.`
- [ ] **Load** ❌: `This is incorrect because the load stage involves moving data to the target data store.`
- [ ] **Transform** ✅: `This is correct because the transform stage typically occurs within the data warehouse after the data has been loaded.`



<div align="center">
  <h3 style="color: #4CAF50;">Total Visitors</h3>
  <img src="https://profile-counter.glitch.me/brown9804/count.svg" alt="Visitor Count" style="border: 2px solid #4CAF50; border-radius: 5px; padding: 5px;"/>
</div>
