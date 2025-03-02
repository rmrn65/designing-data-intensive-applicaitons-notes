# Modes of Dataflow

## Introduction
- "_In a database, the process that writes to the database encodes the data, and the process that reads from the database decodes it_"

## Dataflow over a network connection

- Web Services are services that use HTTP as the transport layer.
- Web Services use REST or SOAP as the communication protocol.
  - REST uses: simple data formats (e.g. JSON, XML), HTTP methods for commands (GET, POST, PUT, DELETE) and URLs for identifying resources.
  - SOAP uses: XML for encoding data, HTTP or SMTP for transport, and WSDL for describing the interface.
- RPC (Remote Procedure Call):
  - Function calls that look like local calls but are executed on a remote machine.
  - Challenges: Network communication is a challenge in RPC because of the network's unreliability.
  - Advantages: Supports asynchronous mode, with promises or futures. Supports streaming requests and responses.
  - In RPC, the client and server can change independently - can lead to versioning issues.


## Keywords
- WSDL - Web Services Description Language -  XML format for describing network services as a set of endpoints operating 
on messages containing either document-oriented or procedure-oriented information.
- 
