# Relational Model Versus Document Model

## SQL

- Relational Database Model
- To interact with them, we use RDBM-ses. (e.g. PostgreSQL, MySQL, MicrosoftSQL)
- Suitable for structured data with predefined schema
- Requires vertical scaling for big loads of data
- Restrictive and might need expertise

## NoSQL

- Non-Relational Model
- Horizontally scalable
- Dynamic but more error-prone
- Suitable for non-structured data
- Are good for file-structured application (e.g. WordPress)
- Not efficient with joins (many-to-many operations)

## ORM

- An interface between code and db (e.g. Hibernate) used to reduce boilerplate code
- JSON reduces impedance mismatch between code and data layer.
  - JSON also helps with avoiding multiple joins for extracting all data relevant to one component wit multiple dependencies

## Many-to-One Many-to-Many

- Auto-generated IDs, or primary keys are a must because relevant information changes over time
- A DB is **normalized** if it follows *normal forms*. This ensures that there is no data redundancy (e.g. duplicated values), and there is strong data integrity (e.g. data is structured and stored exactly as intended)
- Normalizing data requires Many-to-One relationships

## Relational vs Document Database

- Document databases (schemaless) have no predefined structure - users can expect both attributes and values to be undefined
  - More proper name: schema-on-read - the structure of data is implicit
  - Data and Data structure needs to be checked or validated
  - Allows for flexibility on filtering on dynamic schemas - doesn't need migration
  - Advantageous if there are too many types of objects, or if objects are coming from external services you have no control over

- Relational databases support schemaless structures - PostgreSQL and MySQL support JSON type columns 

## Keywords

- Query optimizers
