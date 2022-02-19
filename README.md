# Pewlett-Hackard-Analysis
Module 7 SQL
## Purpose:
To determine the number of retiring employees per title, and identify employees who are eligible to participate in a mentorship program. In addition, I will need to determine the current number of employees born between January 1, 1952 and December 31, 1955. This will help to understand how many positions will need to be filled. All employees born within that timeframe are considered for a mentorship program, so employees who are close to retirement age can help prepare other employees to fill their positions.

# Deliverable 1: The Number of Retiring Employees by Title

## Retrieve the emp_no, first_name, and last_name columns from the Employees table.
* Retrieve the title, from_date, and to_date columns from the Titles table.
* Create a new table using the INTO clause.
* Join both tables on the primary key.
* Filter the data on the birth_date column to retrieve the employees who were born between 1952 and 1955. Then, order by the employee number.
* Export the Retirement Titles table from the previous step as retirement_titles.csv and save it to your Data folder in the Pewlett-Hackard-Analysis folder.

![image](https://user-images.githubusercontent.com/87340105/154817800-67e3fd07-6cc1-4981-86fb-9c2369668783.png)

![image](https://user-images.githubusercontent.com/87340105/154817727-2e84e0be-7ab0-46c1-836b-c21abf5bca10.png)

## Use the following instructions to remove these duplicates and keep only the most recent title of each employee.

* Copy the query from the Employee_Challenge_starter_code.sql and add it to your Employee_Database_challenge.sql file.
* Retrieve the employee number, first and last name, and title columns from the Retirement Titles table.
* These columns will be in the new table that will hold the most recent title of each employee.
* Use the DISTINCT ON statement to retrieve the first occurrence of the employee number for each set of rows defined by the ON () clause.

![image](https://user-images.githubusercontent.com/87340105/154817873-0fbceb0a-832b-474d-82ff-9ddfc2a15bb3.png)

* Exclude those employees that have already left the company by filtering on to_date to keep only those dates that are equal to '9999-01-01'.
* Create a Unique Titles table using the INTO clause.
* Sort the Unique Titles table in ascending order by the employee number and descending order by the last date (i.e., to_date) of the most recent title.
* Export the Unique Titles table as unique_titles.csv and save it to your Data folder in the Pewlett-Hackard-Analysis folder.

![image](https://user-images.githubusercontent.com/87340105/154817952-5d8bd2bc-ab6a-48f9-bb71-97d5ebc5621f.png)

![image](https://user-images.githubusercontent.com/87340105/154818018-526815b4-a312-443d-a8ac-133075ada8ea.png)

* Write another query in the Employee_Database_challenge.sql file to retrieve the number of employees by their most recent job title who are about to retire.

* First, retrieve the number of titles from the Unique Titles table.

![image](https://user-images.githubusercontent.com/87340105/154818145-cc726589-7d32-4507-b268-f856596800c1.png)

![image](https://user-images.githubusercontent.com/87340105/154818168-7b4e531e-2f71-4c9d-96a3-c26bdd007c6b.png)

* Then, create a Retiring Titles table to hold the required information.
* Group the table by title, then sort the count column in descending order.
* Export the Retiring Titles table as retiring_titles.csv and save it to your Data folder in the Pewlett-Hackard-Analysis folder.

![image](https://user-images.githubusercontent.com/87340105/154818233-42e374e8-c64e-4a77-9a01-d4b8b29d1faf.png)

![image](https://user-images.githubusercontent.com/87340105/154818294-201c9b9e-b390-4129-8744-f0dfafa93abf.png)

# Deliverable 2: The Employees Eligible for the Mentorship Program

## Write a query to create a Mentorship Eligibility table that holds the employees who are eligible to participate in a mentorship program.

* Retrieve the emp_no, first_name, last_name, and birth_date columns from the Employees table.
* Retrieve the from_date and to_date columns from the Department Employee table.
* Retrieve the title column from the Titles table.
* Use a DISTINCT ON statement to retrieve the first occurrence of the employee number for each set of rows defined by the ON () clause.
* Create a new table using the INTO clause.
* Join the Employees and the Department Employee tables on the primary key.
* Join the Employees and the Titles tables on the primary key.
* Filter the data on the to_date column to all the current employees, then filter the data on the birth_date columns to get all the employees whose birth dates are between January 1, 1965 and December 31, 1965.
* Order the table by the employee number.

![image](https://user-images.githubusercontent.com/87340105/154818698-73c1d32c-f71c-4a87-870a-50f20fc292a9.png)

![image](https://user-images.githubusercontent.com/87340105/154818706-685957d2-7b71-4c00-b88d-d9036cbaa4eb.png)

![image](https://user-images.githubusercontent.com/87340105/154818739-03de640b-cbc5-4c4b-b26c-7273641f00ca.png)

* Export the Mentorship Eligibility table as mentorship_eligibilty.csv and save it to your Data folder in the Pewlett-Hackard-Analysis folder.

![image](https://user-images.githubusercontent.com/87340105/154818767-92b424ec-3562-41b2-abf9-2e952bdbb1ba.png)

![image](https://user-images.githubusercontent.com/87340105/154818828-d7e76e97-9727-4701-9465-a276f0518089.png)

## Results: 
* At the time of this analysis there are currently 300,024 employees in the company. 

* There are 41,380 employees who will be retiring within the near future.

* There are 1,549 employees who are eligible to participate in the mentorship program.	

* Most of the retiring employees hold Senior positions in the company. It will be even more important to ensure that the employees who will fill their positions are trained well to ensure the positions contiue to be run smoothly. 


## Summary: 
### How many roles will need to be filled as the "silver tsunami" begins to make an impact?
  - There are 42, 929 roles that will need to be filled once the “silver tsunami” begins to make an impact.

### Are there enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees?
  - No, currently there are 1,549 retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees. 
