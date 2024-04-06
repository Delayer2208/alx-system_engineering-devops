# Simple Web Stack

![Image of a simple web stack](Images/0-simple_web_stack.PNG)

## Description

This is a simple web infrastructure that hosts a website reachable via `www.foobar.com`. It comprises a single server with a LAMP stack (Linux, Apache, MySQL, PHP/Perl/Python). However, there are no firewalls or SSL certificates for protecting the server's network. Each component (database, application server) shares the resources (CPU, RAM, and SSD) provided by the server.

## Specifics About This Infrastructure

- **What is a server?**  
A server is a computer hardware or software that provides services to other computers, usually referred to as clients.

- **The role of the domain name:**  
A domain name provides a human-friendly alias for an IP Address, making it easier to recognize and remember. For example, `www.wikipedia.org` is easier to remember than `91.198.174.192`.

- **Type of DNS record for `www.foobar.com`:**  
`www.foobar.com` uses an A record, which maps the domain name to an IPv4 address.

- **Role of the web server:**  
The web server accepts requests via HTTP or HTTPS and responds with the content of the requested resource or an error message.

- **Role of the application server:**  
The application server hosts and manages applications and associated services for end users and organizations.

- **Role of the database:**  
The database maintains a collection of organized information that can be easily accessed, managed, and updated.

- **Communication between server and client:**  
Communication occurs over the internet network through the TCP/IP protocol suite.

## Issues With This Infrastructure

- **Single Point Of Failure (SPOF):**  
Multiple SPOFs exist in this infrastructure. For example, if the MySQL database server is down, the entire site would be unavailable.

- **Downtime during maintenance:**  
Maintenance checks on any component require downtime or server shutdown. Since there's only one server, the website experiences downtime during maintenance.

- **Scalability issues:**  
The infrastructure cannot scale effectively to handle increased traffic. With only one server containing all components, resource limitations may lead to performance degradation or downtime during peak traffic.
