# System Design

## How to design large-scale systems - suggested process

1. <b>Clarify the goals</b> and understand the basic requirements;
2. <b>Determine the scope</b>;
3. <b>Design for the right scale</b> and determine the scale so you know whether the data can be supported by a single machine or if you need to scale;
4. <b>Start simple, then iterate</b>, but don't forget to discuss potential botlenecks;
5. <b>Consider relevant DSA</b> and determine which fundamental data structures and algorithms will help your system perform efficiently and appropriately;
6. <b>Describe trade-offs</b>.

## Distributed systems fundamentals

- <b>Data durability and consistency:</b> the differences and impacts of failures rates of storage solutions and corruption rates in read-write processes.
- <b>Replication:</b> backing up data and repeating processes at scale.
- <b>Consensus:</b> ensuring all nodes are in agreement, which prevents fault processes from running and ensures consistency and replication of data and processes.
- <b>Partitioning:</b> dividing data across different nodes within systems, which reduces reliance on pure replication.
- <b>Distributed transactions:</b> once consensus is reachded, transactions from applications need to be committed across databases with fault checks by each resource involved.

## Architecture of scalable web applications

- <b>HTTP:</b> the API on which the entire internet runs.
- <b>REST:</b> t.e set of design principles that directly interact with HTTP to enable system efficiency and scalability;
- <b>DNS and load balancing:</b> routing client requests to the right servers and the right tiers when processing happens to ensure the system stability.
- <b>Caching:</b> making tradeoffs and caching decisions to determine what should be stored in a cache, how to direct traffic to a cache, and how to ensure we have the appropriate data in cache.
- <b>N-tier applications:</b> understanding how processing tiers interact with each other and the specific process they control.
- <b>Stream processing:</b> applying uniform processes to data streams to allow for efficient use of local resources.

***

### Horizontal scaling vs. Vertical scaling

| Scaling Type | Description |
|---|------|
|Horizontal | Increase in number of machines. <br> <br> More instances of servers are added to the existing pool and the traffic load is distributed across these devices in efficient manner.|
|Vertical| Increase in processing power. <br> <br> Refers to the concept of upgrading the resource capacity such as increasing RAM, or adding efficient processors (among others) of a single machine or switching to a new machine with more capacity. The capability of the server can be enhanced without the need for code manipulation. |

### Load balancing

**Load balancing** consists in distributing incoming traffic efficiently across a group of various backend servers (server pools).

Nowadays, most websites are designed to serve millions of requests from clients and return the responses in a fast and reliable manner. In order to serve these requests, the addition of more servers is required (horizontal scaling).

The previous scenario makes it essential to distribute request traffic efficiently across each server so that they don't face undue loads. As such, the **load balancer** acts a traffic police facing the requests and routing them across the available servers in a way that not a single server is overwhelmed, which could possibly degrade the application performance.

### Sharding

It is the process of splitting the large logical dataset into multiple databases. It also refers to horizontal partitioning of data as it will be stored on multiple machines. By doing so, a sharded database becomes capable of handling more requests than a single large machine.

***

<br>

### Exercise: how to design a Library Management System?

WIP.

See link at the end of the page.

***

<br>

### Main sources and links:

- https://faun.pub/top-30-system-design-interview-questions-and-problems-for-programmers-417e89eadd67
- How do you design an Amazon clone: https://youtu.be/b67C1Ou9b1Y
- How do you design a StackOverFlow clone: https://youtu.be/k4xr-UHfWtM
- How do you design a movie ticket system: https://youtu.be/lBAwJgoO3Ek
- How to design a library management system: https://www.educative.io/courses/grokking-the-object-oriented-design-interview/RMlM3NgjAyR?affiliate_id=5073518643380224
