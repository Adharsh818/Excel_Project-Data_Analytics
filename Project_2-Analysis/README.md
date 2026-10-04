# 📊 Project 2 — Data Science Job Market Analysis

## 📌 Introduction

As a final-year student exploring the field of **Data Analytics and Data Science**, I wanted to understand what skills are most in demand in the industry and how different skills and job roles relate to salary.

For this project, I analyzed a real-world dataset of data science job postings to explore the relationship between **skills, salaries, job roles, and geographical regions**.

The goal was to use Excel's data analytics capabilities to answer practical questions that can help students and aspiring data professionals make better decisions about the skills they choose to develop.

---

## 🎯 Questions I Wanted to Answer

To better understand the data science job market, I explored four main questions:

1. **Do more skills lead to better pay?**
2. **What is the salary for data jobs in different regions?**
3. **What are the most in-demand skills for data professionals?**
4. **What is the salary associated with the top skills?**

---

# 🛠️ Tools & Excel Skills Used

The project was built entirely using **Microsoft Excel** and involved several advanced Excel features:

- 📊 **PivotTables**
- 📈 **PivotCharts**
- 🧮 **DAX (Data Analysis Expressions)**
- 🔍 **Power Query**
- 💪 **Power Pivot**
- 🔗 **Data Modeling**
- 📊 **Data Visualization**

---

# 📂 Dataset

The dataset contains real-world information from **data science job postings from 2023**.

It includes information about:

- 👨‍💼 Job Titles
- 💰 Salaries
- 📍 Locations
- 🛠️ Required Skills
- 🆔 Job IDs
- 🌎 Countries

The dataset provided the foundation for exploring salary trends and the skills employers look for in data-related roles.

---

# 1️⃣ Do More Skills Get You Better Pay?

## 🔍 Data Preparation — Power Query

Before beginning the analysis, I used **Power Query** to clean and transform the raw data.

### 📥 Extract

I extracted the original data from `data_salary_all.xlsx` and created two queries:

- 📊 `data_jobs_all` — containing information about the job postings.
- 🛠️ `data_jobs_skills` — containing the skills associated with each job ID.

### 🔄 Transform

I transformed both queries by:

- Changing column data types
- Removing unnecessary columns
- Cleaning text values
- Removing unwanted words
- Trimming unnecessary whitespace

### 📊 `data_jobs_all`

![Data Jobs All](/0_Resources/Images/2_Project_Analysis_Screenshot1.png)

### 🛠️ `data_jobs_skills`

![Data Job Skills](/0_Resources/Images/2_Project_Analysis_Screenshot2.png)

### 🔗 Load

After cleaning and transforming the data, I loaded both queries into Excel to prepare them for further analysis.

### 📊 `data_jobs_all`

![Loaded Data Jobs](/0_Resources/Images/2_Project_Analysis_Screenshot3.png)

### 🛠️ `data_jobs_skills`

![Loaded Data Skills](/0_Resources/Images/2_Project_Analysis_Screenshot4.png)

---

## 📊 Analysis

I analyzed the relationship between the **number of skills required for a job and its median salary**.

### 💡 Key Insights

- 📈 Higher-paying roles generally tend to be associated with a greater number of required skills.
- 💼 Roles such as **Senior Data Engineer** and **Data Scientist** require multiple technical skills and are among the higher-paying roles.
- 📊 Roles requiring fewer specialized skills, such as **Business Analyst**, generally have lower median salaries compared with highly specialized technical roles.

![Salary vs Skills Analysis](/0_Resources/Images/2_Project_Analysis_Chart1.png)

### 🤔 Why Does This Matter?

For someone entering the data field, this highlights the importance of developing a **strong and relevant technical skill set** rather than focusing on only one skill.

---

# 2️⃣ What Is the Salary for Data Jobs in Different Regions?

## 🧮 Tools Used — PivotTables & DAX

For this analysis, I used the **Data Model created with Power Pivot** and a PivotTable to compare salary levels across different regions.

### 📊 PivotTable

I created a PivotTable using the Data Model.

The fields were organized as follows:

- `job_title_short` → **Rows**
- `salary_year_avg` → **Values**

I then created a DAX measure to calculate the **median salary for jobs in the United States**.

```DAX
Median US Salary :=
CALCULATE(
    MEDIAN(data_jobs_all[salary_year_avg]),
    data_jobs_all[job_country] = "United States"
)
<img width="759" height="513" alt="2_Project_Analysis_Chart3" src="https://github.com/user-attachments/assets/a2fd2d66-9c90-4e6c-bdda-f76e5e2a1a52" />
<img width="862" height="452" alt="2_Project_Analysis_Chart4" src="https://github.com/user-attachments/assets/61e58142-3d00-4b71-97d2-b4033c82d0b1" />

