<b>Overview of Distributed Systems</b>
It is always easier to first, build systems on single machine and then move to distributed systems. This is because, in a single machine, we can easily debug and test our system. However, in a distributed system, it is difficult to debug and test the system as it is spread across multiple machines.

<b>Reasons for moving to distributed systems:</b>
1. Scalability: Distributed systems can handle more load by adding more machines to the system.
2. Fault tolerance: Distributed systems can continue to operate even if some machines fail. /
3. Resource sharing: Distributed systems can share resources such as storage and processing power across multiple machines.
4. Geographical distribution: Distributed systems can be deployed across multiple locations, allowing for better performance and availability.
5. Cost efficiency: Distributed systems can be more cost-effective than single machine systems, as they can utilize cheaper hardware and resources.
6. Flexibility: Distributed systems can be designed to support different types of applications and workloads, making them more versatile than single machine systems.
7. Improved performance: Distributed systems can improve performance by distributing the workload across multiple machines, allowing for faster processing and response times.
8. Better reliability: Distributed systems can provide better reliability by replicating data and services across multiple machines, reducing the risk of data loss or service downtime.
9. Enhanced security: Distributed systems can provide enhanced security by implementing security measures across multiple machines, making it more difficult for attackers to compromise the system.
10. Support for large-scale applications: Distributed systems can support large-scale applications that require high availability, scalability, and fault tolerance, making them suitable for modern applications such as cloud computing and big data processing.
11. Parallel processing (Parallelism): Distributed systems can enable parallel processing, allowing for faster execution of tasks by dividing them into smaller sub-tasks that can be processed simultaneously across multiple machines.

<b>Complexity of distributed systems:</b>
1. Communication: Distributed systems require communication between multiple machines, which can introduce latency and complexity in the system.
2. Synchronization: Distributed systems require synchronization between multiple machines, which can be challenging to implement and maintain.
3. Consistency: Distributed systems require consistency between multiple machines, which can be difficult to achieve, especially in the presence of failures or network partitions.
4. Fault tolerance: Distributed systems require fault tolerance mechanisms to handle failures of individual machines or components, which can add complexity to the system.
5. Security: Distributed systems require security mechanisms to protect against unauthorized access and attacks, which can be more complex than in single machine systems.
6. Debugging and testing: Distributed systems can be more difficult to debug and test than single machine systems, as issues may arise from interactions between multiple machines or components, making it harder to isolate and identify the root cause of problems.
7. Resource management: Distributed systems require effective resource management to ensure that resources are allocated efficiently across multiple machines, which can be more complex than in single machine systems.
8. Deployment and maintenance: Distributed systems require careful deployment and maintenance to ensure that all machines are running the correct software versions and configurations, which can be more complex than in single machine systems.
9. Monitoring and logging: Distributed systems require effective monitoring and logging mechanisms to track the performance and behavior of the system across multiple machines, which can be more complex than in single machine systems.
10. Scalability: Distributed systems require careful design and implementation to ensure that they can scale effectively as the number of machines and users increases, which can be more complex than in single machine systems.
11. Interoperability: Distributed systems may need to interact with other systems or services, which can introduce additional complexity in terms of compatibility and integration.
12. Data management: Distributed systems require effective data management strategies to ensure that data is stored, accessed, and updated consistently across multiple machines, which can be more complex than in single machine systems.
13. Network issues: Distributed systems are susceptible to network issues such as latency, bandwidth limitations, and network partitions, which can introduce additional complexity in terms of communication and coordination between machines.
14. Load balancing: Distributed systems require effective load balancing mechanisms to distribute workloads evenly across multiple machines, which can be more complex than in single machine systems.
15. Concurrency: Distributed systems require effective concurrency control mechanisms to manage access to shared resources and prevent conflicts between multiple machines, which can be more complex than in single machine systems.
16. Partial failures: Distributed systems must be designed to handle partial failures, where some machines or components may fail while others continue to operate, which can introduce additional complexity in terms of fault tolerance and recovery mechanisms.
17. Time synchronization: Distributed systems require effective time synchronization mechanisms to ensure that clocks on different machines are synchronized, which can be more complex than in single machine systems.
18. Testing and validation: Distributed systems require effective testing and validation strategies to ensure that the system behaves correctly under various conditions, which can be more complex than in single machine systems.
19. Complexity of algorithms: Distributed systems often require more complex algorithms to handle issues such as consensus, leader election, and distributed transactions, which can be more complex than in single machine systems.
20. Human factors: Distributed systems require effective communication and collaboration between team members, which can be more complex than in single machine systems due to the distributed nature of the system and potential differences in time zones, cultures, and work styles.
21. Debugging and troubleshooting: Distributed systems require effective debugging and troubleshooting strategies to identify and resolve issues that may arise in the system, which can be more complex than in single machine systems due to the distributed nature of the system and potential interactions between multiple machines or components.

Programming Labs
1. Simple MapReduce:
   - MapReduce is a programming model and an associated implementation for processing and generating large data sets with a parallel, distributed algorithm on a cluster.
   - It consists of two main functions: Map and Reduce. The Map function processes input data and produces intermediate key-value pairs, while the Reduce function takes these intermediate key-value pairs and combines them to produce the final output.
   - MapReduce is designed to handle large-scale data processing tasks by distributing the workload across multiple machines in a cluster, allowing for parallel processing and improved performance.
   - It is widely used in big data processing frameworks such as Apache Hadoop and Apache Spark, enabling efficient processing of massive datasets in a distributed manner.
   - Project: Implement a simple MapReduce program to count the occurrences of words in a large text file. The program should read the input file, apply the Map function to generate intermediate key-value pairs for each word, and then use the Reduce function to aggregate the counts and produce the final word count output.
   2. Raft (Managing replcition for fault tolerance):
   - Raft is a consensus algorithm that is designed to manage replication in distributed systems, ensuring fault tolerance and consistency across multiple nodes in a cluster.
   - It provides a way for distributed systems to agree on a single value or state, even in the presence of failures or network partitions.
   - Raft achieves this by electing a leader node that is responsible for coordinating the replication of log entries and ensuring that all follower nodes maintain a consistent state.
   - The algorithm consists of three main components: leader election, log replication, and safety. Leader election ensures that a single leader is chosen among the nodes, log replication ensures that all nodes have the same log entries, and safety guarantees that the system remains consistent even in the presence of failures.
   - Raft is widely used in distributed systems to provide fault tolerance and consistency, making it suitable for applications such as distributed databases, distributed file systems, and distributed key-value stores.
   Project: Implement a simple Raft-based system that manages replication of log entries across multiple nodes in a cluster. The system should handle leader election, log replication, and ensure consistency among the nodes, even in the presence of failures or network partitions.

   3. Build Key-Value server using Raft:
   - A key-value server is a distributed system that stores and retrieves data in the form of key-value pairs. It provides a simple interface for clients to store and retrieve data, making it suitable for applications that require fast and efficient data access.
   - By using Raft as the underlying consensus algorithm, the key-value server can achieve fault tolerance and consistency across multiple nodes in a cluster, ensuring that data is replicated and available even in the presence of failures or network partitions.
   - The key-value server should support basic operations such as put, get, and delete, allowing clients to store, retrieve, and remove key-value pairs from the server. It should also handle leader election, log replication, and ensure consistency among the nodes, providing a reliable and fault-tolerant data storage solution.
   Project: Implement a simple key-value server that uses Raft for replication and fault tolerance. The server should support basic operations such as put, get, and delete, and ensure consistency among the nodes in the cluster, even in the presence of failures or network partitions.

   4. Use the Replicated Key-Value server and clone it to build a distributed file system (Sharded K/V Service):
   - A distributed file system is a system that allows users to store and access files across multiple machines in a network, providing a unified view of the file system and enabling efficient data sharing and collaboration.
   - By using the replicated key-value server as the underlying storage layer, the distributed file system can achieve fault tolerance and consistency, ensuring that files are replicated and available even in the presence of failures or network partitions.
   - The distributed file system should support basic file operations such as create, read, write, and delete, allowing users to manage files across the distributed system. It should also handle leader election, log replication, and ensure consistency among the nodes, providing a reliable and fault-tolerant file storage solution.
   Project: Implement a simple distributed file system that uses the replicated key-value server for storage and fault tolerance. The file system should support basic file operations such as create, read, write, and delete, and ensure consistency among the nodes in the cluster, even in the presence of failures or network partitions.

Key Focus Areas:
Infrastructure Abstraction for Storage, Communication, and Computation. Implementations using tools like RPC, threads, concurrency controls

Performance. Achieving scalability and high throughput. 2x computers  -> 2x throughput. 

Fault Tolerance. Handling failures and ensuring system reliability. The ability to continue operating correctly even in the presence of failures. There are various ways to perceive fault tolerance, such as availability, recoverability.

Consistency. Ensuring that all nodes in the distributed system have a consistent view of the data. This can be achieved through various consistency models, such as eventual consistency, strong consistency, and causal consistency. Put(key, value) -> Get(key) = value.
Get(key) -> Value. If a node fails, the system should be able to recover and ensure that all nodes have a consistent view of the data.
Strong consistency ensures that all nodes see the same data at the same time, while eventual consistency allows for temporary inconsistencies that will eventually be resolved. Causal consistency ensures that operations that are causally related are seen in the same order by all nodes.
Weak consistency models may allow for temporary inconsistencies, but they can provide better performance and availability in certain scenarios. The choice of consistency model depends on the specific requirements of the distributed system and the trade-offs between consistency, availability, and performance.
Practically, Strong vs Weak consistency is a tradeoff between performance and availability. Strong consistency may require more coordination and communication between nodes, which can impact performance, while weak consistency may allow for better performance but may sacrifice availability in certain scenarios. The choice of consistency model should be based on the specific requirements of the distributed system and the trade-offs between consistency, availability, and performance.

There are research into how to structure weak consistency guarantees so they are actually useful in terms of high performance to applications. For example, causal consistency is a weak consistency model that provides useful guarantees for certain types of applications, such as collaborative editing and social networking. By ensuring that operations that are causally related are seen in the same order by all nodes, causal consistency can help prevent conflicts and ensure that users have a consistent view of the data.

MapReduce is a programming model that allows for parallel processing of large data sets across multiple machines in a distributed system. It consists of two main functions: Map and Reduce. The Map function processes input data and produces intermediate key-value pairs, while the Reduce function takes these intermediate key-value pairs and combines them to produce the final output.

References:
- [MapReduce: Simplified Data Processing on Large Clusters](https://storage.googleapis.com/gweb-research2023-media/pubtools/4449.pdf)