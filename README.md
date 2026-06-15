#  AILab Cloud Infrastructure Modernization on AWS

##  Project Overview

AILab is a fictional Artificial Intelligence and Machine Learning organization that previously relied on manual processes, spreadsheets, and disconnected systems for managing operations.

This project modernizes AILab's infrastructure by migrating its operations to Amazon Web Services (AWS), providing a scalable, secure, monitored, and highly available cloud environment.

The objective was to design and implement a production-inspired cloud architecture that demonstrates real-world AWS services and best practices.

---

# 🏗️ Architecture

```text
Internet
    │
    ▼
Application Load Balancer (ALB)
    │
 ┌──┴──┐
 ▼     ▼
EC2-1  EC2-2
(Web)  (Web)
    │
    ▼
Amazon RDS MySQL
    │
 ┌──┴────────────┐
 ▼              ▼
CloudWatch   CloudTrail
Monitoring   Audit Logs
                 │
                 ▼
              Amazon S3
```

---

# ☁️ AWS Services Implemented

## Amazon EC2

Two EC2 instances were deployed across different Availability Zones to host the AILab web portal.

### Features

* Amazon Linux 2
* Nginx Web Server
* Publicly accessible
* Highly available architecture

---

## Application Load Balancer (ALB)

An Application Load Balancer was configured to distribute incoming traffic across both EC2 instances.

### Benefits

* High Availability
* Traffic Distribution
* Improved Reliability
* Fault Tolerance

---

## Amazon RDS MySQL

A managed MySQL database was deployed using Amazon RDS.

### Database Design

Tables created:

* users
* operational_records
* ml_jobs
* audit_logs

### Benefits

* Centralized Data Storage
* Automated Backups
* Secure Access
* Simplified Database Management

---

## Amazon CloudWatch

CloudWatch was configured to monitor infrastructure performance.

### Implemented Monitoring

* CPU Utilization Monitoring
* Alarm Creation
* Email Notifications using SNS

### Example Alarm

```text
CPUUtilization > 70%
```

---

## AWS CloudTrail

CloudTrail was enabled to capture all AWS account activities.

### Benefits

* Security Auditing
* Activity Tracking
* Compliance Monitoring
* User Action History

---

## Amazon S3

S3 is used as the storage backend for CloudTrail logs and future backup requirements.

### Benefits

* Durable Storage
* Secure Log Retention
* Cost Effective

---

## VPC & Security

A dedicated Virtual Private Cloud (VPC) was used to isolate project resources.

### Security Features

* Custom VPC
* Security Groups
* Controlled Inbound Rules
* Network Isolation

---

# 🌐 AILab Portal

A web-based portal was developed and deployed on EC2.

### Portal Features

* Login Interface
* Dashboard
* Monitoring View
* Operational Records
* ML Job Tracking
* Reports Section
* Infrastructure Overview

---



## Architecture 
For detailed implementation steps, architecture, AWS configurations, screenshots, and project documentation, please refer to the attached Project Report.
---

# 💰 Estimated Infrastructure Cost

| Service               | Monthly Cost |
| --------------------- | ------------ |
| Amazon EC2            | $16.52       |
| Amazon RDS MySQL      | $84.08       |
| Elastic Load Balancer | $29.13       |
| Amazon S3             | $2.50        |
| Amazon CloudWatch     | $3.00        |
| Total                 | $135.23      |

Estimated Annual Cost:

```text
$1,622.76/year
```

---

# 📈 Key Learnings

Through this project, I gained hands-on experience with:

* AWS EC2
* AWS VPC
* Application Load Balancer
* Amazon RDS MySQL
* CloudWatch Monitoring
* CloudTrail Auditing
* S3 Storage
* Infrastructure Design
* Cost Optimization
* High Availability Architecture


---

## ⭐ Project Summary

This project demonstrates the design and deployment of a cloud-native infrastructure on AWS using EC2, RDS, Load Balancing, CloudWatch, CloudTrail, and S3. The solution transforms AILab's manual operations into a centralized, secure, scalable, and highly available cloud platform while following industry-standard cloud architecture practices.
