# Secured and Monitored Web Infrastructure

![Image of a secured and monitored infrastructure](Images/2-secured_and_monitored_web_infrastructure.PNG)

## Description

This is a 3-server web infrastructure that is secured, monitored, and serves encrypted traffic.

## Specifics About This Infrastructure

- **Purpose of Firewalls:**  
Firewalls are implemented to protect the web servers from unauthorized access and potential threats originating from the external network. They act as a barrier between the internal network and the internet, filtering incoming and outgoing traffic based on predefined security rules.

- **Purpose of SSL Certificate:**  
SSL certificates are utilized to encrypt the traffic between the web servers and external network, ensuring data privacy, integrity, and authentication. By encrypting the communication, SSL certificates prevent eavesdropping and tampering of sensitive information exchanged between the servers and clients.

- **Purpose of Monitoring Clients:**  
Monitoring clients are deployed to continuously monitor the health and performance of the servers and network infrastructure. They collect and analyze various metrics such as CPU usage, memory utilization, network traffic, and server uptime. Monitoring tools generate alerts and notifications to administrators in case of abnormal behavior or performance degradation, enabling proactive troubleshooting and maintenance.

## Issues With This Infrastructure

- **Terminating SSL at the Load Balancer Level:**  
Terminating SSL at the load balancer level could expose the communication between the load balancer and web servers to potential security risks, as the traffic between them would remain unencrypted. It's crucial to ensure end-to-end encryption to maintain data security and privacy.

- **Single MySQL Server as a Potential Single Point of Failure:**  
Relying on a single MySQL server poses scalability and reliability concerns. In the event of hardware failure or high traffic load, the MySQL server may become overwhelmed or unavailable, causing downtime and data loss. Implementing a redundant and scalable database solution, such as clustering or replication, can mitigate this risk.

- **Uniform Server Components and Resource Contention:**  
Deploying servers with identical components may lead to resource contention and performance bottlenecks. Components such as CPU, memory, and I/O resources may be overutilized, affecting the overall performance and scalability of the infrastructure. Adopting a diversified approach to server configuration and resource allocation can improve resource utilization and scalability.

