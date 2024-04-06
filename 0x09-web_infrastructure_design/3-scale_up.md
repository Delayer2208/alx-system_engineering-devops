# Scaled Up Web Infrastructure

![Image of a scaled up web infrastructure](3-scale_up.png)

## Description

This web infrastructure is a scaled-up version of the infrastructure described [here](2-secured_and_monitored_web_infrastructure.md). In this version, all single points of failure (SPOFs) have been eliminated, and each major component (web server, application server, and database servers) has been moved to separate GNU/Linux servers. Additionally, SSL protection isn't terminated at the load balancer, and each server's network is protected with a firewall, and they are also monitored.

## Specifics About This Infrastructure

- **Addition of Firewall Between Each Server:**  
A firewall has been installed between each server to protect them from unwanted and unauthorized access attempts. By implementing individual firewalls for each server, the security posture of the entire infrastructure is enhanced, and the risk of unauthorized access and malicious attacks is mitigated.

## Issues With This Infrastructure

- **High Maintenance Costs:**  
While removing single points of failure and increasing security, the scaled-up infrastructure also introduces higher maintenance costs. With each major component hosted on separate servers, the company incurs additional expenses for purchasing, maintaining, and powering these servers. This increase in operational costs may strain the company's budget and require careful consideration of resource allocation.
