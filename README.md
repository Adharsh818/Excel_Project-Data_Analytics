# 📊 My Data Analytics Projects

A collection of my **Data Analytics projects built using Microsoft Excel**, covering interactive dashboards, data analysis, PivotTables, Power Pivot, Data Models, DAX, and data visualization.

---

# 📈 Project 1 — Salary Dashboard

[🔗 Check out my work here](Project_1-Dashboard)

An interactive **Salary Dashboard** built in Microsoft Excel to analyze salary trends across different job roles, countries, employment types, and job platforms.

<img width="800" height="333" alt="Salary Dashboard" src="https://github.com/user-attachments/assets/91a05102-550c-4143-b213-aa79b5645dc8" />

## 🎯 Objective

The objective of this project was to transform raw job-market data into an interactive dashboard that can be used to explore salary trends and compare different segments of the job market.

## 🔎 Analysis Performed

- Analyzed salaries across different **job roles**
- Compared salary information across **countries**
- Analyzed salaries by **employment type**
- Analyzed job postings across different **job platforms**
- Used **median salary** to represent typical salary levels
- Created interactive filters to explore specific job categories
- Built supporting calculation tables for dynamic dashboard outputs

## 🛠️ Excel Skills Used

- Excel Tables
- PivotTables
- Data Validation
- XLOOKUP
- COUNTIFS
- IF / Conditional Logic
- Data Cleaning
- Data Visualization
- Interactive Dashboard Design

## 💡 Key Learning

This project helped me understand how to take raw job-market data and transform it into an **interactive dashboard that communicates useful business insights through visualizations and filters**.

---

# 📊 Project 2 — Job Market Analysis Using Power Pivot

[🔗 Check out my work here](Project_2-Analysis)

This project focuses on deeper analysis of job-market data using **Power Pivot, Data Models, DAX, PivotTables, and data relationships**.

The analysis explores the relationship between **job roles, salaries, and required technical skills**.

---

## 📌 Analysis 1 — Skill Demand

Analyzed the frequency of different technical skills across job postings to understand which skills are most commonly requested by employers.

Examples of skills analyzed include:

- Java
- Azure
- AWS
- Spark
- Python
- SQL

This analysis helps identify the **most frequently requested technical skills** in the dataset.

<img width="759" height="513" alt="Skill Analysis" src="https://github.com/user-attachments/assets/f37764b4-bee8-41d7-9025-33f1dd5c5c94" />

---

## 💰 Analysis 2 — Salary by Job Role

Analyzed **median salary** across different job roles and compared salary levels across different geographical segments.

Examples of roles analyzed include:

- Data Analyst
- Data Engineer
- Data Scientist
- Business Analyst
- Cloud Engineer
- Senior Data Analyst
- Senior Data Scientist

Using median salary helps reduce the influence of extreme salary values and provides a better representation of typical compensation.

<img width="862" height="452" alt="Salary Analysis" src="https://github.com/user-attachments/assets/da07dd74-d0c7-4c31-b5f8-33bef647b98b" />

---

## 🧠 Analysis 3 — Skills vs Salary

Analyzed the relationship between **technical skills and median salary**.

The analysis helps identify which skills are associated with higher-paying job opportunities.

Examples include comparing skills such as:

- AWS
- Azure
- Java
- Spark
- Python
- SQL

<img width="874" height="537" alt="Skills vs Salary Analysis" src="https://github.com/user-attachments/assets/c96fd964-124b-4805-b43a-eaa5b42adb74" />

---

## 📈 Analysis 4 — Salary vs Number of Skills

Analyzed the relationship between:

**Job Salary ↔ Number of Skills Required**

This provides insight into how the number of technical skills associated with a job varies across different job roles and salary levels.

The analysis compares metrics such as:

- Median Salary
- Number of Skills per Job
- Job Role

This helps explore whether higher-paying roles tend to require a broader range of technical skills.

---

# ⚙️ Power Pivot & Data Modeling

For this project, I used **Power Pivot** to build a Data Model and analyze multiple related datasets.

### Power Pivot was used for:

- Creating a Data Model
- Connecting related tables
- Creating relationships between tables
- Building PivotTables
- Creating DAX measures
- Performing salary analysis
- Performing skill analysis
- Analyzing multiple datasets together

### Data Model

```text
                    Data Model
                        │
              ┌─────────┴─────────┐
              ↓                   ↓
       Job / Salary Data      Skills Data
              │                   │
              └────── job_id ─────┘
                    Relationship
