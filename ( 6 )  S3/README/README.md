\# ☁️ Introduction to Amazon Simple Storage Service (S3)



\## 📘 Overview

This project demonstrates my hands-on learning experience with \*\*Amazon Simple Storage Service (Amazon S3)\*\* — one of the foundational services of \*\*AWS Cloud\*\*.  

Through this guided lab, I explored how to securely create, configure, and manage cloud object storage using the \*\*AWS Management Console\*\* and \*\*CLI commands\*\*.



---



\## 🎯 Objectives

By completing this lab, I learned how to:



\- 🪣 Create and configure an \*\*Amazon S3 bucket\*\*

\- 📁 Upload and manage \*\*objects (files)\*\* within a bucket

\- 🔐 Set and test \*\*access permissions\*\* using \*\*ACLs\*\* and \*\*bucket policies\*\*

\- 🔄 Implement \*\*bucket versioning\*\* to protect against accidental data loss

\- 💻 Test \*\*EC2 to S3 connectivity\*\* using AWS CLI commands



---



\## 🧠 Lab Scenario

I worked as a Cloud Trainee simulating a real-world use case:  

> An EC2 instance needed to upload and retrieve daily reporting data from an S3 bucket securely.



To accomplish this, I:

1\. Created a new \*\*S3 bucket\*\* following AWS naming conventions.  

2\. Uploaded a report image (`new-report.png`) to the bucket.  

3\. Configured and tested \*\*access control\*\* to make objects publicly viewable using ACLs and permissions.  

4\. Connected to an \*\*EC2 instance\*\* via AWS Systems Manager Session Manager to verify \*\*read/write\*\* permissions to S3.  

5\. Created a \*\*custom bucket policy\*\* using the \*\*AWS Policy Generator\*\* for secure, role-based access.  

6\. Enabled \*\*Versioning\*\* to preserve multiple versions of objects and restore accidentally deleted files.



---



\## ⚙️ AWS Services Used

\- \*\*Amazon S3\*\* – For object storage and access control  

\- \*\*Amazon EC2\*\* – To simulate report uploads and downloads  

\- \*\*IAM\*\* – To configure bucket policies and instance roles  

\- \*\*AWS Systems Manager (Session Manager)\*\* – For secure EC2 access without SSH  

\- \*\*AWS CLI\*\* – To test S3 operations (`ls`, `cp`, `put`, `get`)  



---



\## 🧩 Key Skills Demonstrated

\- Hands-on understanding of \*\*S3 architecture and permissions\*\*

\- Basic \*\*IAM policy creation\*\* and principle of least privilege  

\- Practical use of \*\*AWS CLI commands\*\* for S3 operations  

\- Implementation of \*\*versioning\*\* for data protection  

\- Understanding of \*\*EC2 and S3 integration\*\*



---



\## 🚀 Result

Successfully deployed a secure, versioned \*\*S3 bucket\*\* connected to an \*\*EC2 instance\*\* for automated report uploads and retrieval.  

This project enhanced my understanding of AWS \*\*object storage\*\*, \*\*security best practices\*\*, and \*\*real-world cloud data management workflows\*\*.



---



\## 🧾 Conclusion

This lab strengthened my practical skills in:

\- Cloud storage configuration  

\- Role-based access management  

\- Data lifecycle protection  



It represents one of my early but solid steps toward mastering \*\*AWS Cloud Services\*\* and preparing for \*\*AWS Certified Cloud Practitioner\*\* and \*\*AWS Solutions Architect – Associate\*\* level knowledge.



---



> 💡 \*Note:\* I am still expanding my AWS Cloud and DevOps knowledge through continuous labs and real-world use cases.



