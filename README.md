# PALMORA GROUP HR ANALYSIS DOCUMENTATION 
## PROJECT OVERVIEW
This project involves analyzing HR data for Palmora Group, a manufacturing company in Nigeria, to address gender inequality issues. The analysis focuses on gender distribution, performance ratings, salary structures, and compliance with a new minimum wage regulation. The goal is to provide actionable insights to promote gender equality within the organization.  
## DATA CLEANING AND TRANSFORMATION STEPS 
### 1. Handling Missing Gender Data
Issue: Some employees did not disclose their gender.
Solution: Replaced blank entries in the Gender column with "Undisclosed" using Power Query's Replace Values feature.

### 2. Removing Employees Without Salary
Issue: Some ex-employees had no salary records.
Solution:Sorted the Salary column in ascending order.
Identified and removed the first 43 rows (where salary was blank or zero).

### 3. Handling NULL Departments
Issue: Some departments were marked as "NULL".
Solution:Replaced "NULL" with a blank value.
Sorted the Department column and removed the top rows with missing departments.

###4. Creating Employee Count Measure
DAX Formula Used:
dax
Employee Count = COUNTROWS('Palmora HR Data')
