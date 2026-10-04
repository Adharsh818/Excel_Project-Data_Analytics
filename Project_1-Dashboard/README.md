# 📊 Excel Salary Dashboard

![1_Salary_Dashboard.png](/0_Resources/Images/1_Salary_Dashboard_Final_Dashboard.gif)

## 📌 Introduction

As a final-year student exploring **Data Analytics and Data Science**, I created this interactive Excel Salary Dashboard to analyze salary trends across different data-related job roles, countries, and employment types.

The project uses a real-world dataset of data science job postings from 2023 containing information about **job titles, salaries, locations, employment types, and skills**.

The goal of this project was to transform raw job-market data into an interactive dashboard that makes it easier to explore salary trends and understand how factors such as **job role, location, and employment type** can influence salary.

---

## 📂 Dashboard File

You can view the complete Excel dashboard here:

📁 [1_Salary_Dashboard.xlsx](1_Salary_Dashboard.xlsx)

---

# 🛠️ Excel Skills Used

The following Excel features were used to build the dashboard:

- 📉 **Charts & Data Visualization**
- 🧮 **Formulas & Functions**
- ❎ **Data Validation**
- 📊 **Excel Tables**
- 🔍 **Data Filtering**
- 📈 **Median Salary Analysis**
- 🎨 **Dashboard Design**

---

# 📊 Data Jobs Dataset

The dataset used in this project contains real-world data science job information from **2023**.

It includes detailed information about:

- 👨‍💼 **Job Titles**
- 💰 **Salaries**
- 📍 **Locations**
- 🛠️ **Skills**
- ⏰ **Job Schedule Types**
- 🌎 **Countries**

The dataset provided the foundation for analyzing salary trends across different segments of the data-job market.

---

# 🏗️ Dashboard Build

## 📉 1. Data Science Job Salaries — Bar Chart

<img src="/0_Resources/Images/1_Salary_Dashboard_Chart1.png" width="850" height="550" alt="Salary Dashboard Chart1">

### 🛠️ Excel Features

- Used a **horizontal bar chart** to compare median salaries across different job titles.
- Formatted salary values for easier interpretation.
- Sorted job titles by salary to make comparisons easier.

### 🎨 Design Choices

A horizontal bar chart was selected because it makes it easier to compare salary values across multiple job roles.

### 💡 Insights

The visualization makes it easy to identify salary differences between data-related roles.

Higher-level and specialized roles such as **Senior Data Scientist and Data Engineer** tend to have higher median salaries compared with roles such as **Data Analyst and Business Analyst**.

---

# 🗺️ 2. Country Median Salaries — Map Chart

![1_Salary_Dashboard_Chart2.png](/0_Resources/Images/1_Salary_Dashboard_Country_Map.gif)

### 🛠️ Excel Features

- Used Excel's **Map Chart** to visualize median salaries geographically.
- Represented salary differences across countries using color intensity.
- Included countries with available salary data.

### 🎨 Design Choice

A map visualization was selected because geographical salary differences can be understood more quickly through a visual representation than through a large table of numbers.

### 💡 Insights

The map highlights differences in median salaries across countries and provides a quick overview of **global salary variation within data-related jobs**.

---

# 🧮 3. Formulas & Functions

## 💰 Median Salary by Job Title

One of the main calculations used in the dashboard was determining the median salary based on multiple conditions.

```excel
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
