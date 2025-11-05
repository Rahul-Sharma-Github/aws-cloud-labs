\# ⚙️ Introduction to Amazon DynamoDB



\## 📘 Overview

This hands-on lab introduces \*\*Amazon DynamoDB\*\*, a fully managed NoSQL database service that delivers fast and predictable performance with seamless scalability.  

In this lab, I created and managed a \*\*Music Library database\*\* to understand table creation, item insertion, querying, updating, and deletion in DynamoDB.



---



\## 🎯 Objectives

By completing this lab, I achieved the following:

\- Created a \*\*DynamoDB table\*\* with partition and sort keys.

\- Inserted and managed multiple \*\*items (records)\*\* with flexible attributes.

\- Queried and scanned data efficiently using \*\*DynamoDB console tools\*\*.

\- Updated and deleted items and tables.

\- Understood the \*\*core concepts of NoSQL data modelling\*\* in AWS.



---



\## ⚙️ Steps Performed



\### \*\*1. Created a DynamoDB Table\*\*

\- Table Name: \*\*Music\*\*

\- \*\*Partition Key:\*\* `Artist` (String)  

\- \*\*Sort Key:\*\* `Song` (String)

\- Used default settings for indexing and provisioned capacity.

\- Waited for table status to become \*\*Active\*\* before proceeding.



✅ \*Result:\* Successfully created the `Music` table.



---



\### \*\*2. Added Data to the Table\*\*

\- Added multiple items with unique attributes:

&nbsp; - \*\*Item 1:\*\* `Artist: Pink Floyd`, `Song: Money`, `Album: The Dark Side of the Moon`, `Year: 1973`

&nbsp; - \*\*Item 2:\*\* `Artist: John Lennon`, `Song: Imagine`, `Album: Imagine`, `Year: 1971`, `Genre: Soft Rock`

&nbsp; - \*\*Item 3:\*\* `Artist: Psy`, `Song: Gangnam Style`, `Album: Psy 6 (Six Rules), Part 1`, `Year: 2011`, `LengthSeconds: 219`



🧠 \*Learning:\* Each item can contain different attributes — showing DynamoDB’s \*\*schema-less flexibility\*\*.



---



\### \*\*3. Modified an Existing Item\*\*

\- Edited the `Psy` item to change `Year` from \*\*2011 → 2012\*\*.

\- Saved the update successfully in the console.



✅ \*Result:\* Confirmed the \*\*update operation\*\* in DynamoDB.



---



\### \*\*4. Queried and Scanned Data\*\*

\#### 🔍 Query:

\- Queried for:

&nbsp; - `Artist = Psy`

&nbsp; - `Song = Gangnam Style`

\- DynamoDB quickly returned the exact record using indexed lookup.



\#### 🔎 Scan:

\- Scanned the table using filter:

&nbsp; - `Year = 1971`

\- Returned only records matching that year.



🧠 \*Learning:\*  

\- \*\*Query\*\* is faster (uses index).  

\- \*\*Scan\*\* checks all items — slower but useful for non-key searches.



---



\### \*\*5. Deleted the Table\*\*

\- Selected the \*\*Music\*\* table → chose \*\*Delete\*\*.

\- Typed “confirm” and deleted the table successfully.



✅ \*Result:\* Table and all data were deleted, completing the full lifecycle operation.



---



\## 🧠 Key Learnings

\- Understood how \*\*Amazon DynamoDB\*\* stores and retrieves data using partition and sort keys.  

\- Learned differences between \*\*Query\*\* (indexed) and \*\*Scan\*\* (full-table) operations.  

\- Practiced inserting, editing, and deleting data using the AWS Management Console.  

\- Observed \*\*schema flexibility\*\* — each item can have unique attributes.  

\- Built practical understanding of \*\*NoSQL data modelling\*\* and \*\*table lifecycle management\*\*.



---



\## ✅ Outcome

Successfully created and managed a \*\*NoSQL DynamoDB Music Library\*\* database.  

This lab improved my understanding of \*\*serverless database management\*\*, \*\*query efficiency\*\*, and \*\*AWS data services\*\* for modern cloud-based applications.



