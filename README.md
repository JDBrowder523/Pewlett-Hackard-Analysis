# Pewlett-Hackard-Analysis

## Overview and Analysis:

 The purpose of this analysis was to use PostgreSQL to conduct a database analysis on the company Pewlett Hackard to determine the number of employees that would be retiring in the near future.  Pewlett Hackard specifically wanted to know the number of employees who would be retiring from each department as well as the employees who would be potential mentors for new hires.

## Results:

 The first step in performing this analysis was to determine the relationships between each of the data sets that Pewlett Hackard provided.  This was done using an Entity Relationship Diagram (ERD) which is shown below.
![This is an image](https://github.com/JDBrowder523/Pewlett-Hackard-Analysis/blob/main/EmployeeDB.png)

### The Number of Retiring Employees by Title:

 - More than 60% of the employees at retirement age are "senior" employees with almost an equal number being senior engineers and senior staff.

 - 50% of the employees at retirement age are in engineers in positions of senior engineer, engineer, and assistant engineer.

![This is an image](https://github.com/JDBrowder523/Pewlett-Hackard-Analysis/blob/main/job_openings_by_title.png)

### The Employees Eligible for the Mentorship Program

 - The candidates who are eligible to become mentors are all born in the year 1965 but have varying time with the company.

 - Most of the candidates who are eligible to become mentors have a senior title.

![This is an image](https://github.com/JDBrowder523/Pewlett-Hackard-Analysis/blob/main/mentorship_candidates.png)

## Summary:

 1. There are a total of 72458 employees who are of retirement age.  Pewlett Hackard will need to start filling these roles as soon as possible in order to maintain enough employees to carry the current workload.  The total number of retirement age employees was determined using the PostgreSQL query below:

--Get the total nummber of mentor candidates
SELECT COUNT (me.emp_no)
FROM mentorship_eligibility AS me;

 2. There are not enough mentorship eligible candidates to mentor all the new hires that Pewlett Hackard will have to hire to replace the retiring workforce.  The total number of mentor candidates is 1549.  This was determined using the PostgreSQL query below:

--Get the total nummber of mentor candidates
SELECT COUNT (me.emp_no)
FROM mentorship_eligibility AS me;