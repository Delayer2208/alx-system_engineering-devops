# Distributed Web Infrastructure

![Image of a distributed web infrastructure](Images/1-distributed_web_infrastructure.PNG)

[Visit Board](https://miro.com/app/board/uXjVOfI6jcU=/)

## Description

This is a distributed web infrastructure that attempts to reduce the traffic to the primary server by distributing some of the load to a replica server with the aid of a load balancer.

## Specifics About This Infrastructure

- **Distribution Algorithm of the Load Balancer:**  
The HAProxy load balancer is configured with the Round Robin distribution algorithm. This algorithm distributes incoming requests equally among the servers behind the load balancer, ensuring fair utilization of resources.

- **Setup Enabled by the Load Balancer:**  
The HAProxy load balancer enables an Active-Passive setup. In this configuration, one server (Primary) actively handles incoming requests while the other server (Replica) remains on standby. The Replica server becomes active only if the Primary server fails, ensuring high availability and fault tolerance.

- **How a Database Primary-Replica (Master-Slave) Cluster Works:**  
In a Primary-Replica setup, one server serves as the Primary node, handling both read and write operations, while the other server serves as the Replica node, handling only read operations. Data synchronization occurs from the Primary node to the Replica node, ensuring consistency and redundancy.

- **Difference Between the Primary and Replica Nodes in Regard to the Application:**  
The Primary node is responsible for processing both read and write operations, making it the primary point of interaction for the application. The Replica node primarily handles read operations, offloading some of the read traffic from the Primary node.

## Issues With This Infrastructure

- **Single Point Of Failure (SPOF):**  
Several components in this infrastructure present single points of failure. For instance, if the Primary MySQL database server or the server containing the load balancer fails, the availability and functionality of the entire site could be impacted.

- **Security Issues:**  
The absence of SSL encryption for network traffic exposes data to potential interception by malicious actors. Additionally, the lack of a firewall leaves the infrastructure vulnerable to unauthorized access and attacks.

- **No Monitoring:**  
The absence of monitoring tools means there's no visibility into the health and performance of the servers. Monitoring is essential for detecting issues proactively and ensuring the reliability of the infrastructure.

