# Pwelett-Hackard-Analysis
## Overview
The purpose of this analysis was to act as a Human Resource Analyst to determine which employees of Pwelett HAckard are likely going to retire in the near future and get an approximate of how many positions would need to be filled. Doing this analysis provides the decision makers of the company important insight on the future of their workforce and can help them plan accordingly to ensure adequate staffing and production for the future.
## Resources
* Original datasets:
    * departments.csv
    * dept_emp.csv
    * dept_manager.csv
    * employees.csv
    * salaries.csv
    * titles.csv
* Software:
    * PostgreSQl
    * pgAdmin
    * SQL

## Results
I created the *unique_titles* table to see how many employees could potentially retire and their respective title. I did this by joining the employees and titles tables, filtering by date of birth and date hired, removing duplicates, and ording the data points by date hired. Based on the results there are approximately **72,458** employees retiring.

Using this new table I created the *retiring_titles* table to count and identify the number of retirment-eligible employees based on their respective titles. Below is a list of our findings.
* Results:
    * **25,916** Senior Engineers
    * **24,926** Senior Staff
    * **9,285** Engineers
    * **7,636** Staff
    * **3,603** Tehcnique Leaders
    * **1,090** Assistant Engineers
    * **2** Managers

![Retiring_titles](https://user-images.githubusercontent.com/107579508/182459238-2f3c97b2-f156-479f-a22a-dc5f2bfa4a93.png)

Another task was to create a table that identified eligible employees who could participate in a Mentorship Program to assist the company in this transition period. The *mentorship_eligibility* table was created by joing the employees, department employees and title tables. The criteria for the table was employees born in 1965 and currently working at Pewlett Hackard. There are **1,549** employees eligible to participate in the Mentorship Program. 

## Summary
Starting in the next few months, Pwelett Hackard wil be facing a silver tsunami - an impending wave of retirement-aged employees who are ready to leave the workforce. Given the current economy, this present a major challenge for business. To understand this, I have created an additional table using the code below.

<img width="500" alt="Employees_leaving" src="https://user-images.githubusercontent.com/107579508/182467690-dbf6cbc0-7f6b-4dfc-b40c-aa33e475653d.png">

Pewlett Hackard is going to need to preapre for the departe of approximately **13,505** employees. This number represents the number of people that are currently working at the company, have been there since 1985 to 1988, and their birth date is between 1962 and 1965 to be eligible to retire. 

To see if there are enough potential mentors in each department, I created the *employees_leaving_by_dept* table.

<img width="410" alt="employees_leaving_by_dept_table" src="https://user-images.githubusercontent.com/107579508/182469466-e37222e7-cea7-4c22-be52-d711afb5910b.png">

I ran this query to get the count of mentor eligible employees for each department.

<img width="317" alt="leaving_by_dept_query" src="https://user-images.githubusercontent.com/107579508/182469713-f1f54d2e-8907-482b-927d-5ef63b7271bc.png">

<img width="112" alt="employees_leaving_by_dept_count" src="https://user-images.githubusercontent.com/107579508/182469515-dd127290-2b9c-46d8-ad65-0ef37991ca93.png">

In conclusion, it all depends on how many employees retire and are willing to mentor. More mentors will be required for the Developement, Production, and Sales Departments than incomparison to the Human Resources, Finance, and Marketing Departments. Most of the focus should be surroudning the Departments that are more at risk of negative impact and conversation surrounding the Mentorship Program should commence quickly if executed.