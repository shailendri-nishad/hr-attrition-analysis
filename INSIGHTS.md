# Insights — HR Attrition Analysis

Notes on what the cleaned dataset actually shows once you cut it by department, role, income, tenure, and a few other angles. Numbers below come straight from `02_cleaned_hr_attrition.csv` (1,470 employees) and line up with the Power BI dashboard.

## The headline number

237 out of 1,470 employees left the company, resulting in an attrition rate of 16.1%. The next step is understanding where these employee exits are concentrated.
## 1. Department contributes to attrition, but other factors have a bigger impact.

| Department | Attrition rate |
|---|---|
| Sales | 20.6% |
| Human Resources | 19.0% |
| Research & Development | 13.8% |

Sales has the highest attrition rate, while HR is close behind. R&D has a lower attrition rate, but the difference isn't huge. This suggests that factors like job role, overtime, and income may have a bigger impact on attrition than department alone.
## 2. Overtime is the single biggest factor

- With overtime: **30.5%** attrition
- Without overtime: **10.4%** attrition

Employees who worked overtime had an attrition rate of 30.5%, compared to just 10.4% for those who didn't. This makes overtime one of the strongest indicators of employee turnover in the dataset.
## 3. Job role matters a lot, and it's not evenly spread

| Job Role | Attrition rate |
|---|---|
| Sales Representative | 39.8% |
| Laboratory Technician | 23.9% |
| Human Resources | 23.1% |
| Sales Executive | 17.5% |
| Research Scientist | 16.1% |
| Healthcare Representative | 6.9% |
| Manufacturing Director | 6.9% |
| Manager | 4.9% |
| Research Director | 2.5% |

Attrition rates vary significantly across job roles. Sales Representatives have the highest attrition rate at 39.8%, followed by Laboratory Technicians and Human Resources employees. In contrast, Managers and Research Directors have the lowest attrition rates, indicating that employee turnover is concentrated in a few specific roles rather than being evenly distributed across the organization.
## 4. Lower income bands lose more people

| Income Band | Attrition count |
|---|---|
| Low | 108 |
| Medium | 52 |
| High | 39 |
| Very High | 38 |

Employees in the Low income band account for the largest share of attrition, with 108 out of 237 total employee exits. While attrition is present across all income levels, lower-income employees appear more likely to leave the organization. This suggests that compensation may play an important role in employee retention.
## 5. Singles leave more than married or divorced employees

- Single: 25.5%
- Married: 12.5%
- Divorced: 10.1%

Single employees have the highest attrition rate (25.5%), compared to married (12.5%) and divorced employees (10.1%). This suggests that employee turnover is noticeably higher among single employees, although the dataset does not explain the underlying reasons for this difference.
## 6. New employees are the highest risk group

| Tenure | Attrition rate |
|---|---|
| 0-2 years | 29.8% |
| 3-5 years | 13.8% |
| 6-10 years | 12.3% |
| 10+ years | 8.1% |

Employees with 0–2 years of tenure have the highest attrition rate (29.8%). Attrition decreases as employees stay longer with the company, indicating that the highest risk of turnover occurs during the early years of employment.
## 7. Work-life balance score matters more than any other satisfaction metric

| Work-Life Balance Score | Attrition rate |
|---|---|
| 1 (worst) | 31.2% |
| 2 | 16.9% |
| 3 | 14.2% |
| 4 (best) | 17.6% |

Work-life balance appears to influence attrition. Employees with the lowest score (1) show the highest attrition rate at 31.2%, while employees reporting better work-life balance experience considerably lower turnover rates.
## 8. Frequent travelers leave more

- Travel frequently: 24.9%
- Travel rarely: 15.0%
- No travel: 8.0%

Employees who travel frequently are more likely to leave the company than those who travel less or not at all. Attrition rises from 8.0% among non-travelers to 24.9% among frequent travelers.
## A few other patterns worth noting

- Employees who left lived slightly farther from work on average (10.6 vs 8.9 miles).
- Leavers had worked at more companies previously (2.94 vs 2.65), indicating a slightly higher tendency to switch jobs.
- Gender showed no significant impact on attrition, as employee exits closely reflected the overall workforce distribution.
## Where this overlaps

Many of these factors are likely connected. Employees affected by multiple high-risk factors may be more likely to leave than those affected by just one. Further analysis could explore these relationships in more detail.
