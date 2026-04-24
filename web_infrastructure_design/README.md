# Web Infrastructure Design

This project is part of the SysAdmin/DevOps track. The goal is to design and explain various web infrastructures, starting from a simple one-server setup and scaling up to a secured, monitored, and high-availability cluster.

## Learning Objectives
At the end of this project, I am able to explain:
* What a server is.
* The role of a domain name and DNS record types (A, CNAME, etc.).
* The role of web servers (Nginx), application servers, and databases (MySQL).
* System redundancy and High Availability (Active-Active vs Active-Passive).
* Single Point of Failure (SPOF) and how to avoid it.
* The importance of HTTPS, Firewalls, and Monitoring.

---

## Tasks Summary

### [Task 0: Simple Web Stack](./web_infrastructure_design/0-simple_web_stack)
A basic one-server infrastructure (LAMP stack) hosting `www.foobar.com`.
* **Components:** 1 Server, Nginx, App Server, MySQL.
* **Issues:** SPOF, downtime during maintenance, no scalability.
* **Diagram:** [View Diagram](https://imgur.com/a/IFyMLG8) (Example Link)

### [Task 1: Distributed Web Infrastructure](./web_infrastructure_design/1-distributed_web_infrastructure)
A three-server infrastructure to improve redundancy.
* **Components:** Load Balancer (HAProxy), 2 Web/App Servers, Master-Slave Database Cluster.
* **Concepts:** Round Robin algorithm, Primary-Replica replication.
* **Issues:** LB is a SPOF, no security (Firewall/HTTPS), no monitoring.
* **Diagram:** [View Diagram]https://imgur.com/a/cIiM57V

### [Task 2: Secured and Monitored Web Infrastructure](./web_infrastructure_design/2-secured_and_monitored_web_infrastructure)
A secured infrastructure with encryption and health checks.
* **Components:** 3 Firewalls, SSL Certificate (HTTPS), 3 Monitoring clients (Sumo Logic).
* **Concepts:** SSL Termination, Network filtering, QPS monitoring.
* **Issues:** SSL termination risk, single Primary DB for writes.
* **Diagram:** [View Diagram]https://imgur.com/a/Hh9e4Pn

### [Task 3: Scale Up](./web_infrastructure_design/3-scale_up)
A high-availability, decoupled infrastructure with clustered load balancers.
* **Components:** 2 Clustered Load Balancers, Separate Web/App/Database tiers.
* **Concepts:** Failover (Keepalived), Service decoupling, Horizontal scaling.
* **Diagram:** [View Diagram]https://imgur.com/a/mXGl2ap


---

## Acronyms Used
* **LAMP:** Linux, Apache/Nginx, MySQL, PHP/Python/Perl.
* **SPOF:** Single Point of Failure.
* **QPS:** Queries Per Second.
* **HTTPS:** HyperText Transfer Protocol Secure.
* **SSL/TLS:** Secure Sockets Layer / Transport Layer Security.

## Author
* **Name:** Ilgar Hasanof
* **GitHub:** hasanoffh
