# Diagnostic Analysis of Employee Attrition Risk Factors for Retention Strategy. 


## Executive Summary 

### *Problem 1*

* Is there wage inequality between employees who quit and those who stay?

### *Insight (Key Findings)* 

* Employees who quit have an average salary of only $1.1 million (assuming local currency) compared to $8.4 million for those who stay.

### *Recommendations*

* Conduct Targeted Salary Audits on all employees earning less than $5,000 (risk threshold) for retention interventions.


### *Problem 2*

* How much does overtime work affect the risk of turnover?

### *Insight (Key Findings)* 

* Employees who work overtime have a turnover risk of 39.0%, almost three times that of those who do not work overtime (14.0%).

### *Recommendations*

* Freeze critical overtime in high-risk departments/positions (Sales, Lab Tech) and allocate additional headcount immediately.


### *Problem 3*

* Which positions are the most vulnerable and require immediate managerial attention?

### *Insight (Key Findings)* 

* Sales Representatives, Laboratory Technicians, and Human Resources have the highest turnover rates (around 25-30% in the Top 5 segment).

### *Recommendations*

* Prioritize the Special Position Retention Program in these three functions, focusing on coaching their team managers.


### *Problem 4*

* Is turnover risk really triggered by dissatisfaction?

### *Insight (Key Findings)* 

* There is a direct correlation. Employees with a Satisfaction score of 1 have the highest attrition risk of 26.2% for Job and 25.2% for Environment.

### *Recommendations*

* Require monthly pulse surveys for employees with scores of 1 or 2 to detect problems and intervene early.


### *Problem 5*

* What is the worst-case risk combination (High-Risk quadrant)?

### *Insight (Key Findings)* 

* High Risk Quadrant: Employees with Job Satisfaction 1 and Low Income show the highest risk (marked by the dark Treemap area).

### *Recommendations*

* Target the Red Quadrant: Allocate 100% of the retention budget to employees in this quadrant, as they are most likely to quit.


### *Problem 6*

* How does overtime worsen the risks for low-wage employees?

### *Insight (Key Findings)* 

* Extreme Impact: Low-income employees who work overtime have a 53% risk of attrition. Double workload is disastrous for low-wage employees.

### *Recommendations*

* Stop mandatory overtime for employees in the low income tier. Compensation must be increased or overtime must be avoided.


### *Problem 7*

* Are the salary increases we offer effective in retaining employees?

### *Insight (Key Findings)* 

* Not entirely effective. The attrition rate tends to remain high at an increase of 11%-13%.

### *Recommendations*

* Revised Raise Policy: Stop giving ineffective small raises. Shift the budget to larger raises (>17%) for high performers.



## Requirements

* **Subject:** 
  * **Priority Project:** Diagnosis and Mitigation of Employee Attrition Risk



Data Analyst Team

The annual turnover rate (16.12%) is too high. We need a clear analysis to find out who is leaving and why. We don't need complicated predictions, we need a strong diagnosis to allocate the retention budget effectively. Focus on compensation, workload, and satisfaction.


Regards, 
VP People & Culture, 
Sarah Johnson




## Exploratory Data Analysis (EDA)


### *Data source:* 

* IBM HR Analytics Employee Attrition & Performance.

*Total Rows (Employees):* 1,470

*Total Data Columns:* 35 (After removing the constant/ID column)

*Unique Values:* 44 (Refers to the total unique values in all columns, for example: 9 Departments + 5 Education + 2 Genders, etc.)

*Target Variable:* Attrition (Converted to Attrition_Numeric: 1 = Yes, 0 = No)

*Overall Attrition Rate:* 16.12% (Calculated from SUM (Attrition_Numeric) / COUNT (Attrition_Numeric))





