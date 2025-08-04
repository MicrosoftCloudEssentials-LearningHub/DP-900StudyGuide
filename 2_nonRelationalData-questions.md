# Non-Relational Data on Azure: Sample Questions and Answers 

Costa Rica

[![GitHub](https://img.shields.io/badge/--181717?logo=github&logoColor=ffffff)](https://github.com/)
[brown9804](https://github.com/brown9804)

Last updated: 2025-07-16

----------

> [!NOTE]
> The questions and answers provided in this study guide are for practice purposes only and are not official practice questions.
> They are intended to help you prepare for the [DP-900 Microsoft certification exam](https://learn.microsoft.com/en-us/credentials/certifications/resources/study-guides/dp-900).
> For additional preparation materials and the most up-to-date information, please refer to the [official Microsoft documentation](https://learn.microsoft.com/en-us/credentials/certifications/azure-data-fundamentals/?practice-assessment-type=certification).

- Describe considerations for working with non-relational data on Azure

<details>
<summary><b>List of References </b> (Click to expand)</summary>

- [What is Azure Cosmos DB for Apache Gremlin?](https://learn.microsoft.com/en-us/azure/cosmos-db/gremlin/introduction)
  
</details>

<details>
<summary><b>List of questions/answers </b> (Click to expand)</summary>

- [Q1: Understanding NoSQL Database Types](#q1-understanding-nosql-database-types)
- [Q2: Understanding Azure Cosmos DB APIs](#q2-understanding-azure-cosmos-db-apis)
- [Q3: Understanding Azure Cosmos DB APIs](#q3-understanding-azure-cosmos-db-apis)
- [Q4: Understanding CAP Theorem](#q4-understanding-cap-theorem)
- [Q5: Understanding Azure Cosmos DB APIs](#q5-understanding-azure-cosmos-db-apis)
- [Q6: Understanding NoSQL Data Models](#q6-understanding-nosql-data-models)
- [Q7: Understanding NoSQL Use Cases](#q7-understanding-nosql-use-cases)
- [Q8: Understanding NoSQL Scalability](#q8-understanding-nosql-scalability)
- [Q9: Understanding Azure Cosmos DB APIs](#q9-understanding-azure-cosmos-db-apis)
- [Q10: Understanding Azure Cosmos DB APIs](#q10-understanding-azure-cosmos-db-apis)

</details>

> [!TIP]
> Cosmos APIs:

| Cosmos API        | Description                                                                 |
|------------|-----------------------------------------------------------------------------|
| Core (SQL) | A native API for Azure Cosmos DB that supports SQL-like queries to manage JSON documents. Ideal for applications requiring rich querying capabilities and transactional consistency. |
| Gremlin    | A graph database API based on Apache TinkerPop, used to store and query graph data with vertices and edges. Suitable for applications that need to model and traverse complex relationships. |
| MongoDB    | An API that provides wire protocol compatibility with MongoDB, allowing you to use existing MongoDB drivers and tools. Ideal for applications already using MongoDB. |
| Table      | An API that provides key-value storage with a schemaless design, compatible with Azure Table Storage. Suitable for applications that need a simple, scalable, and cost-effective storage solution. |

> [!TIP]
> CAP means:

The CAP theorem, also known as Brewer's theorem, states that in a distributed data store, it is impossible to simultaneously provide all three of the following guarantees. In essence, a distributed system can only achieve two out of the three properties at any given time.

1. **Consistency**: Every read receives the most recent write or an error.
2. **Availability**: Every request receives a response, without guarantee that it contains the most recent write.
3. **Partition Tolerance**: The system continues to operate despite an arbitrary number of messages being dropped (or delayed) by the network between nodes.


## Q1: Understanding NoSQL Database Types

> For each of the following statements about NoSQL database types, select if the statement is correct.

- [ ] **Key-value stores are optimized for complex queries and transactions.** ❌: `This is incorrect because key-value stores are optimized for simple lookups and do not support complex queries and transactions.`
- [ ] **Document databases store data in JSON-like documents.** ✅: `This is correct because document databases, such as MongoDB, store data in JSON-like documents, which allows for flexible schemas.`
- [ ] **Column family databases are designed for storing and managing large volumes of structured data.** ✅: `This is correct because column family databases, such as Apache Cassandra, are designed to handle large volumes of structured data efficiently.`
- [ ] **Graph databases use nodes and edges to represent and store data.** ✅: `This is correct because graph databases, such as Neo4j, use nodes and edges to represent and store data, making them ideal for analyzing relationships between entities.`

## Q2: Understanding Azure Cosmos DB APIs

> For each of the following statements about Azure Cosmos DB APIs, select if the statement is correct.

- [ ] **The Table API is used for complex relational queries.** ❌: `This is incorrect because the Table API provides key-value storage with a schemaless design, not for complex relational queries.`
- [ ] **The Core (SQL) API supports SQL-like queries to manage JSON documents.** ✅: `This is correct because the Core (SQL) API supports SQL-like queries to manage JSON documents.`
- [ ] **The Gremlin API is used to store and query graph data with vertices and edges.** ✅: `This is correct because the Gremlin API is based on Apache TinkerPop and is used to store and query graph data with vertices and edges.`
- [ ] **The MongoDB API provides wire protocol compatibility with MongoDB.** ✅: `This is correct because the MongoDB API provides wire protocol compatibility with MongoDB, allowing you to use existing MongoDB drivers and tools.`

## Q3: Understanding Azure Cosmos DB APIs

> For each of the following statements about Azure Cosmos DB APIs, select if the statement is correct.

- [ ] **The MongoDB API is not compatible with existing MongoDB drivers and tools.** ❌: `This is incorrect because the MongoDB API provides wire protocol compatibility with MongoDB, allowing the use of existing MongoDB drivers and tools.`
- [ ] **The Core (SQL) API is ideal for applications requiring rich querying capabilities and transactional consistency.** ✅: `This is correct because the Core (SQL) API supports SQL-like queries and provides transactional consistency, making it ideal for such applications.`
- [ ] **The Gremlin API is suitable for applications that need to model and traverse complex relationships.** ✅: `This is correct because the Gremlin API is designed for graph data, which is used to model and traverse complex relationships.`
- [ ] **The Table API is suitable for applications that need a simple, scalable, and cost-effective storage solution.** ✅: `This is correct because the Table API provides key-value storage with a schemaless design, making it suitable for simple, scalable, and cost-effective storage.`

## Q4: Understanding CAP Theorem

> For each of the following statements about the CAP theorem, select if the statement is correct.

- [ ] **The CAP theorem states that a distributed database can achieve consistency, availability, and partition tolerance simultaneously.** ❌: `This is incorrect because the CAP theorem states that a distributed database can only achieve two out of the three properties: consistency, availability, and partition tolerance.`
- [ ] **Consistency in the CAP theorem means that all nodes see the same data at the same time.** ✅: `This is correct because consistency ensures that all nodes in a distributed system see the same data at the same time.`
- [ ] **Availability in the CAP theorem means that every request receives a response, even if some nodes are down.** ✅: `This is correct because availability ensures that every request receives a response, even if some nodes are down.`
- [ ] **Partition tolerance in the CAP theorem means that the system continues to operate despite network partitions.** ✅: `This is correct because partition tolerance ensures that the system continues to operate even if there are network partitions.`

## Q5: Understanding Azure Cosmos DB APIs

> For each of the following statements about Azure Cosmos DB APIs, select if the statement is correct.

- [ ] **The Core (SQL) API is based on Apache TinkerPop.** ❌: `This is incorrect because the Core (SQL) API is not based on Apache TinkerPop; the Gremlin API is.`
- [ ] **The Gremlin API supports SQL-like queries to manage JSON documents.** ❌: `This is incorrect because the Gremlin API is used for graph data, not for SQL-like queries to manage JSON documents.`
- [ ] **The MongoDB API allows you to use existing MongoDB drivers and tools.** ✅: `This is correct because the MongoDB API provides wire protocol compatibility with MongoDB, allowing the use of existing MongoDB drivers and tools.`
- [ ] **The Table API provides key-value storage with a schemaless design.** ✅: `This is correct because the Table API provides key-value storage with a schemaless design.`

## Q6: Understanding NoSQL Data Models

> For each of the following statements about NoSQL data models, select if the statement is correct.

- [ ] **Document databases use a tabular format to store data.** ❌: `This is incorrect because document databases store data in JSON-like documents, not in a tabular format.`
- [ ] **Key-value stores use a simple key-value pair to store data.** ✅: `This is correct because key-value stores use a simple key-value pair to store data, making them ideal for simple lookups.`
- [ ] **Column family databases organize data into rows and columns, similar to relational databases.** ✅: `This is correct because column family databases organize data into rows and columns, but they are optimized for large-scale data storage and retrieval.`
- [ ] **Graph databases are designed to store and analyze relationships between entities.** ✅: `This is correct because graph databases use nodes and edges to represent and store data, making them ideal for analyzing relationships between entities.`

## Q7: Understanding NoSQL Use Cases

> For each of the following statements about NoSQL use cases, select if the statement is correct.

- [ ] **Key-value stores are suitable for applications requiring high-speed transactions and real-time analytics.** ❌: `This is incorrect because key-value stores are designed for simple lookups and do not support high-speed transactions and real-time analytics.`
- [ ] **Column family databases are suitable for applications requiring complex joins and relationships.** ❌: `This is incorrect because column family databases are not designed for complex joins and relationships; they are optimized for large volumes of structured data.`
- [ ] **Graph databases are suitable for applications requiring the analysis of social networks and recommendation systems.** ✅: `This is correct because graph databases are ideal for analyzing social networks, recommendation systems, and other applications involving complex relationships.`
- [ ] **Document databases are suitable for applications requiring flexible schemas and semi-structured data.** ✅: `This is correct because document databases provide flexible schemas and are designed to handle semi-structured data.`

## Q8: Understanding NoSQL Scalability

> For each of the following statements about NoSQL scalability, select if the statement is correct.

- [ ] **NoSQL databases are limited to vertical scaling by adding more resources to a single server.** ❌: `This is incorrect because NoSQL databases are designed to scale horizontally, not just vertically.`
- [ ] **NoSQL databases are not suitable for applications requiring high availability and fault tolerance.** ❌: `This is incorrect because NoSQL databases are designed to provide high availability and fault tolerance.`
- [ ] **NoSQL databases are designed to scale horizontally by adding more servers.** ✅: `This is correct because NoSQL databases are designed to scale horizontally, allowing them to handle large volumes of data by adding more servers.`
- [ ] **NoSQL databases can handle large volumes of unstructured and semi-structured data.** ✅: `This is correct because NoSQL databases are designed to handle large volumes of unstructured and semi-structured data.`

## Q9: Understanding Azure Cosmos DB APIs

> For each of the following statements about Azure Cosmos DB APIs, select if the statement is correct.

- [ ] **The Core (SQL) API is used to store and query graph data.** ❌: `This is incorrect because the Core (SQL) API is used for SQL-like queries to manage JSON documents, not for graph data.`
- [ ] **The Gremlin API is used for key-value storage with a schemaless design.** ❌: `This is incorrect because the Gremlin API is used for graph data, not for key-value storage.`
- [ ] **The MongoDB API is ideal for applications already using MongoDB.** ✅: `This is correct because the MongoDB API provides wire protocol compatibility with MongoDB, making it ideal for applications already using MongoDB.`
- [ ] **The Table API is compatible with Azure Table Storage.** ✅: `This is correct because the Table API provides key-value storage with a schemaless design and is compatible with Azure Table Storage.`

## Q10: Understanding Azure Cosmos DB APIs

> For each of the following statements about Azure Cosmos DB APIs, select if the statement is correct.

- [ ] **The Core (SQL) API is suitable for applications that need to model and traverse complex relationships.** ❌: `This is incorrect because the Core (SQL) API is used for SQL-like queries to manage JSON documents, not for modeling and traversing complex relationships.`
- [ ] **The MongoDB API is not suitable for applications already using MongoDB.** ❌: `This is incorrect because the MongoDB API provides wire protocol compatibility with MongoDB, making it suitable for applications already using MongoDB.`
- [ ] **The Table API provides key-value storage with a schemaless design, suitable for simple, scalable, and cost-effective storage.** ✅: `This is correct because the Table API provides key-value storage with a schemaless design, making it suitable for simple, scalable, and cost-effective storage.`
- [ ] **The Gremlin API is based on Apache TinkerPop and is used to store and query graph data.** ✅: `This is correct because the Gremlin API is based on Apache TinkerPop and is used to store and query graph data.`

<!-- START BADGE -->
<div align="center">
  <img src="https://img.shields.io/badge/Total%20views-1327-limegreen" alt="Total views">
  <p>Refresh Date: 2025-08-04</p>
</div>
<!-- END BADGE -->
