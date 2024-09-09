# Web Infrastructure Design

## Overview
This project covers designing and understanding web infrastructure components at various levels of complexity. You will explore how to design simple, distributed, secured, and scalable web infrastructures, ensuring redundancy, security, and monitoring capabilities.

The project focuses on key infrastructure concepts such as servers, web servers, DNS, load balancers, and monitoring tools.

## Concepts Covered
This project involves the following concepts:
- **Network Basics**
- **Server**
- **Web Server**
- **DNS**
- **Load Balancer**
- **Monitoring**

### Key Resources
To get started, make sure to review the following resources:
- [Network Basics](https://example.com)
- [Server](https://example.com)
- [Web Server](https://example.com)
- [DNS](https://example.com)
- [Load Balancer](https://example.com)
- [Monitoring](https://example.com)
- [What is a Database?](https://example.com)
- [Difference between Web Server and App Server](https://example.com)
- [DNS Record Types](https://example.com)
- [Single Point of Failure (SPOF)](https://example.com)
- [How to Avoid Downtime during Deployment](https://example.com)
- [High Availability Cluster](https://example.com)
- [What is HTTPS?](https://example.com)
- [What is a Firewall?](https://example.com)

## Learning Objectives
By the end of this project, you will be able to:
- Design and draw diagrams of the web stack infrastructure you build.
- Explain the roles and interactions of each infrastructure component.
- Understand and explain system redundancy and identify Single Points of Failure (SPOF).
- Explain common acronyms: LAMP, SPOF, QPS.

## Project Requirements
- You must include a `README.md` file in the root directory of the project.
- For each task, after whiteboarding the infrastructure (using a whiteboard, paper, or software), take a screenshot of your diagram.
- All tasks will be manually reviewed.

## Tasks

### 0. Simple Web Stack
Design a basic web infrastructure with the following components:
- **1 server** with IP: `8.8.8.8`
- **1 web server** (Nginx)
- **1 application server**
- **1 database** (MySQL)
- **1 domain**: `foobar.com` with a `www` record pointing to the server's IP.

#### You should be able to explain:
- What is a server?
- What is a domain name and its role?
- What type of DNS record is `www` in `www.foobar.com`?
- The roles of the web server, application server, and database.
- How the server communicates with the client.
- Infrastructure issues: SPOF, downtime during maintenance, scalability issues.

### 1. Distributed Web Infrastructure
Expand the infrastructure to include:
- **3 servers**: 1 load balancer (HAproxy), 1 web server (Nginx), 1 application server.
- **1 MySQL database**.

#### You should be able to explain:
- The reason for each additional component.
- Load balancing algorithm and Active-Active vs. Active-Passive setups.
- The difference between a primary and replica database in a master-slave setup.
- Issues: SPOF, security (no firewall, no HTTPS), and lack of monitoring.

### 2. Secured and Monitored Web Infrastructure
Design a secured infrastructure:
- **3 servers** with firewalls.
- **SSL certificate** for HTTPS traffic.
- **Monitoring clients** for logging and tracking (e.g., Sumologic).

#### You should be able to explain:
- Why firewalls are needed.
- The importance of HTTPS for secure traffic.
- How monitoring tools collect data and measure web server QPS.
- Infrastructure issues: SSL termination at the load balancer, single writable MySQL instance, identical server components.

### 3. Scale Up
Add additional infrastructure for scalability:
- **1 additional server** with a load balancer (HAproxy) clustered with the existing one.
- Split web server, application server, and database onto separate servers.
