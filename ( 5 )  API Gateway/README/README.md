# 🌐 Introduction to Amazon API Gateway

## 📘 Overview
This hands-on lab demonstrates how to build a **simple serverless microservice** using **Amazon API Gateway** and **AWS Lambda**.  
The project implements a **FAQ (Frequently Asked Questions)** service that returns a random question-answer pair in JSON format when accessed through an API endpoint.

Amazon API Gateway receives HTTP requests, triggers the **AWS Lambda** function, and returns the processed JSON response to the client — all without managing any servers.

---

## 🎯 Objectives
By completing this lab, I achieved the following:
- Created and configured an **AWS Lambda** function.
- Deployed an **Amazon API Gateway REST API endpoint**.
- Integrated **API Gateway** with **Lambda** for real-time responses.
- Tested and debugged the integration using **Amazon CloudWatch Logs**.
- Gained hands-on understanding of **serverless APIs** in AWS.

---

## ⚙️ Services Used
- **Amazon API Gateway** – For creating, managing, and exposing RESTful APIs.  
- **AWS Lambda** – To run backend code without provisioning or managing servers.  
- **Amazon CloudWatch** – For monitoring, logging, and debugging.  
- **VPC (Virtual Private Cloud)** – To provide secure networking to Lambda.  

---

## ⚙️ Steps Performed

### **1. Created an AWS Lambda Function**
- **Function Name:** `FAQ`
- **Runtime:** Node.js 22.x  
- **Execution Role:** Used existing `lambda-basic-execution` IAM role  
- **Networking:** Attached Lambda to a predefined **VPC**, **Subnets**, and **Security Group** for security and isolation.  

#### 📜 Code Used:
```javascript
export const handler = function(event, context) {
  const faqs = [
    { q: "What is AWS Lambda?", a: "AWS Lambda lets you run code without provisioning or managing servers." },
    { q: "What events can trigger a Lambda function?", a: "Events such as S3 uploads, DynamoDB updates, or API Gateway requests." },
    { q: "What languages does Lambda support?", a: "Node.js, Python, Java, and more." }
  ];
  
  const random = Math.floor(Math.random() * faqs.length);
  const response = { body: JSON.stringify(faqs[random]) };
  
  console.log(response);
  context.succeed(response);
};
```

✅ **Result:** Successfully created a Lambda function that returns random FAQ entries in JSON format.

---

### **2. Created an Amazon API Gateway Endpoint**
- Added an **API Gateway Trigger** to the Lambda function.
- **Configuration:**
  - **API Type:** REST API  
  - **Security:** Open (for testing)  
  - **API Name:** `FAQ-API`  
  - **Deployment Stage:** `myDeployment`  

✅ **Result:** API Gateway created a REST endpoint URL that directly invokes the Lambda function.

---

### **3. Tested the Lambda Function and API**
- Copied the **API Endpoint URL** from the API Gateway trigger.  
- Opened the URL in a web browser — the API returned a random FAQ in JSON format:  

```json
{
  "q": "What is AWS Lambda?",
  "a": "AWS Lambda lets you run code without provisioning or managing servers."
}
```

- Also tested the function within the **AWS Lambda Console** using an empty event `{}`.
- Confirmed **Execution result: succeeded** and reviewed execution logs.

✅ **Result:** Both the standalone Lambda and API Gateway trigger worked successfully.

---

### **4. Monitored the Integration Using CloudWatch**
- Opened the **Monitor** tab in AWS Lambda.
- Viewed key metrics:
  - Invocations
  - Duration
  - Error Count and Success Rate (%)
  - Memory Usage
- Chose **View CloudWatch Logs** to analyze log streams for debugging details.

#### 🧠 Insights:
CloudWatch Logs displayed details such as request IDs, execution times, and logged responses.  
This helped validate the Lambda’s behavior and API call trace.

✅ **Result:** Successfully monitored and debugged the API using CloudWatch.

---

### **5. Key Learnings**
- Understood how **Amazon API Gateway** connects client requests to **AWS Lambda** functions.
- Learned to create **serverless APIs** with minimal setup and zero infrastructure management.
- Experienced event-driven execution and monitoring in **AWS CloudWatch**.
- Observed how **VPC security groups** ensure Lambda isolation in a networked environment.
- Practiced **real-world troubleshooting** for API and Lambda integration.

---

## 🧩 Final Outcome
Successfully built and deployed a **Serverless FAQ Microservice** using **Amazon API Gateway** and **AWS Lambda**.  

---

## 🚀 Conclusion
🎉 I successfully completed this AWS lab and gained hands-on experience in creating, deploying, and monitoring **serverless APIs** using AWS services.  
This project improved my understanding of how **API Gateway**, **Lambda**, and **CloudWatch** work together in a real-world cloud environment.

---

