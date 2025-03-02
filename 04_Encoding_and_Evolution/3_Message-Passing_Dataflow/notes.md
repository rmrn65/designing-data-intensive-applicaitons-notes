# Message-Passing Dataflow

## Message Brokers
- Message brokers are used to send messages between processes. Messages is a sequence of bytes with data of any format
- Message brokers advantages:
  - act like buffers
  - retry mechanism through resending messages
  - works in a publish-subscribe model
  - messages can be broadcast
  - decouples producers and consumers

## Distributed actor frameworks
- Actors:
  - independent lightweight processes
  - receive messages through mailboxes
  - can send messages to other actors based on their address
- Distributed actor frameworks - scale across multiple nodes; messages are encoded by the sender and decoded by the receiver
- Location transparency - actors can be moved to different nodes without changing the code
- Advantages:
  - fault tolerance - also self-healing
  - scalability - actors are lightweight
  - location transparency
  - no shared state
- Disadvantages:
  - debugging is hard
  - deadlocks can occur
  - overflowing mailboxes
