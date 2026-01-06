# 🚀 AWS 3-Tier Architecture Project  
**Tomcat + MySQL (RDS) | Nginx | AWS VPC**

---

## 📌 Project Overview
Implemented a secure and scalable **3-Tier Architecture on AWS** separating **Presentation**, **Application**, and **Database** layers using best practices.

---

## 🏗️ Architecture
- **Presentation Layer:** Nginx (Jump Server) – Public Subnet  
- **Application Layer:** Apache Tomcat – Private Subnet  
- **Database Layer:** Amazon RDS (MariaDB) – Private Subnet  

---

## ☁️ Services Used
- Amazon VPC, EC2, RDS (MariaDB)
- Internet Gateway, NAT Gateway
- Route Tables, Security Groups
- Nginx, Apache Tomcat, Java, MySQL Connector

---

## 🔐 Network Design
- Custom VPC
- 1 Public Subnet (Jump Server)
- 2 Private Subnets (App & DB)
- IGW for public access
- NAT Gateway for private subnet internet access

---

## 🖥️ EC2 Instances
| Instance | Subnet | Purpose |
|--------|--------|---------|
| Jump Server | Public | Reverse Proxy & Access |
| App Server | Private | Tomcat Application |
| DB Server | Private | RDS Access |

---

## ⚙️ Implementation Steps
1. Create VPC  
2. Create 3 Subnets (Public, Private-App, Private-DB)  
3. Enable public IP for Public Subnet  
4. Create Security Group (SSH, HTTP, HTTPS, 8080, 3306)  
5. Launch EC2 instances  
6. Create & attach Internet Gateway  
7. Configure Public Route Table → IGW  
8. Transfer key to Jump Server  
9. Create NAT Gateway in Public Subnet  
10. Configure Private Route Table → NAT  
11. Install Java & Tomcat on App Server  
12. Deploy application to `/opt/apache-tomcat-9.0.113/webapps/`  
13. Install & start Nginx on Jump Server  
14. Configure Nginx reverse proxy to App Server private IP  
15. Create RDS (MariaDB) in same VPC  
16. Configure DB & tables  
17. Add MySQL Connector & update `context.xml`  
18. Restart Tomcat

---

## 🎯 Output
- Access app via **Public IP of Jump Server**
- Nginx → Tomcat → RDS data flow
- Secure, scalable 3-tier deployment

---

## 🧠 Learnings
- VPC networking & subnetting
- NAT Gateway usage
- Reverse proxy with Nginx
- Tomcat deployment
- RDS integration

---

## 👨‍💻 Author
**Arya Kadam**  
🎓 Cloud Computing Student | ☁️ AWS | Linux | DevOps Learner 🚀
