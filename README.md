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


## Data Cleaning and Data Preparation

### *Cleaning/Preparation Steps* 

* Deleting Constant/ID Columns
* Encoding Target Variables
* Creation of Numeric Buckets
* Data Structure Validation

### *Description and Justification* 

* Remove columns that do not vary in value across the dataset or only serve as unique IDs. These columns do not provide predictive value.
* Convert categorical target variables (Attrition) to numerical format (1/0). This is required for statistical calculations (Correlation, Average) in Excel and metrics in Looker Studio.
* Grouping continuous numeric variables into categories/segments (buckets) to be used as effective Dimensions in Looker Studio.
* Ensure that all categorical variables (such as Job Role, Department) are of the Text (Dimension) type and numeric variables (such as Monthly Income, Attrition_Numeric) are of the Number (Metric) type in Looker Studio.

### *Affected Variables* 

* Employee Count, Standard Hours, Over 18, Employee Number
* Attrition then to Attrition_Numeric (Yes=1, No=0)
* Monthly Income then to Income Group (Low, Middle, High). Age then to Age Group. Salary Increase Percentage then to Salary Increase Group.
* All Columns


## Statistical Analysis 

### *Segmentation Analysis (Pivot Table)*

*Pivot Table Analysis (using Excel/Google Sheets) focuses on comparing attrition rates per category segment to identify the strongest risk triggers.*

* Highest Risk Trigger (Most Impactful Visual):
 * Employees who work overtime have a very high attrition rate (39.0%) compared to those who do not (14.0%).
 * The positions with the highest attrition rates are Sales Representative, Laboratory Technician, and Human Resources.
 * Example of Extreme Risk Combination:
 * Based on preliminary data, Laboratory Technicians in Research & Development who work overtime show an attrition rate of nearly 68%.


### *Statistical Analysis (Mean & Correlation)* 

* The analysis continued by comparing the averages of seven key numerical variables between employees who left (Attrition = 1) and those who remained (Attrition = 0).


### *Statistical conclusions* 

* **Strongest Numerical Factors:** Total Working Years (r = -0.171) and Monthly Income (r = -0.159) are the best predictors. The negative correlation indicates that the lower the length of service and salary, the higher the risk of attrition.
* **Salary Gap:** A significant average salary gap of approximately $2,095 was found between the two groups, making it a key metric for intervention.
* **Profile Factors:** Employees who quit tend to be younger (33.8 years old) and have shorter tenure with the company (5.1 years) compared to those who remain.


## Overview- Rapid Intervention in Risky Segments and Compensation Inequality

### *Turnover Rate vs. Overtime Policy*


![alt text](https://github.com/restianimutoharoh/Diagnostic-Analysis-of-Employee-Attrition-Risk-Factors-for-Retention-Strategy.-/blob/master/IMG/Turnover%20Time%20vs.%20Overtime%20Policy.png?raw=true)


### *Insight* 

*  The turnover rate of employees who work overtime is 39.0% vs. 14.0% for those who do not work overtime. Overtime is the strongest risk catalyst.

### *Recommendation* 

*  Mandate overtime freeze for the 3 job roles with the highest turnover (Sales Representative, Laboratory Technician, Human Resources — see Top 5 Attrition). Immediately allocate compensation resources in the form of time off in lieu (TOIL) to reduce existing burnout.


### *Comparison of Attrited vs. Non-Attrited Salaries*


![alt text](https://github.com/restianimutoharoh/Diagnostic-Analysis-of-Employee-Attrition-Risk-Factors-for-Retention-Strategy.-/blob/master/IMG/Comparison%20Attrited%20vs%20Non-Attrited.png?raw=true)


### *Insight*  

* Show significant differences in average salary: Retained Employees ($8.4M) vs. Departed Employees ($1.1M). Note: The assumption of 1.1M/8.4M is the Average Monthly Salary in Rupiah/Local Currency.


### *Recommendation* 

* Implement focused salary retention for employees in high-risk job roles (Sales, Lab Tech) whose salaries are close to or below the average salary of employees who quit. This action must be swift and significant to move them out of the financial risk segment.


### *Top 5 Attrition by Job Role*


![alt text](https://github.com/restianimutoharoh/Diagnostic-Analysis-of-Employee-Attrition-Risk-Factors-for-Retention-Strategy.-/blob/master/IMG/Comparion%20Attrited%20by%20Positions.png?raw=true)


### *Insight*  

* Three positions have the highest turnover risk: Sales Representative, Laboratory Technician, and Human Resources.
  

### *Recommendation* 

* Implement a Pulse Survey Program focused on Job Satisfaction and Environment Satisfaction in these three positions every month (not quarterly). Use these results as performance metrics for team managers in these positions.



### *Scorecard KPI: Avg. Employee Age (36.9) & Avg. Years at Company (7.0)*


![alt text](https://github.com/restianimutoharoh/Diagnostic-Analysis-of-Employee-Attrition-Risk-Factors-for-Retention-Strategy.-/blob/master/IMG/KPI%20Avg%20Employee.png?raw=true)


![alt text](https://github.com/restianimutoharoh/Diagnostic-Analysis-of-Employee-Attrition-Risk-Factors-for-Retention-Strategy.-/blob/master/IMG/KPI%20Avg%20Years.png?raw=true)



### *Insight*  

* An average tenure of 7.0 years and age of 36.9 years, combined with a high risk of overtime in early tenure (findings from the Analysis page), indicates retention issues among young and new talent.


### *Recommendation* 

* Develop a Loyalty Bonus program linked to 1-3 years of service. This provides a financial incentive early in their career to retain them through the highest risk period.



## Diagnostic Analysis of Employee Attrition Risk Factors for Retention Strategy


### *Risk by Income Tier and Over Time*


![alt text](https://github.com/restianimutoharoh/Diagnostic-Analysis-of-Employee-Attrition-Risk-Factors-for-Retention-Strategy.-/blob/master/IMG/Risk%20by%20Income%20Tier%20%26%20Over%20Time.png?raw=true)


### *Insight* 

* Low-income employees who work overtime have an attrition rate of 53% (vs. 17% for non-overtime workers). This risk is exacerbated among new employees (0-2 years of tenure), where 75% of attrition in this group is related to overtime.


### *Recommendation*  

* **Immediate Action:** Implement an Automated Overtime Approval System that limits overtime for employees in the low-income tier (below $4K) and for those with 0-2 years of tenure.
* **Headcount Increase:** Prioritize hiring new employees (or redistributing workloads) in departments/positions that are the primary sources of overtime (such as Laboratory Technicians in your initial EDA findings).



### *Attrition Rate by Job Satisfaction and Monthly Income*


![alt text](https://github.com/restianimutoharoh/Diagnostic-Analysis-of-Employee-Attrition-Risk-Factors-for-Retention-Strategy.-/blob/master/IMG/Attrition%20by%20Job%20Satisfaction.png?raw=true)


### *Insight* 

* The highest risk segment is employees with Job Satisfaction 1 and Low Income. The average Age (36.9) and Tenure (7.0) you show indicate that turnover tends to occur among younger and less experienced talent.


### *Recommendation*   

* **Double Salary Intervention:** Identify employees in the “Job Satisfaction 1” quadrant on the Treemap. Make ad hoc salary adjustments to raise their Monthly Income above your attrition average (above $5,000), as they present the worst combination of risks. 
* **Mentorship and Check-ins:** Focus HR mentorship and check-ins on younger employees (under 30) and new hires, as they are most vulnerable to the risks of low salary and satisfaction.



### *Attrition Rate by Salary Hike*


![alt text](https://github.com/restianimutoharoh/Diagnostic-Analysis-of-Employee-Attrition-Risk-Factors-for-Retention-Strategy.-/blob/master/IMG/Attritied%20by%20Salary%20Hike.png?raw=true)


### *Insight* 

* The risk of attrition does not decrease linearly with salary increases. Particularly in the Low Hike (11%-13%) range, the Attrition Rate shows a minimal decrease.


### *Recommendation*   

* **Optimize Salary Increase Budget:** Based on this data, the salary increase budget allocation (e.g., currently allocated for the 11%-13% range) should be directed toward providing more substantial increases (20%+) to high-performing talent, or used for salary interventions for employees whose salaries are below the risk threshold.
* **Transparency:** Evaluate whether the current salary increase policy is perceived as unfair by employees, as small increases do not seem to be effective in retaining turnover.



### *Risk by Job Satisfaction & Risk by Environment Satisfaction*


![alt text](https://github.com/restianimutoharoh/Diagnostic-Analysis-of-Employee-Attrition-Risk-Factors-for-Retention-Strategy.-/blob/master/IMG/Risk%20Job%20Satisfaction%20%26%20Environment.png?raw=true)


### *Insight* 

* Clear direct relationship: Job Satisfaction Score 1 has the highest Attrition Rate (26%) and Environment Satisfaction Score 1 has an Attrition Rate of 25%.


### *Recommendation*   

* **Focused Diagnostic Survey:** Use a pulse survey targeted at employees with low satisfaction scores (1 or 2). Ask specific reasons behind low Job Satisfaction (e.g., lack of development opportunities, relationship with superiors) and Environment Satisfaction (e.g., facilities, team culture).
* **Managerial Training:** Provide mandatory training to managers whose teams show the lowest satisfaction scores, as managers are the main drivers of Job and Environment Satisfaction.




[Dashboard Analysis of Employee Attrition](https://lookerstudio.google.com/reporting/3ef05b2e-0f94-4503-b372-374d87bbb1bd)
