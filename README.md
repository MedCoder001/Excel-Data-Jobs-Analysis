# 📊 Excel-Data-Jobs-Analysis

## 📌 Introduction

This project explores data-related job trends and salaries using Excel dashboards. Designed for job seekers and data enthusiasts, the analysis is divided into two parts. The first part `Analysis 1.xlsx` aims to help job seekers to investigate the salary benchmarks while the second part `Analysis 2.xlsx` aims to uncover popular job roles, and high-paying skills in the data industry. The data used originates from Luke Barousse's curated dataset of real-world data jobs from 2023.

## 📁 File Structure

- `Resources/` – Contains the raw dataset files used for the analysis.
- `Analysis 1.xlsx` – Final dashboard file for **Project 1: Salary Dashboard**.
- ``Analysis 2.xlsx`` – Final dashboard file for **Project 2: Skills vs Salary Deep Dive**.

---

## 📊 Project 1: Data Jobs Salary Dashboard

### 🔎 Goal
To help job seekers investigate salary trends across roles, regions, and job types, and ensure fair compensation.

### Final Dashboard
My final dashboard is in [1_Salary_Dashboard.xlsx]().

### 🛠️ Excel Skills Used
- 📉 Charts
- 🧮 Formulas and Functions
- ❎ Data Validation

### Dashboard Build
## 📉 Charts
# 📊 Bar Chart: Data Science Job Salarie

- 🛠️ Excel Features: Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
- 🎨 Design Choice: Horizontal bar chart for easier visual comparison of median salaries.
- 📉 Data Organization: Sorted job titles by descending salary for improved readability.
- 💡 Insights Gained: This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.



#### Map Chart: Country-wise Median Salaries
- **Color-coded Map** – Global disparities in salaries easily observable.

#### Median Salary Formula
Used an array formula to filter by title, country, and schedule type:
```excel
=MEDIAN(IF((jobs[job_title_short]=A2)*(jobs[job_country]=country)*(ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*(jobs[salary_year_avg]<>0), jobs[salary_year_avg]))
