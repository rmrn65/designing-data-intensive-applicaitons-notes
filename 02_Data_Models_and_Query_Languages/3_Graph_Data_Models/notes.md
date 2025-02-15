# Graph-Like Data Models

## Introduction

Graphs used in representing data are composed of vertices and edges, where the vertices are entities and edges are relationships. (e.g. webpages over network)

Vertex:

- Unique ID
- Properties
- Incoming and outgoing edges

Edge:

- Unique ID
- Starting and ending edge
- Label
- Properties

Graphs data models are useful for their flexibility.

## Graph queries in SQL

Can be done using aliases for vertices and edges, combined with JSONB columns.
Queries are too long and overcomplicated compared to a language like Cypher.

## Triple-Stores

- Is equivalent of property graph model
- The structure includes: subject - verb - attribute
- The semantic web makes data understandable to machines by defining data relationships, meanings, and intent;
