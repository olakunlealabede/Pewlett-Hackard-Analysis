# Pewlett-Hackard-Analysis
# Overview of the Anaysis
This project is to determine the number of retiring employees per title, and identify employees who are eligible to participate in a mentorship program. Afterwards, a report is being provided to summarize the analysis and helps prepare managers for the “silver tsunami” as many current employees reach retirement age.
# Deliverable 1: The Number of Retiring Employees by Title
Create a SQL Queries with the following instructions:
Retrieve the emp_no, first_name, and last_name columns from the Employees table.
Retrieve the title, from_date, and to_date columns from the Titles table.
Create a new table using the INTO clause.
Join both tables on the primary key.
Filter the data on the birth_date column to retrieve the employees who were born between 1952 and 1955. Then, order by the employee number.
Export the Retirement Titles table from the previous step as retirement_titles.csv and save it to Data folder in the Pewlett-Hackard-Analysis folder.
<img width="532" alt="Retirement_title" src="https://user-images.githubusercontent.com/89113627/140635435-2ea4aa48-83a1-4634-b65b-8efe1898dbaf.png">
Note: There are duplicate entries for some employees because they have switched titles over the years. The following instructions are used to remove these duplicates and keep only the most recent title of each employee.
Retrieve the employee number, first and last name, and title columns from the Retirement Titles table.
These columns will be in the new table that will hold the most recent title of each employee.
Use the DISTINCT ON statement to retrieve the first occurrence of the employee number for each set of rows defined by the ON () clause.
Create a Unique Titles table using the INTO clause.
Sort the Unique Titles table in ascending order by the employee number and descending order by the last date (i.e. to_date) of the most recent title.
<img width="394" alt="Unique_title_table" src="https://user-images.githubusercontent.com/89113627/140635589-13c850c1-7349-416f-849f-32cb8e842323.png">
Write another query to retrieve the number of employees by their most recent job title who are about to retire.
First, retrieve the number of titles from the Unique Titles table.
Then, create a Retiring Titles table to hold the required information.
Group the table by title, then sort the count column in descending order.
<img width="270" alt="retiring_title" src="https://user-images.githubusercontent.com/89113627/140635854-4d6c248c-0206-459d-8eb7-e4ace52d676d.png">
# Deliverable 2: The Employees Eligible for the Mentorship Program
Create a mentorship-eligibility table that holds the current employees who were born between January 1, 1965 and December 31, 1965.
Write a query to create a Mentorship Eligibility table that holds the employees who are eligible to participate in a mentorship program.
Retrieve the emp_no, first_name, last_name, and birth_date columns from the Employees table.
Retrieve the from_date and to_date columns from the Department Employee table.
Retrieve the title column from the Titles table.
Use a DISTINCT ON statement to retrieve the first occurrence of the employee number for each set of rows defined by the ON () clause.
Create a new table using the INTO clause.
Join the Employees and the Department Employee tables on the primary key.
Join the Employees and the Titles tables on the primary key.
Filter the data on the to_date column to all the current employees, then filter the data on the birth_date columns to get all the employees whose birth dates are between January 1, 1965 and December 31, 1965.
Order the table by the employee number.
<img width="559" alt="mentorship_eligibility" src="https://user-images.githubusercontent.com/89113627/140636203-18d70069-ae29-46d2-a8b4-e42a947a56e4.png">
# Summary
How many roles will need to be filled as the "silver tsunami" begins to make an impact?

About 90,398 will be needed to be filled as the "silver tsunami" begins to make an impact.
Are there enough qualified, retirement-ready employees in the departments to mentor the next generation of Pewlett Hackard employees?

There will not be enough because of the total number 1,940 of retirement-ready employees in the departments.
