# 👥 HR Gender Attrition Analysis Dashboard | Power BI

> Interactive Power BI dashboard exploring employee attrition patterns
> by gender, age group, department, education level, and job satisfaction
> — uncovering the hidden drivers behind workforce turnover.

![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)
![Power Query](https://img.shields.io/badge/Power%20Query-217346?style=for-the-badge&logo=microsoft&logoColor=white)
![Excel](https://img.shields.io/badge/Excel-217346?style=for-the-badge&logo=microsoftexcel&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

---

## 📸 Dashboard Preview

![HR Gender Attrition Dashboard](hr_gender_attrition_dashboard.jpg)

---

## 📌 Project Overview

| Detail      | Info                                              |
|-------------|---------------------------------------------------|
| Tool        | Power BI Desktop                                  |
| Data Source | HR Data.xlsx + Employee Attrition Dataset.xlsx    |
| Techniques  | DAX, Power Query, KPI Cards, Slicers              |
| Domain      | Human Resources / Workforce Analytics             |
| Focus       | Gender-based Attrition Deep Dive                  |
| Status      | ✅ Completed                                      |

---

## 🎯 Business Questions Answered

- ✅ What is the overall attrition rate split by gender?
- ✅ Which age groups show the highest female vs male attrition?
- ✅ Which departments are the biggest drivers of attrition?
- ✅ How does education level impact resignation tendency?
- ✅ What is the relationship between job satisfaction and attrition?
- ✅ Which job roles show highest gender-specific attrition risk?

---

## 🔍 Key Findings

> 💡 Real insights discovered from this analysis:

- 👩 **Female exits peak at age 25–34** — highest resignation 
  concentration in this age band across all departments
- 🏢 **R&D and Sales drive 94% of total attrition** — 
  critical areas requiring immediate retention strategies
- 😞 **Low job satisfaction** directly correlates with higher 
  resignation rates across both genders
- 🎓 **Life Sciences & Medical education** backgrounds show 
  distinct attrition patterns compared to other fields
- 👨 Male attrition is higher in volume but female attrition 
  is concentrated in specific age and role segments
- ⚖️ **Work-life balance scores** are a strong predictor of 
  resignation intent across all departments

---

## 📊 Key KPIs Tracked

| KPI                  | Description                            |
|----------------------|----------------------------------------|
| Total Employees      | Overall headcount                      |
| Total Attrition      | Number of employees who resigned       |
| Attrition Rate %     | Overall turnover percentage            |
| Gender Split         | Male vs Female attrition breakdown     |
| Department Attrition | Department-wise resignation count      |
| Avg Job Satisfaction | Satisfaction score by role & gender    |
| Age Group Analysis   | Attrition pattern by age band          |

---

## 🧮 DAX Measures Used
```dax
-- Overall Attrition Rate
Attrition Rate = 
DIVIDE(
    CALCULATE(COUNT(HR_Data[Attrition]), 
              HR_Data[Attrition] = "Yes"),
    COUNT(HR_Data[Attrition]), 0
) * 100

-- Female Attrition Count
Female Attrition = 
CALCULATE(COUNT(HR_Data[Attrition]),
          HR_Data[Attrition] = "Yes",
          HR_Data[Gender] = "Female")

-- Dept Attrition %
Dept Attrition % = 
DIVIDE(
    CALCULATE(COUNTROWS(HR_Data), 
              HR_Data[Attrition] = "Yes"),
    CALCULATE(COUNTROWS(HR_Data)),
    0
) * 100
```

---

## 📂 Project Structure
```
├── Hr_Attrition_Analysis_Crio_Project_1.pbix  # Power BI dashboard
├── HR Data.xlsx                                # Primary HR dataset
├── Employee Attrition Analysis-Dataset.xlsx   # Supporting dataset
├── hr_gender_attrition_dashboard.jpg          # Dashboard screenshot
└── README.md                                  # Project documentation
```

---

## ▶️ How to Use

1. Download **Power BI Desktop** (free) from
   [microsoft.com](https://powerbi.microsoft.com/desktop/)
2. Clone this repository
```bash
   git clone https://github.com/DebashisSen2025/HR-Data.git
```
3. Open `Hr_Attrition_Analysis_Crio_Project_1.pbix` in 
   Power BI Desktop
4. Explore the dashboard using slicers:
   - Filter by **Gender** to see male vs female patterns
   - Filter by **Department** to isolate R&D and Sales
   - Filter by **Age Group** to find the 25–34 peak
   - Filter by **Education** to see qualification impact

---

## 🎯 Business Impact

This dashboard directly supports HR teams to:

- 🎯 **Target retention programs** at R&D and Sales departments
- 👩 **Design female-specific retention policies** for the 25–34 
  age group
- 📋 **Improve job satisfaction** tracking and early warning systems
- 💰 **Reduce recruitment costs** by identifying at-risk employees 
  before they resign

---

## 👋 About Me

**Debashis Sen** | Data Analyst

🏆 HackerRank SQL — 5 Star (Advanced Certified)
📊 11+ real-world analytics projects | Crio.do NextGen Fellowship
📍 Jamshedpur, India | Immediate Joiner

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Debashis_Sen-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/debashis-sen25)
[![GitHub](https://img.shields.io/badge/GitHub-DebashisSen2025-black?style=flat&logo=github)](https://github.com/DebashisSen2025)
[![Email](https://img.shields.io/badge/Email-sen.debashis.sd@gmail.com-red?style=flat&logo=gmail)](mailto:sen.debashis.sd@gmail.com)

---

⭐ If you found this project useful, please give it a star!
