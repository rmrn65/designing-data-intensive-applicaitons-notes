# Leaders and Followers

## Introduction

- Each database has a replica. The question is: how do we keep the replicas in sync?
- The strategy is called **leader-based replication** = request is first processed by the leader, then sent to the followers.
- Reads can be done from any replica, but writes are only done on the leader.

## Synchronous vs Asynchronous Replication

- **Synchronous replication** = leader waits for ack; only ONE replica can communicate synchronously with the leader.
- **Semi-synchronous replication** = leader waits for ack from at least one replica; the rest of the replicas can communicate asynchronously.
- **Asynchronous replication** = \[Most often\] leader doesn't wait for ack; all replicas communicate asynchronously.

### Setting up followers

- Create snapshot of leader (this is also useful for backups)
- Create replica based on snapshot
- Replica connects to leader and requests missing data

### Node Outage Handling

- **Followers Failover** = once the follower is back-up, it can catch up with the leader.
- **Leader Failover** = the leader is down, a new leader is elected from the followers - this implies a lot of issues 
because of the async communication

### Replication Logs

Non-deterministic methods differ between leader and followers (e.g. auto-incrementation for columns).
Solution: leader replaces non-deterministic methods with fixed return value ones when statement is **logged**

There are built-in logging systems in databases that can be used for building replicas:
- Write-ahead log (WAL) shipping
- Logical (row-based) log replication
- Trigger-based replication
