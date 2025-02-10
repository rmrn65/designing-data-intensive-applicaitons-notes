# Reliability

## Introduction - Functionalities of a data intensive application

Basic characteristics of data intensive applications:

- **Persistence** = save data that can be used later
- **Cache** = results of expensive operations
- **Search indexes** = filtering by keywords
- **Stream processing** = series of asynchronous messages
- **Batch processing** = process a large amount of data

## What is Reliability?

### **What does it mean to be reliable?**

Application does what is supposed to in the way it was supposed to function.

### **How is an application reliable?**

Tolerates user mistakes, has a good performance. Can be calculated as "how much time it operates without manual intervention?".

### Types of errors

| Error | Solution |
|----------|----------|
| Hardware | avoided by adding redundancy   |
| Software | thorough testing & process isolation   |
| Human    |  well-designed abstractions and interfaces, decoupling  |

## Keywords

- MTTF - Mean time to failure - how much it takes for a system to fail
- RAID configuration
