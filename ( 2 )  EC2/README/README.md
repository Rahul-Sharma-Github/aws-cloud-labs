# 🚀 Introduction to Amazon EC2

## 📘 Overview
This hands-on lab focused on understanding and managing **Amazon Elastic Compute Cloud (EC2)** — a core AWS service that provides resizable compute capacity in the cloud.  
Throughout the exercise, I launched, configured, monitored, resized, and terminated an EC2 instance to gain real-world experience in managing virtual servers on AWS.

---

## 🎯 Objectives
By completing this lab, I achieved the following:

- Launched a **web server instance** (Amazon Linux 2023 AMI) with **termination protection** enabled.  
- Configured **User Data scripts** to automatically install and start an Apache web server.  
- Monitored EC2 instance health and performance metrics using **CloudWatch**.  
- Modified **security group rules** to allow inbound HTTP traffic (port 80).  
- Resized the instance from **t3.micro → t3.small** and expanded its **EBS volume** (8 GiB → 10 GiB).  
- Tested **termination protection** and properly terminated the instance.

---

## ⚙️ Key Steps Performed
1. **Launch Instance** – Created an EC2 instance named *Web Server* in a custom VPC with a user-data script that deployed a simple “Hello From Your Web Server!” webpage.  
2. **Monitor Instance** – Viewed CloudWatch metrics, instance logs, and screenshots to verify setup and health status.  
3. **Update Security Group** – Enabled HTTP (port 80) access by editing inbound rules for the instance’s security group.  
4. **Resize Instance** – Stopped the instance, changed the type to **t3.small**, and increased EBS volume size to **10 GiB**.  
5. **Test Termination Protection** – Verified protection behaviour, then safely disabled it to terminate the instance.

---

## 🧠 Key Learnings
- Gained hands-on experience with **EC2 lifecycle management** — from launch to termination.  
- Learned to use **User Data scripts** for automated instance configuration.  
- Understood **security groups** and **firewall configurations** for HTTP access.  
- Practiced **scaling resources** and managing **EBS volumes**.  
- Observed how **termination protection** prevents accidental deletion of resources.

---

## ✅ Outcome
Successfully deployed and managed a working **Amazon EC2 web server** that hosted a live “Hello From Your Web Server!” webpage — demonstrating fundamental AWS compute and networking concepts.

---
