# VProfile Project — Local Setup Documentation

## 📌 Overview

The VProfile Project is a multi-tier web application setup designed to simulate a real-world production environment locally using virtual machines.

This project establishes a strong foundation for future DevOps practices such as:
- CI/CD pipelines
- Containerization (Docker)
- Kubernetes deployment
- Infrastructure as Code (IaC)

---

## 🎯 Objectives

- Understand multi-tier architecture
- Learn how different services interact
- Perform manual provisioning of services
- Transition from manual setup to automation
- Build confidence in handling real-world systems

---

## 🏗️ Architecture Overview

The application follows a multi-tier architecture consisting of:

- **Nginx** → Load Balancer / Reverse Proxy  
- **Tomcat** → Application Server  
- **MySQL** → Database  
- **Memcached** → Caching Layer  
- **RabbitMQ** → Message Broker  

### 🔄 Request Flow

User → Nginx → Tomcat → MySQL  
                             → Memcached  
                             → RabbitMQ  

---

## 🧠 Concept: Application Stack

A "stack" is a collection of services working together to deliver a complete application experience.

Each service has a specific role:
- Web layer (Nginx)
- Application layer (Tomcat)
- Data layer (MySQL)
- Performance layer (Memcached)
- Communication layer (RabbitMQ)

---

## 🖥️ Local Environment Setup

The project is executed locally using:

- Virtual Machines (VMs)
- Vagrant (for automation)
- VirtualBox (as hypervisor)

### Why Local Setup?

- Safe testing environment
- No risk to production systems
- Enables experimentation and learning
- Helps understand system internals

---

## ⚙️ Virtual Machine Architecture

Multiple VMs are created, each dedicated to a specific service:

- db01 → MySQL  
- mc01 → Memcached  
- rmq01 → RabbitMQ  
- app01 → Tomcat  
- web01 → Nginx  

### Key Feature

Hostnames are mapped to IP addresses automatically using Vagrant plugins, enabling seamless communication between services.

---

## 🔁 Manual Provisioning

Manual provisioning involves setting up each service step-by-step.

### Key Characteristics

- Time-consuming  
- Not repeatable  
- Error-prone  
- Requires manual intervention  

### Learning Outcome

- Deep understanding of system internals  
- Clear understanding of service dependencies  
- Ability to debug issues  

---

## 📊 Service Setup Order (Very Important)

Services must be configured in the correct order:

1. MySQL  
2. Memcached  
3. RabbitMQ  
4. Tomcat  
5. Nginx  

### Why Order Matters?

- Application depends on database  
- Cache depends on database  
- Messaging depends on application  
- Web server depends on application  

---

## 🗄️ MySQL (Database Layer)

### Role
Stores application data such as user credentials.

### Key Concepts

- Database initialization  
- User creation and permissions  
- Schema import  

### Important Insight

Applications rely on databases for authentication and persistent storage.

---

## ⚡ Memcached (Caching Layer)

### Role
Improves performance by caching frequently accessed data.

### Key Concept

- Reduces load on database  
- Speeds up repeated requests  

### Important Configuration

By default, services listen only on localhost.  
To allow communication across VMs, the service must be configured to listen on all IPs (`0.0.0.0`).

---

## 📩 RabbitMQ (Messaging Layer)

### Role
Acts as a message broker for asynchronous communication.

### Key Concepts

- Queue-based communication  
- Decouples services  
- Improves scalability  

### Note

In this project, RabbitMQ is used mainly to simulate real-world complexity.

---

## ☕ Tomcat (Application Layer)

### Role
Hosts the Java-based web application.

### Key Concepts

- WAR file deployment  
- Application configuration  
- Backend service connectivity  

### Important File

`application.properties`

This file contains:
- Database connection details  
- Cache server details  
- Messaging service details  

---

## 🌐 Nginx (Web Layer)

### Role
Acts as:
- Reverse proxy  
- Load balancer  

### Key Function

- Receives user requests  
- Forwards them to Tomcat  

---

## ✅ Validation of Setup

The application is validated through a browser.

### Successful Validation Indicates:

- Nginx is routing correctly  
- Tomcat is running application  
- MySQL is storing data  
- Memcached is caching data  
- RabbitMQ is functioning  

---

## ⚠️ Challenges in Manual Setup

- Time-consuming  
- Difficult to repeat  
- Prone to human errors  
- Complex dependency handling  

---

## 🤖 Automated Provisioning

Automation is introduced to solve manual setup challenges.

### Approach

- Use Vagrant provisioning  
- Use shell scripts for setup  

### Benefits

- Fast setup  
- Repeatable process  
- Consistent environments  
- Infrastructure as Code (IaC)  

---

## 🧾 Automation Workflow

- Vagrant creates VMs  
- Shell scripts install services  
- Configuration is applied automatically  
- Entire stack is deployed with a single command  

---

## 🔁 Manual vs Automated Setup

| Feature | Manual | Automated |
|--------|--------|----------|
| Speed | Slow | Fast |
| Repeatability | No | Yes |
| Effort | High | Low |
| Errors | High | Low |

---

## 🧠 Key Learnings

- Real-world applications use multiple services  
- Service communication is critical  
- Configuration management is essential  
- Automation is the backbone of DevOps  

---

## 🚀 Conclusion

This project provides:

- A strong foundation in DevOps  
- Hands-on experience with real-world architecture  
- Understanding of system design and dependencies  
- Transition from manual setup to automation  

It prepares the learner for advanced topics such as:
- CI/CD pipelines  
- Docker  
- Kubernetes  
- Cloud deployments  

---
