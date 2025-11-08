\# 🔐 Introduction to AWS Identity and Access Management (IAM)



\## 📘 Overview

This hands-on lab demonstrates my practical understanding of \*\*AWS Identity and Access Management (IAM)\*\* — the service used to \*\*manage users, groups, and permissions\*\* in AWS.  

The lab simulates a \*\*real-world access control scenario\*\* where users are assigned permissions based on their roles and responsibilities within an organization.



---



\## 🎯 Objectives

By completing this lab, I learned how to:



\- 👤 Create and manage \*\*IAM Users\*\* and \*\*Groups\*\*

\- 🧩 Attach \*\*AWS Managed Policies\*\* and \*\*Inline Policies\*\*

\- 🔑 Assign \*\*role-based permissions\*\* for Amazon EC2 and S3

\- 🌐 Locate and use the \*\*IAM Sign-In URL\*\* for console access

\- 🧠 Test and verify \*\*policy-based access controls\*\* through user login simulation



---



\## 🧠 Lab Scenario

The company uses both \*\*Amazon EC2\*\* and \*\*Amazon S3\*\* for its operations.  

As part of the IAM team, my task was to configure \*\*access permissions\*\* for three users based on their job functions:



| \*\*User\*\* | \*\*Group\*\* | \*\*Permissions\*\* |

|-----------|------------|----------------|

| user-1 | S3-Support | Read-only access to Amazon S3 |

| user-2 | EC2-Support | Read-only access to Amazon EC2 |

| user-3 | EC2-Admin | Start, Stop, and View EC2 instances |



---



\## ⚙️ Tasks Performed



\### \*\*1️⃣ Explored IAM Users and Groups\*\*

\- Reviewed pre-created IAM users (`user-1`, `user-2`, `user-3`)

\- Inspected IAM Groups (`S3-Support`, `EC2-Support`, `EC2-Admin`)

\- Examined \*\*Managed\*\* and \*\*Inline\*\* policies attached to each group



\### \*\*2️⃣ Assigned Users to Groups\*\*

\- Added each user to their respective groups based on business roles  

\- Verified permissions inheritance through attached IAM policies



\### \*\*3️⃣ Tested Permissions via IAM Sign-In URL\*\*

\- Signed in as each user using the IAM-specific URL  

\- Tested \*\*service access behavior\*\*:  

&nbsp; - `user-1` could view S3 buckets but not EC2  

&nbsp; - `user-2` could view EC2 instances but could not modify or access S3  

&nbsp; - `user-3` had administrative access to start/stop EC2 instances



---



\## 🧩 AWS Services Used

\- \*\*AWS IAM\*\* – For managing users, groups, and permissions  

\- \*\*Amazon EC2\*\* – To test admin and support-level access  

\- \*\*Amazon S3\*\* – To test read-only access controls  



---



\## 🚀 Key Learnings

\- ✅ Gained hands-on experience in \*\*IAM access management\*\*  

\- 🔐 Understood the difference between \*\*Managed Policies\*\* and \*\*Inline Policies\*\*  

\- 🧱 Learned \*\*role-based access control (RBAC)\*\* principles  

\- 🧩 Practiced real-world \*\*user testing and access validation\*\*



---



\## 🧾 Result

Successfully implemented and verified a \*\*secure IAM setup\*\* where each user had limited and appropriate access to AWS services based on their group membership.  

This exercise improved my practical understanding of \*\*AWS identity management\*\*, \*\*policy design\*\*, and \*\*principle of least privilege\*\*.



---



\## 🧠 Conclusion

This lab strengthened my AWS foundation in:

\- Access control and user management  

\- IAM policy creation and troubleshooting  

\- Understanding how permissions affect real AWS services  



> 💡 \*Note:\* I am continuously learning AWS Cloud concepts and performing labs to build practical experience for future \*\*Cloud Support\*\*, \*\*DevOps\*\*, and \*\*AWS Practitioner\*\* roles.



