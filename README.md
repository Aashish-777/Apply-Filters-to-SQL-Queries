
Apply Filters to SQL Queries

Project Description:
In this project, I utilized SQL to investigate and address potential security concerns through detailed analysis of login activity and employee data. The tasks demonstrate proficiency in filtering data using SQL operators such as AND, OR, NOT, and LIKE to extract meaningful insights. This work reflects my ability to investigate security incidents, analyze patterns, and provide actionable results, which are vital skills in cybersecurity.

---

Retrieve After-Hours Failed Login Attempts:

SQL Query:

SELECT * 
FROM log_in_attempts 

WHERE success = 0 AND login_time > '18:00';

**Screenshot Reference:**
<p align="center"> <img src="https://imgur.com/KVhFQZq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> <br /> <br />



Explanation:
This query identifies all failed login attempts that occurred after 6:00 PM. The AND operator ensures both conditions—failed login and time—are met, which helps narrow the results to only suspicious after-hours activity.

---

Retrieve Login Attempts on Specific Dates:

SQL Query:

SELECT * 
FROM log_in_attempts 

WHERE login_date = '2022-05-09' OR login_date = '2022-05-08';
<p align="center"> <img src="https://imgur.com/VZ7DdLR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> <br /> <br />

Explanation:
This query retrieves login attempts for May 8 and May 9, 2022, by filtering the `login_date` column. The OR operator ensures inclusion of both dates, providing a comprehensive view of activity around the incident date.

---

Retrieve Login Attempts Outside of Mexico:

SQL Query:

SELECT * 
FROM log_in_attempts 

WHERE country NOT LIKE 'MEX%' AND country NOT LIKE 'MEXICO%';
<p align="center"> <img src="https://imgur.com/ewtrzFG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> <br /> <br />

Explanation:
This query excludes login attempts originating from Mexico. The NOT LIKE operator, combined with the % wildcard, ensures records starting with "MEX" or "MEXICO" are excluded, effectively isolating non-Mexican login attempts.

---

Retrieve Employees in Marketing (East Building):

SQL Query:

SELECT * 
FROM employees 

WHERE department LIKE '%Marketing%' AND office LIKE 'East-%';
<p align="center"> <img src="https://imgur.com/y04o15V.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> <br /> <br />

Explanation:
This query focuses on employees in the Marketing department working in offices located in the East building. The LIKE operator with wildcards allows pattern matching for both the department and office columns.

---

Retrieve Employees in Finance or Sales:

SQL Query:

SELECT * 
FROM employees 

WHERE department LIKE '%Finance%' OR department LIKE '%Sales%';
<p align="center"> <img src="https://imgur.com/yGqDO0F.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> <br /> <br />

Explanation:
This query retrieves employees belonging to either the Finance or Sales departments. The OR operator ensures both departments are included in the results.

---

Retrieve All Employees Not in IT:

SQL Query:

SELECT * 
FROM employees 

WHERE department NOT LIKE '%Information Technology%';
<p align="center"> <img src="https://imgur.com/y6EachH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> <br /> <br />

Explanation:
This query identifies employees who are not part of the Information Technology department. The NOT LIKE operator excludes all records with "Information Technology" in the department column.

---

Summary:
In this project, I used SQL to investigate login activity and employee data, addressing specific cybersecurity concerns such as unauthorized access and departmental machine updates. The queries demonstrate proficiency in filtering data using logical operators, pattern matching with LIKE, and focusing on time and date constraints. This portfolio piece highlights my ability to perform precise and effective data queries to support cybersecurity efforts.
