# Non-Relational Data on Azure: Sample Questions and Answers 

Costa Rica

[![GitHub](https://img.shields.io/badge/--181717?logo=github&logoColor=ffffff)](https://github.com/)
[brown9804](https://github.com/brown9804)

Last updated: 2025-01-16

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

</details>

> [!TIP]
> Cosmos APIs:

| Cosmos API        | Description                                                                 |
|------------|-----------------------------------------------------------------------------|
| Core (SQL) | A native API for Azure Cosmos DB that supports SQL-like queries to manage JSON documents. Ideal for applications requiring rich querying capabilities and transactional consistency. |
| Gremlin    | A graph database API based on Apache TinkerPop, used to store and query graph data with vertices and edges. Suitable for applications that need to model and traverse complex relationships. |
| MongoDB    | An API that provides wire protocol compatibility with MongoDB, allowing you to use existing MongoDB drivers and tools. Ideal for applications already using MongoDB. |
| Table      | An API that provides key-value storage with a schemaless design, compatible with Azure Table Storage. Suitable for applications that need a simple, scalable, and cost-effective storage solution. |


## Q: Understanding Azure Cosmos DB APIs

> For each of the following statements about Azure Cosmos DB APIs, select if the statement is correct.

- [ ] **The Table API is used for complex relational queries.** ❌: `This is incorrect because the Table API provides key-value storage with a schemaless design, not for complex relational queries.`
- [ ] **The Core (SQL) API supports SQL-like queries to manage JSON documents.** ✅: `This is correct because the Core (SQL) API supports SQL-like queries to manage JSON documents.`
- [ ] **The Gremlin API is used to store and query graph data with vertices and edges.** ✅: `This is correct because the Gremlin API is based on Apache TinkerPop and is used to store and query graph data with vertices and edges.`
- [ ] **The MongoDB API provides wire protocol compatibility with MongoDB.** ✅: `This is correct because the MongoDB API provides wire protocol compatibility with MongoDB, allowing you to use existing MongoDB drivers and tools.`

## Q: Understanding Azure Cosmos DB APIs

> For each of the following statements about Azure Cosmos DB APIs, select if the statement is correct.

- [ ] **The MongoDB API is not compatible with existing MongoDB drivers and tools.** ❌: `This is incorrect because the MongoDB API provides wire protocol compatibility with MongoDB, allowing the use of existing MongoDB drivers and tools.`
- [ ] **The Core (SQL) API is ideal for applications requiring rich querying capabilities and transactional consistency.** ✅: `This is correct because the Core (SQL) API supports SQL-like queries and provides transactional consistency, making it ideal for such applications.`
- [ ] **The Gremlin API is suitable for applications that need to model and traverse complex relationships.** ✅: `This is correct because the Gremlin API is designed for graph data, which is used to model and traverse complex relationships.`
- [ ] **The Table API is suitable for applications that need a simple, scalable, and cost-effective storage solution.** ✅: `This is correct because the Table API provides key-value storage with a schemaless design, making it suitable for simple, scalable, and cost-effective storage.`

## Q: Understanding Azure Cosmos DB APIs

> For each of the following statements about Azure Cosmos DB APIs, select if the statement is correct.

- [ ] **The Core (SQL) API is based on Apache TinkerPop.** ❌: `This is incorrect because the Core (SQL) API is not based on Apache TinkerPop; the Gremlin API is.`
- [ ] **The Gremlin API supports SQL-like queries to manage JSON documents.** ❌: `This is incorrect because the Gremlin API is used for graph data, not for SQL-like queries to manage JSON documents.`
- [ ] **The MongoDB API allows you to use existing MongoDB drivers and tools.** ✅: `This is correct because the MongoDB API provides wire protocol compatibility with MongoDB, allowing the use of existing MongoDB drivers and tools.`
- [ ] **The Table API provides key-value storage with a schemaless design.** ✅: `This is correct because the Table API provides key-value storage with a schemaless design.`

## Q: Understanding Azure Cosmos DB APIs

> For each of the following statements about Azure Cosmos DB APIs, select if the statement is correct.

- [ ] **The Core (SQL) API is used to store and query graph data.** ❌: `This is incorrect because the Core (SQL) API is used for SQL-like queries to manage JSON documents, not for graph data.`
- [ ] **The Gremlin API is used for key-value storage with a schemaless design.** ❌: `This is incorrect because the Gremlin API is used for graph data, not for key-value storage.`
- [ ] **The MongoDB API is ideal for applications already using MongoDB.** ✅: `This is correct because the MongoDB API provides wire protocol compatibility with MongoDB, making it ideal for applications already using MongoDB.`
- [ ] **The Table API is compatible with Azure Table Storage.** ✅: `This is correct because the Table API provides key-value storage with a schemaless design and is compatible with Azure Table Storage.`

## Q: Understanding Azure Cosmos DB APIs

> For each of the following statements about Azure Cosmos DB APIs, select if the statement is correct.

- [ ] **The Core (SQL) API is suitable for applications that need to model and traverse complex relationships.** ❌: `This is incorrect because the Core (SQL) API is used for SQL-like queries to manage JSON documents, not for modeling and traversing complex relationships.`
- [ ] **The MongoDB API is not suitable for applications already using MongoDB.** ❌: `This is incorrect because the MongoDB API provides wire protocol compatibility with MongoDB, making it suitable for applications already using MongoDB.`
- [ ] **The Table API provides key-value storage with a schemaless design, suitable for simple, scalable, and cost-effective storage.** ✅: `This is correct because the Table API provides key-value storage with a schemaless design, making it suitable for simple, scalable, and cost-effective storage.`
- [ ] **The Gremlin API is based on Apache TinkerPop and is used to store and query graph data.** ✅: `This is correct because the Gremlin API is based on Apache TinkerPop and is used to store and query graph data.`


<div align="center">
  <h3 style="color: #4CAF50;">Total Visitors</h3>
  <img src="https://profile-counter.glitch.me/brown9804/count.svg" alt="Visitor Count" style="border: 2px solid #4CAF50; border-radius: 5px; padding: 5px;"/>
</div>
