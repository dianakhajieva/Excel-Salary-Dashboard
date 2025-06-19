# Excel-Salary-Dashboard

![main](https://github.com/user-attachments/assets/8ea4f203-cb26-46f3-9fdf-ad487f06172d)


## 📘 Overview:
This Excel-based interactive dashboard provides a visual summary of salary information for data-related roles based on user-selected filters such as Job Title, Country, and Job Type. It helps users (students, professionals, and job seekers) explore and compare median salary ranges in the data science field globally.
#### You can [click](https://1drv.ms/x/c/EDEEB2CD1F01113A/EcqS267efMtGllOHnRaCUBMBvbk_ypHg0obmwbv4hAoJpQ?e=awdMyg) to see

## 🎯 Purpose:
To assist users in estimating and comparing expected salaries across different job titles and countries. This can guide career decisions, job applications, and negotiation strategies.

## 📊 Key Features:

Interactive slicers allow filtering by job title, country, and employment type (e.g., full-time, part-time).

KPI cards display metrics such as median salary, top job platform, and total job count.

## 📍 Data Source:
Real-world datasets scraped or aggregated from platforms like Ai-Jobs.net and LinkedIn

# Dashboard Build

### Data Job Salaries
![job title](https://github.com/user-attachments/assets/c4497b99-002a-48c2-9ef0-409cba62fbb0)

- Excel Capabilities: Employed bar charts with formatted salary figures and arranged components for clear presentation.
- Visualization: Used horizontal bar charts to make salary comparisons more intuitive.
- Data Structuring: Job titles are ordered from highest to lowest salary to enhance readability.
- Key Points: The visualization highlights salary patterns, showing that Senior and Engineering positions generally earn more than Analyst roles.

### Country Median Salaries
![country map](https://github.com/user-attachments/assets/e41fc9b9-021e-4b31-87d2-cc6efa8194d6)

- Excel Capabilities: Used Excel’s map chart to display median salaries by country.
- Visualization: Applied color gradients to indicate varying salary levels across different regions.
- Data Display: Showed median salaries for each country where data is available.
- Key Points: Offers a fast overview of global salary variations, spotlighting both high- and low-paying areas.

### Job Schedule Type
![schedule type](https://github.com/user-attachments/assets/d410bb35-d815-4c0e-a80e-50840f2810d6)

- Excel Capabilities: Implemented horizontal bar chart to compare median salaries by job type.
- Design Choice: Used contrasting shades to clearly distinguish between Part-time, Contractor, and Full-time roles.
- Data Representation: Displays salary ranges aligned to employment type categories.
- Insights Gained: Reveals that Part-time roles offer the highest median salary, followed by Contractor and Full-time positions—suggesting higher hourly rates for limited-hour roles.

# Functions Used
### Median Salary by Country
```
MEDIAN(
  IF(
     (jobs[job_country]=B3)*
     (jobs[salary_year_avg]<>0)*
     (jobs[job_title_short]=title)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type]))),
      jobs[salary_year_avg]
    )
)
```

- 🧩 Conditional Matching: Evaluates job records where country, role, schedule type match user input, and salary is non-zero.
- 📐 Median Calculation: Leverages an array-based MEDIAN with logical filters for accurate output.
- 📍 Context-Aware Output: Generates salary figures tailored to specific job profiles and regions.
- 🧮 Functional Role: Drives the salary summary table by returning median pay for filtered job criteria.


# Conclusion

This dashboard was developed to help users quickly explore and compare salaries across job titles, countries, and work types. With interactive filters and visual elements like KPI cards and charts, the tool makes salary trends easy to understand. This project shows how Excel can turn raw data into practical career insights.














