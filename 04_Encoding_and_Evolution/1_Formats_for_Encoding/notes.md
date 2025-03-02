# Formats for encoding data

## Introduction

On a schemaless database, the format of the data is not predefined (e.g. logging apps/ user interaction monitoring)
Reading and interpreting the data is done using code, but if the code is not backwards compatible with the data changing
it can lead to data loss.

- Programs work with data that is either in memory or sent over the network.
- The data send over the network is encoded (e.b. JSON).
- Encoding = translation of data from in-memory to byte sequence

## Language-specific formats
- Each programming language has its own serialization format & libraries
- Downside: not all languages can read all formats
- Upside: minimal additional code to read/write data, convenient

## Standardized encodings
- JSON, XML, CSV - main formats
- Advantages: human-readable, widely supported
- Disadvantages: not space-efficient, not always easy to read/write, don't support for all data types
- Encoding binary takes less space, but is not human-readable

## Avro
- Avro is another binary encoding format
- Avro schema = JSON document that defines the structure of the data
- Advantages: schema stored with the data, data read without the schema, schema evolution supported, type-safe
- Disadvantages: not human-readable, not space-efficient
 
## Keywords

- Backward compatibility - Newer code can read data that was written by older code. - easier to achieve
- Forward compatibility - Older code can read data that was written by newer code. - tricky to achieve
- Schema evolution - changing the schema of the data
