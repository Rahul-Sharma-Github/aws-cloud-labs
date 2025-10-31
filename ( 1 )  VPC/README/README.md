# 🧩 Introduction to Amazon Virtual Private Cloud (VPC)

## 📘 Overview
- This lab introduces the core concepts of **Amazon Virtual Private Cloud (VPC)**.  
- In this exercise, I created a custom VPC using the **VPC Wizard**, explored its components, and configured basic networking elements such as **subnets**, **route tables**, **Internet Gateway**, and **NAT Gateway**.

---

## 🎯 Objectives
By completing this lab, I achieved the following:

- Created an Amazon VPC using the **VPC Wizard**.
- Configured **public and private subnets** with defined CIDR blocks.
- Attached and verified an **Internet Gateway** for external connectivity.
- Set up a **NAT Gateway** to allow secure outbound access from the private subnet.
- Reviewed **route tables**, **network ACLs**, and **security groups** for traffic management.
- Gained hands-on understanding of how AWS isolates and routes traffic within a VPC.

---

## ⚙️ Steps Performed

### **1. Created a Custom VPC**
- Used the **VPC and More** option in the VPC Wizard.
- Configured:
  - **1 Availability Zone (AZ)**
  - **1 Public Subnet (10.0.25.0/24)**
  - **1 Private Subnet (10.0.50.0/24)**
  - **NAT Gateway in Public Subnet**
  - **No VPC endpoints**
- The VPC was automatically provisioned with required route tables, subnets, and gateways.

---

### **2. Verified VPC Components**
- **VPC:** Confirmed VPC creation with unique VPC ID.
- **Internet Gateway:** Verified successful attachment for internet access to the public subnet.
- **Subnets:**
  - Public Subnet → has route to the Internet Gateway (`0.0.0.0/0`)
  - Private Subnet → routes outbound traffic to the NAT Gateway.
- **Route Tables:** Analyzed routes to understand local vs external traffic flow.
- **Network ACLs:** Checked default rules allowing inbound/outbound traffic; understood stateless filtering behavior.
- **Security Groups:** Reviewed default group allowing internal communication between instances.

---

## 🧠 Key Learnings
- Understood how **VPCs** create isolated virtual networks in AWS.
- Learned how **subnets** are categorized as public or private based on their route tables.
- Observed how **Internet Gateways** and **NAT Gateways** manage inbound and outbound connectivity.
- Recognized the role of **Network ACLs** and **Security Groups** in controlling traffic and enhancing security.

---
