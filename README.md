# HR Workforce Dashboard

> A Power BI HR analytics dashboard covering workforce size, turnover, satisfaction/engagement, absenteeism, payroll cost and recruitment sources.

---

## 1. Project Overview

**Objective:** Give HR and leadership a view of workforce health, so they can spot hot spots (departments with high turnover, at-risk employee groups) and support decisions on retention, recruitment and HR budget.

### Data Model

A star schema consisting of the following tables:

- **Employee** (fact): employee information, gender, age group, recruitment source, departure reason, status, Retention Risk, race, etc.
- **Department**, **Position**, **Manager**, **Performance**, **MaritalStatus**: dimension tables
- **Dimensions**: a helper table for the slicer that selects the analysis dimension dynamically
- **_Measures**: a table containing the DAX measures (Total Employees, Turnover Rate, Avg. Tenure, etc.)

### Report Structure

| Page | Content |
|---|---|
| **Executive Summary** | 7 KPI cards, 5 analytical charts, 1 summary table by department, and a slicer to select the analysis dimension (Dimension) |
| **Workforce Database** | Detail table by employee, with filters for Department, Performance Score, Manager and Employee Name |

### Main KPIs (Executive Summary)

 <img width="1026" height="70" alt="image" src="https://github.com/user-attachments/assets/fffc976d-ce81-4bd3-ab7c-a3bd99e5b2a9" />


### Main Charts
- Age Distribution: Number of employees by age group (25-34, 35-44, 45-54, 55-64, 65+)
<img width="538" height="368" alt="image" src="https://github.com/user-attachments/assets/fb46d6d1-4460-4a3f-9f66-5af2a34239f7" />

- Gender Distribution: Gender composition, with Turnover Rate shown in the tooltip
<img width="584" height="392" alt="image" src="https://github.com/user-attachments/assets/30b947d5-ebd1-4ff6-b8a7-4e8dae62e5f9" />

- Departure Reason: Number of employees by reason for leaving (e.g., More Money, Career Change, Unhappy, Relocation Out Of Area, Military, Return To School, Terminated for Cause, No-Call No-Show…)
<img width="794" height="410" alt="image" src="https://github.com/user-attachments/assets/bea3a140-e71a-4757-9e05-d6e693c42d22" />

- Turnover Rate by Department: Turnover rate by department
<img width="769" height="370" alt="image" src="https://github.com/user-attachments/assets/04934ece-cebc-48d9-b9ab-c04a13cfe0a4" />

- Top Recruitment Sources: Funnel of recruitment sources (LinkedIn, Employee Referral, Google Search, CareerBuilder, Diversity Job Fair, Website…), with Engagement and Tenure shown in the tooltip
<img width="612" height="442" alt="image" src="https://github.com/user-attachments/assets/cbe9137f-f502-47c7-bf39-2d5b6306dd7f" />

- Workforce Metrics Overview by Dimension: Comparison table of key metrics by department, position, gender, citizenship, age, marital status and ethnicity
<img width="717" height="234" alt="image" src="https://github.com/user-attachments/assets/69e92a3d-8279-4d75-93db-e3e254ed2752" />

- Workforce Database page: Consolidated employee information with filters for Name, Department, Performance Score and Manager
<img width="956" height="488" alt="image" src="https://github.com/user-attachments/assets/77c9e072-79ba-46e1-a10d-02969da7c3e1" />

---

## 2. Main Findings

|  | Issue | Insight | Chart source |
|---|---|---|---|
| 1 | Size and cost | Total headcount - 298, total payroll cost - 20M, average age - 47.8 | KPI cards |
| 2 | Turnover | Company-wide turnover rate - 34.9%; highest department: Production (40.89%), lowest: 16.67% | Turnover Rate by Department |
| 3 | Departure reasons | Most common reason: Another position (19.23% of all departures); controllable reasons (pay, dissatisfaction, work policies) account for 42.31% | Departure Reason |
| 4 | Age structure | Largest age group: 35-44; share of the 55+ group (retirement risk): 20.47% | Age Distribution |
| 5 | Recruitment sources | Source bringing in the most employees: Indeed; source with the best Tenure: Google Search | Top Recruitment Sources |
| 6 | Gender diversity | Male/Female ratio 0.76:1; turnover gap between the two genders 1.39% | Gender Distribution |
| 7 | Satisfaction, engagement, absenteeism | Departments with low Satisfaction and high Absenteeism: Production, IT/IS | Workforce Metrics table |
| 8 | Performance | Satisfaction Score and its relationship with Retention Risk | Workforce Database page |

---

## 3. Main Recommendations

1. **Reduce turnover in high-risk departments:** conduct exit interviews and stay interviews in the departments with the highest Turnover Rate; set quarterly targets to reduce the rate.
2. **Address controllable departure reasons:** if "More Money" and "Unhappy" stand out, review salary bands against the market, career progression paths and the quality of direct management.
3. **Optimize recruitment channels:** increase budget for sources that bring in long-tenured employees; consider cutting sources with short tenure.
4. **Prepare for succession:** for the 55+ age group, build knowledge-transfer plans and train successors.
5. **Monitor the high Retention Risk group:** use the Satisfaction Score + Retention Risk filters on the Workforce Database page to prioritize retaining high-performing employees who are at risk of leaving.
6. **Improve absenteeism and satisfaction:** roll out intervention programs in departments with high Absenteeism and low Satisfaction (flexible work, wellbeing, manager training).

---

## 5. Limitations

- This README was generated from the report structure, so specific figures and conclusions should be verified directly against the dashboard.
- The data supports descriptive analysis only; there is no turnover prediction model yet.
