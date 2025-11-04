# ⚡ Introduction to AWS Lambda

## 📘 Overview
This hands-on lab introduces **AWS Lambda**, a core compute service that runs code automatically in response to events.  
In this lab, I created and tested a **serverless image processing workflow** where a Lambda function was triggered by **Amazon S3 events** to generate image thumbnails automatically.

---

## 🎯 Objectives
By completing this lab, I achieved the following:
- Created an **AWS Lambda function** from scratch using **Python 3.12**.
- Configured **Amazon S3** as a Lambda event source for object upload events.
- Implemented an **event-driven architecture** that automatically resized images.
- Tested and validated function execution using **Lambda test events**.
- Monitored logs and metrics through **Amazon CloudWatch**.

---

## ⚙️ Steps Performed

### **1. Created Two Amazon S3 Buckets**
- **Source bucket:** `images-<randomnumber>` – stores original images.
- **Target bucket:** `images-<randomnumber>-resized` – stores resized thumbnails.
- Uploaded a test image `HappyFace.jpg` (1280x853) to the source bucket.

---

### **2. Built and Configured the AWS Lambda Function**
- Created function: **Create-Thumbnail**
- **Runtime:** Python 3.12  
- **IAM Role:** Attached existing `lambda-execution-role` with S3 access permissions.  
- Connected Lambda to a **VPC** with defined subnets and security groups.
- Added **S3 trigger** for “All object create events”.

#### 🔧 Code Logic:
```python
- Receives an event when an object is uploaded to S3
- Downloads the image file
- Resizes it to (128x128) using Pillow (PIL)
- Uploads the thumbnail to the "-resized" bucket
```

---

### **3. Tested the Function**
- Created a sample S3 **PUT event** test in the Lambda console.
- Triggered the function manually and verified the successful execution.
- Confirmed that the resized image appeared in the **-resized** S3 bucket.

---

### **4. Monitored with CloudWatch**
- Observed metrics such as:
  - Invocations
  - Duration
  - Error Count
  - Success Rate (%)
- Viewed **CloudWatch Log Streams** for event details, request IDs, and memory usage.

---

## 🧠 Key Learnings
- Understood how **AWS Lambda** runs code automatically without managing servers.  
- Learned to integrate **S3 → Lambda → CloudWatch** for serverless automation.  
- Gained experience with **Python-based Lambda functions**, IAM roles, and S3 triggers.  
- Developed practical knowledge of **event-driven cloud architectures**.

---

## ✅ Outcome
Successfully implemented a **serverless image thumbnail generator** using AWS Lambda and Amazon S3.  
This lab strengthened my understanding of **serverless computing, event-driven design, and AWS automation workflows**.
