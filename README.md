# HR Attrition Analysis

A small end-to-end project where I clean an HR dataset in Python, then build a Power BI dashboard on top of it to figure out where and why employees are leaving.

## Why I picked this dataset

Employee attrition is one of those problems every company actually cares about — replacing someone is expensive and slows teams down. I wanted a dataset that was messy enough to practice real cleaning steps on, but also rich enough to build a proper multi-page-feeling dashboard. The IBM HR Analytics dataset (1,470 employees, 35 original columns) fit that well.

## What's in this repo

```
01_data_cleaning.ipynb       -> Jupyter notebook with the full cleaning process
02_cleaned_hr_attrition.csv  -> Output of the notebook, used directly in Power BI
03_HR_Analytics_Dashboard.pbix -> Power BI dashboard file containing all visuals, measures, and data model
Power-Bi_Dashboard.png       -> Screenshot of the final dashboard
INSIGHTS.md                  -> What the data actually shows, broken down factor by factor
```

## Step 1 — Cleaning the data (Python)

The raw file comes in as `.xls` but is actually CSV content, so it gets read with `pd.read_csv()` directly (mentioned this in the notebook so it doesn't look like a mistake).

What I did, in order:

1. Loaded the dataset and checked shape, dtypes, and missing values
2. Checked for duplicate rows
3. Fixed data types where needed
4. Dropped four columns that add zero analytical value:
   - `Over18` — every single employee is "Y"
   - `StandardHours` — same value (80) for everyone
5. Created a few new columns to make the Power BI side easier:
   - `Age_Group` — bucketed into 18-25, 26-35, 36-45, 45-60
   - `Income_Band` — monthly income split into 4 quartile bands (Low / Medium / High / Very High)
   - `Tenure_Band` — years at company grouped into 0-2, 3-5, 6-10, 10+
   - `Is_Overtime` — OverTime Yes/No converted to 1/0, mainly so it's easier to use in some calculations later
6. Exported the result as `cleaned_hr_attrition.csv`

The dataset was already in good shape, with no major missing values or duplicate records. Data preparation mainly focused on organizing the data and creating helper columns for analysis.
## Step 2 — The dashboard (Power BI)

Built on top of the cleaned CSV. Layout is one page, split into three zones:

**Top strip — headline numbers**
Total Employees, Active Employees, Attrition Count, Attrition Rate %, Average Age, Avg Experience.

**Middle row**
- Department filter buttons (HR / R&D / Sales)
- Attrition by Department (donut)
- Attrition by Income Band (bar)
- Attrition by Job Role & Satisfaction (matrix table, satisfaction score 1-4)

**Bottom row**
- Attrition trend against total working years (area chart)
- Age group distribution
- Attrition by Gender
- Department-wise headcount

There's also an Age Group slicer at the top (18-25, 26-35, 36-45, 45-60) that filters the whole page.

For the actual findings and what these numbers mean, see [INSIGHTS.md](./INSIGHTS.md).

## Tools used

- Python (pandas, numpy) for cleaning
- Jupyter Notebook
- Power BI Desktop for the dashboard

## Author

**Shailendri Nishad**
[LinkedIn](https://www.linkedin.com/in/shailendri-nishad-59b13027b) · [GitHub](https://github.com/shailendri-nishad)
