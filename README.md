# Pewlett_Hackard_Analysis
## SUMMARY
The purpose of this analysis is to use company employee data to determine the number of employees retiring by job title as well as to identify employees who are eligible to participate in a mentorship program.  This task will be accomplished using PostreSQL to combine and analyze the employee data that resides in various different sizeable databases.
### BACKGROUND
At Pewlett Hackard, the company is worried that they will be facing an employee shortage in certain departments and management positions when baby-boomers start to reach retirement age.  The department manager has requested a list of employees and count by their latest job Title who will be retiring soon.  In order to plan ahead for this potential upheaval of employees leaving, the manager also wants to get a list of current employees who are eligible for a mentorship program to make them promotable into the potential job openings.
#### DATA PROVIDED 
The following data base files were provided in csv format:
1. Departments
2. Employees
3. Dept_Manager
4. Salaries
5. Titles
6. Dept_emp
  
### ANALYSIS
The first step of the project was to look at the databases provided and create an Entity Relationship Diagram (ERD) in order to see what variables we have and how they can be used and combined as shown below:
  
![](https://github.com/xactuary/Pewlett_Hackard_Analysis/blob/main/Data/EmployeeDB.png)
  
Using this diagram, a list was extracted that shows the employee names, birth dates, titles and employment.  A preview of the file is as follows:
  
![](https://github.com/xactuary/Pewlett_Hackard_Analysis/blob/main/Data/Table_1_retirement_titles_snip.PNG)
  
The previous file contained some duplicates for employees who may have been promoted over time.  So an additional table was created that has only the last title carried by the employee.  So for example, employee Koiychi had 2 entries but the latest job title was Senior Staff.  so the next table removes the older title and only keeps the current one. 
  
![](https://github.com/xactuary/Pewlett_Hackard_Analysis/blob/main/Data/Table_2_unique_titles_snip.PNG)
  
Because the number of employees on these lists is so large, we have developed a summary exhibit of this first part of the analysis:
  
![](https://github.com/xactuary/Pewlett_Hackard_Analysis/blob/main/Data/Table_3_retiring_titles_snip.PNG)
  
  

