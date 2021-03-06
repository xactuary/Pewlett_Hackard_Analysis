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

Because of the very large number of senior staff that are eligible for retirement, management now wants to explore which employees are eligible for a mentorship program so they can make sure they have a plenty of trained employees ready to step into senior roles.  Using the same data, an extract was created of employees who were born in 1965 and are currently employed - as this must be the criteria for being eligible for the mentorship program.  
  
![](https://github.com/xactuary/Pewlett_Hackard_Analysis/blob/main/Data/Table_4_mentorship_snip.PNG)

# CONCLUSION
The first part of the analysis showed the company that:
    
1. There is a significant number of employees who are approaching retirement age
2. The bulk of the potential retirees hold senior level engineering or staff positions
3. With the large number of potential retirees in senior positions, the company needs to prepare to fill these positions in the near future
4. There are a significant number of current employees with senior experience that are within 10 years of retirement who could be used to mentor junior employees
    
Additional queries and summaries that would be valuable in this analysis includes a count of potential mentors by department as well as a count of potential mentors for more additional birth years.  



