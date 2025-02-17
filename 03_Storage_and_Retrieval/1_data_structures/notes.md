# Data Structures That Power Your Database

## Introduction

How can one find values for particular keys efficiently? Indexes.

##  Hash indexes

Considering a file-storage:

- Hash indexes are a dictionary type of index
- Proficient for multiple writes on a key. (plays or clicks on a video)
- How to avoid running out of disk? Re: **compaction** = throw away duplicate tokens

### Implementation challenges

- File format - for logs, binary > CSV
- Record deletion - deletion must cascade for all items with the mentioned hash-key
- Crash recovery - snapshots or backing up is needed
- Partially written records - checksums are needed
- Concurrency control - One thread needs to write at a time

### Drawbacks

- Hash indexes must be held in-memory
- On disk hash indexes require a lot of I/O operation → adds latency
- Repetitive keys leads to high complexity queries

## SSTables and LSM-Trees

- SSTables = Sorted String Tables
- LSM = Log-Structured Merge
- SSTables are sorted by key
- LSM-Trees are a collection of SSTables
- SSTables are immutable
- LSM-Trees are used in Cassandra, HBase, LevelDB, RocksDB
- LSM-Trees are used for Elasticsearch
- Log structured storage with high efficiency for writes

More: https://www.youtube.com/watch?v=I6jB0nM9SKU

## B-Trees
- Break entries in equal sized segments [blocks]
- It's a tree of references ordered by key. The search is O(log n)
- "The number of references to child pages in one page of the B-tree is called the branching factor"
