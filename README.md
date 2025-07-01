# 🌐 AWS Scalable Web Infrastructure Project

This project demonstrates a full-stack, production-grade **cloud architecture** on AWS — including high availability, scalability, automation, monitoring, and cost-optimization best practices.

---

## 📌 Project Overview

A highly available web application architecture using multiple AWS services:
- **2 EC2 Instances** with Apache (auto-scaled)
- **Application Load Balancer**
- **RDS (MySQL)** for relational data
- **DynamoDB** with Lambda integration
- **S3 + Glacier** for tiered storage
- **CloudFront** for global content delivery
- **SNS + Lambda** for event-based notifications
- **CloudWatch + CloudTrail** for full observability
- **Route 53** for DNS resolution

---

## 🛠️ Architecture Diagram

> 🖼 View visual architecture
> ![Image](https://github.com/user-attachments/assets/3f421195-c37b-4262-baee-ecac00e768aa)

---

## ⚙️ Step-by-Step Setup

### 1. **Launch EC2 Instances**
- Launch two `t2.micro` instances (Amazon Linux)
- Install Apache on both
- Generate SSH key pairs for secure access

### 2. **Configure Load Balancer & Auto Scaling**
- Set up an **Application Load Balancer**
- Create an **Auto Scaling Group** linked to both EC2s

### 3. **Relational Database: RDS**
- Launch a **MySQL RDS** instance
- Configure security groups for EC2-RDS connection

### 4. **NoSQL: DynamoDB**
- Create a table `UserActivity`
- Insert & query test data

### 5. **Lambda Integration**
- Create a Lambda function triggered by **DynamoDB Streams**
- Log processing and forward events to SNS

### 6. **Storage & Archiving**
- Upload files to **Amazon S3**
- Set **lifecycle policy** to archive data to **Amazon Glacier**

### 7. **Content Delivery with CloudFront**
- Configure **CloudFront** to serve static content from S3

### 8. **Notifications with SNS**
- Create SNS topic
- Subscribe Lambda for triggered notifications

### 9. **Monitoring with CloudWatch**
- Create **alarms**, **dashboards**, and **logs**
- Monitor EC2, RDS, Lambda, etc.

### 10. **Domain & DNS with Route 53**
- Point custom DNS records to **ALB**

### 11. **Audit & Logging with CloudTrail**
- Enable CloudTrail to track user and resource activity

---

## 📸 Screenshots for Lab Verification

- ✅ EC2 & ELB working
- ✅ Auto Scaling triggers
- ✅ RDS + EC2 connectivity
- ✅ DynamoDB insert/query + Lambda logs
- ✅ S3 data → Glacier transition
- ✅ CloudFront serving S3 content
- ✅ SNS triggered from Lambda
- ✅ CloudWatch dashboards & alarms
- ✅ Route 53 resolving to ALB
- ✅ CloudTrail log entries

---

## 🔐 Security Practices

- Use key pairs (`.pem`, `.ppk`) for SSH access  
- Restrict inbound traffic via Security Groups  
- Enable encryption for RDS and S3  
- Enable IAM roles with least privilege  

---

## 🧠 Lessons Learned

- ✅ Hands-on with real-world AWS services  
- ✅ Built a resilient & cost-effective architecture  
- ✅ Practiced automation, monitoring, and scaling  
- ✅ Gained experience with Lambda, CloudFront, and CloudWatch  

---

## 📚 Tech Stack

| Service        | Purpose                         |
|----------------|----------------------------------|
| EC2            | Web server hosting              |
| ALB + ASG      | Load balancing & scalability    |
| RDS (MySQL)    | Relational database             |
| DynamoDB       | NoSQL data storage              |
| Lambda         | Serverless processing           |
| S3 + Glacier   | Object storage & archiving      |
| CloudFront     | CDN for S3                      |
| SNS            | Notifications                   |
| CloudWatch     | Logs, metrics, and alarms       |
| Route 53       | DNS management                  |
| CloudTrail     | Auditing and activity tracking  |

---

## 🏁 Final Note

This project showcases real-world AWS cloud skills suitable for DevOps, cloud engineers, and system architects. Feel free to fork, learn, or contribute!

