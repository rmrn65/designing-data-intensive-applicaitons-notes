# Scalability

## Introduction

**Scalability** = How can we add more resources to handle additional load

## What is Load ?

Load parameter is the work unit of the system. (requests, messages, writes)

The amount of work or pressure on a system. E.g.: Amount of requests, messages, writes;

## What is performance ?

- When the load parameter is increase, how much should resources need to be increased?
- One metric to calculate performance is **latency**.
  - More specifically: **median latency** used to exclude outliers
    - For understanding how bad outliers are, use *p95* or *p99*
- Statement about how to decide architectural decisions on performance:

>An architecture that scales well for a particular application is built around assumptions of which operations will be common and which will be rare

## Keywords

- SLO (Service level objectives)
- SLA (Service level agreements) = p50 is 200ms and p99 is 1s
