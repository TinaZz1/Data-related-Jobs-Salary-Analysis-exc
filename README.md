# Data-related-Jobs-Salary-Analysis-exc
This project features an interactive Excel dashboard designed to explore and analyze salary and career trends in data-related jobs. Users can easily filter the information to gain insights into different roles, locations, and job-offering platforms.

# Excel Salary Dashboard

![1_Salary_Dashboard.png](https://imgur.com/yh1DNcJ.png)

## Introduction

This Excel-based dashboard combines data analysis and visualization to deliver insights into the job market for data professionals. By filtering salaries, job types (full-time, part-time, internship, etc.), and locations, it highlights key patterns and supports informed career decisions. 


### Dashboard File

Dashboard - [Link](https://1drv.ms/x/c/cbf1b5f212422808/EdPrJMF5mYtGjuQdSx1mErEBr6iZXL0VMm5WZPZC_tXrNA?e=4DG31D)

My final dashboard is also added to this repository as .xlsx file in [DataJobs_Analysis_p1](https://github.com/TinaZz1/Data-related-Jobs-Salary-Analysis-exc/blob/main/DataJobs_Analysis_p1.xlsx) 


### Excel Skills Used

- **Formulas and Functions**
- **Charts**
- **Data Validation**


### Data Jobs Dataset

The dataset used in this project covers the period from January 2023 to June 2025 and is available through Luke Barousse’s Excel course- [Excel Dataset](https://lukeb.co/bonus_excel_file)

## Dashboard Build

### Charts

#### Data-related Job Salaries - Bar Chart

<img width="646" height="389" alt="image" src="https://github.com/user-attachments/assets/a9d67dad-0148-49fb-8e2c-c282015e6af1" />

<img width="646" height="413" alt="image" src="https://github.com/user-attachments/assets/bc83f618-0b07-4a12-b10d-3b2c03fd3277" />




#### Country Median Salaries - Map Chart

<img width="573" height="379" alt="image" src="https://github.com/user-attachments/assets/cd4a2510-aae9-4fee-9bef-f1bb13fe2daf" />

<img width="573" height="377" alt="image" src="https://github.com/user-attachments/assets/73680460-994d-4fb4-a038-49607bbacd1d" /> 



  Enables quick grasp of global salary disparities and highlights high/low salary regions that helps visualize and understand geographic salary trends.

  

### Formulas and Functions

#### Median Salary by Job Titles

```
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

- **Multi-Criteria Filtering:** Checks job title, country, schedule type, and excludes blank salaries.
- **Array Formula:** Utilizes `MEDIAN()` function with nested `IF()` statement to analyze an array.
- **Tailored Insights:** Provides specific salary information for job titles, regions, and schedule types.
- **Formula Purpose:** This formula populates the table below, returning the median salary based on job title, country, and type specified.

 Background Table

<img width="347" height="272" alt="image" src="https://github.com/user-attachments/assets/9b5ddd15-12fe-471a-a916-638ab8b6eff2" />



 Dashboard Implementation

<img width="625" height="642" alt="image" src="https://github.com/user-attachments/assets/6a08e7b5-7ba6-4fb1-8ed0-8cdb54dd25be" />

#### Count of Job Schedule Type

```
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

- **Unique List Generation:** This Excel formula below employs the `FILTER()` function to exclude entries containing "and" or commas, and omit zero values.
- **Formula Purpose:** This formula populates the table below, which gives us a list of unique job schedule types.

Background Table

<img width="387" height="190" alt="image" src="https://github.com/user-attachments/assets/d4d9d79c-f113-4224-ab08-a38c4078ac60" />

 Dashboard Implementation:

<img width="639" height="641" alt="image" src="https://github.com/user-attachments/assets/b75cc280-26b3-4b37-a314-203bf4eae01b" />

### Data Validation

#### Filtered List

- **Enhanced Data Validation:** Implementing the filtered list as a data validation rule under the `Job Title`, `Country`, and `Type` option in the Data tab ensures:
    - User input is restricted to predefined, validated schedule types
    - Incorrect or inconsistent entries are prevented
    - Overall usability of the dashboard is enhanced

<img width="222" height="215" alt="image" src="https://github.com/user-attachments/assets/c4f04a67-4102-4b93-9be8-8dd1c23e894a" />

<img width="222" height="215" alt="image" src="https://github.com/user-attachments/assets/3b309cbd-7662-4767-b05e-2d4668550089" />

<img width="222" height="215" alt="image" src="https://github.com/user-attachments/assets/c5e5370f-b5a3-43cb-bcc3-ce16ffcbf180" />

