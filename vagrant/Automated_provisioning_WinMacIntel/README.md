# 🚀 VProfile Project — Local Setup & Automation

## 📌 Project Overview

This project demonstrates the setup of a real-world multi-tier web application locally using virtual machines and DevOps tools.

The application stack is built manually and then automated using Vagrant and shell scripting.

This project simulates how real production systems are designed and deployed.

---

## 🎯 Objectives

- Understand multi-tier application architecture  
- Learn how different services communicate  
- Perform manual provisioning of services  
- Automate infrastructure using scripts  
- Build a strong DevOps foundation  

---

## 🏗️ Architecture

User → Nginx → Tomcat → MySQL  
                     → Memcached  
                     → RabbitMQ  

### 🔹 Components

- Nginx → Load balancer / reverse proxy  
- Tomcat → Application server  
- MySQL → Database  
- Memcached → Caching layer  
- RabbitMQ → Message broker  

---

## 🧠 Key Concepts Learned

- Multi-tier architecture  
- Service communication  
- Manual provisioning  
- Automated provisioning  
- Infrastructure as Code (IaC)  
- System debugging and validation  

---

## ⚙️ Tools & Technologies

- Vagrant  
- VirtualBox  
- Linux (CentOS / Ubuntu)  
- Git & GitHub  
- Bash Scripting  
- Apache Tomcat  
- Nginx  
- MySQL (MariaDB)  
- Memcached  
- RabbitMQ  

---

## 📂 Project Structure

vprofile-local-setup/
│
├── vagrant-setup/        # Manual setup documentation
│   ├── README.md
│   ├── notes.md
│   └── commands.md
│
├── automated-setup/      # Automation scripts and documentation
│   ├── Vagrantfile
│   ├── scripts/
│   └── automation.md
│
└── README.md             # Main project documentation

---

## 🔁 Setup Approaches

### 🟢 Manual Setup

- Services are installed and configured step-by-step  
- Helps understand system internals  
- Time-consuming but important for learning  

Location:
vagrant-setup/

---

### 🤖 Automated Setup

- Entire setup is automated using Vagrant and shell scripts  
- Single command deployment  
- Fast and repeatable  

Location:
automated-setup/

---

## ▶️ How to Run the Project

### 1. Clone Repository

git clone <your-repo-url>  
cd vprofile-local-setup  

---

### 2. Navigate to Project Code

cd /e/devops-projects/vprofile-project/vagrant/manual_provisioning/Windows_Mac_Intel  

---

### 3. Start Virtual Machines

vagrant up  

---

### 4. Validate Application

- Open browser  
- Access application using VM IP or hostname  
- Verify:
  - Login (MySQL)  
  - Messaging (RabbitMQ)  
  - Caching (Memcached)  

---

## 🧪 Validation

Successful setup ensures:

- Nginx is routing traffic  
- Tomcat is hosting application  
- MySQL is storing data  
- Memcached is caching data  
- RabbitMQ is processing messages  

---

## ⚖️ Manual vs Automated Setup

Manual Setup:
- High effort  
- Slow  
- Not repeatable  

Automated Setup:
- Low effort  
- Fast  
- Repeatable  

---

## 🧠 Key Learnings

- Real-world systems use multiple services  
- Service dependency order is critical  
- Automation is essential in DevOps  
- Infrastructure should be reproducible  
- Debugging is a key skill  

---

## 🚀 Future Enhancements

- Docker containerization  
- Kubernetes deployment  
- CI/CD pipelines  
- AWS cloud deployment  

---

## 💡 Conclusion

This project provides a strong foundation in DevOps by:

- Building a real-world system from scratch  
- Understanding service interactions  
- Transitioning from manual setup to automation  

It prepares for advanced DevOps practices and real-world job scenarios.
