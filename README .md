# Project 5 - Employee Turnover Analysis

**Team:**
1. Arielle Miro 
2. Mekdes Kebede
3. Noah Monastersky 

Presentation link: https://prezi.com/view/jPub1FJnL4i3onm0njRv/

### EXECUTIVE SUMMARY

---

Given the data set from our "client", our goal is to determine the key factors leading to employee turnover. In this process, we will explore the reasons employees are leaving and potential strategies to remedy the turnover rate. The project is organized as follows:

- Company Overview 
- Trends
- Recommendations 


### Introduction

**Objective**: The goal is to understand the main reasons for employee turnover and recommend future strategies for employee retention. 

---

### Overview
 
**Tools**
- Python (Pandas, Seaborn) 
- Prezi

**Data**
Source: hr_employee_attrition.csv (from Github DC-Flex)
Size:
- 1470 observations: in this case observations are employees. We are not certain if this data includes all of the company's employees
- 35 features: these are different attributes such as department, salary, position, etc. 

**Company** 
Given the data provided, we can confirm the below about the company. 
- The company is divided into 3 departments: Research & Development (R&D), Sales, and Human Resources (HR).
- The breakdown for each department out of the company as a whole is below. We have highly imbalanced classes. 
    - R&D : 66%
    - Sales : 30%
    - HR : 4%
- In the given data, about 16% of employees left and 84% of employees remained. 
- Job satisfaction for employees who left vs those who did not leave is not substantially different. This begs the question, why are employees leaving?
- Employee satisfaction is on a scale of 1-4 (we do not have a data dictionary but are assuming that 4 is the highest). Based on the breakdown below, over 60% of employees have significant job satisfaction (within the categories of 4 or 3). 
    - 4  =  31%
    - 3  =  30%
    - 2  =  19%
    - 1   = 20%

### Data Cleaning 
    
- Changed the "Attrition" column to be binary (0,1)
- Dummied the "Department" column in order to analyze correlation through heatmaps
- The data did not have any NaN values 


### Trends

**Based on the data provided, we identified the following trends.**
1. Income Comparison  
- HR Department: There is a large difference between the monthly income of HR employees who left and the mean income for the department overall (about $3,000). 
- R&D Department: The difference in income for employees who left and the mean income is smaller for this department. 
- Sales Department: The difference in income for employees who left and the mean income is smaller for this department. 
- We can suggest that one of the reasons HR employees are leaving is due to income. 

2. Attrition by Job Roles
- When looking only at employees who left the company, the job role with the most attrition was sales representative. 
- Given the above, we decided to look into job satisfaction based on job role. Surprisingly, sales representatives were not the most dissatisfied group of all the job roles. Other job roles across all 3 departments such as Healthcare Representative, Sales Executive, Manufacturing Director, and more have lower job satisfaction rates. 
- So why are sales representatives at this company leaving? Digging deeper, we found that sales representatives have the lowerst monthly income in the company. This could be a determining factor in sales representatives leaving the company. 

3. Attrition by Education Level 
- HR Employees who left seem to have higher education levels. 
- For all employees, those who left tend to have lower education levels. 



### Conclusions & Recommendations

**Conclusions**
- Access to a clear data dictionary will help with further analysis.
- We would like to collect more detailed data from the client (see next steps). 
- Overall, the company's employee retention is pretty good. We believe additional steps taken should be classified preventative action. 

**Next Steps**
- Collect more detailed data on the sales representatives' pay structure (and the overall company).
- Investigate whether the company is paying sales representatives and hr roles up to market value. 
- Collect data on which companies employees are leaving for (i.e. competitors).
- Determine how much the company is willing to increase salaries by and set a budget by department.
- Once we have gathered more data and are confident in a robust data set, the next step is to build a predictive model to determine whether an employee will leave the company or not. Assuming the data is updated regularly, we can monitor our employees and target individuals who are expected to leave. 

