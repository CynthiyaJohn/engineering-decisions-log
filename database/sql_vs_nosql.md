# SQL vs NoSQL Databases

## Context
Applications must choose a data storage model that supports their consistency,
scalability, and query requirements.

## Options Considered

### SQL Databases
Relational databases with fixed schemas and strong consistency guarantees.

### NoSQL Databases
Schema-flexible databases optimized for scalability and high-throughput workloads.

## Decision
SQL databases are chosen when data integrity and complex relationships are critical,
while NoSQL databases are selected for flexible schemas and horizontal scalability.

## Trade-offs

### SQL – Pros
- Strong consistency and ACID guarantees
- Rich querying capabilities
- Mature tooling and ecosystem

### SQL – Cons
- Vertical scaling limitations
- Schema changes can be costly
- Performance bottlenecks under massive scale

### NoSQL – Pros
- Horizontal scalability
- Flexible or schema-less design
- High availability for distributed systems

### NoSQL – Cons
- Eventual consistency in many systems
- Limited support for complex joins
- Data modeling complexity shifts to the application

## When This Decision Fails
- Using NoSQL for highly relational data
- Using SQL in write-heavy, globally distributed systems without sharding strategies

