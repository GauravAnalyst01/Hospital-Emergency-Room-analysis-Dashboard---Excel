# 🏥 Hospital Emergency Room Dashboard

An interactive Excel MIS dashboard built to monitor hospital emergency room performance: patient volume, wait times, treatment delays, and satisfaction scores. The project uses a proper Power Pivot data model instead of flat pivot tables, so the reporting is dynamic and time-based filtering actually works correctly.

![Excel](https://img.shields.io/badge/Tool-Microsoft%20Excel-217346?style=flat&logo=microsoft-excel&logoColor=white)
![PowerPivot](https://img.shields.io/badge/Engine-Power%20Pivot-2C5F91?style=flat)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

## 📌 Overview

Hospitals collect a huge amount of patient-level data every day: admissions, wait times, satisfaction feedback. On their own, these raw records don't help staff make quick decisions. This project converts 2023-2024 ER patient data into a live, filterable MIS dashboard so hospital administrators can track service quality by month and year without touching a single formula.

The main part of this project is the backend setup. Instead of using flat pivot tables directly on raw data, I built a proper data model using Power Query and Power Pivot, the same basic approach used in tools like Power BI. This allows accurate, relationship-based time analysis instead of relying on raw date columns.

---

## 🎯 Objective

- Track core ER performance metrics (patient volume, average wait time, satisfaction score, admission status) in one dashboard
- Enable proper year and month level analysis using a dedicated calendar table
- Build a dashboard that helps hospital management make faster staffing and resource decisions

---

## 🛠️ Tools & Techniques

| Technique | Purpose |
|---|---|
| Power Query | Built a standalone calendar table (Date, Month, Year) from scratch, used as the base for all time-based filtering |
| Power Pivot (Data Model) | Created a relationship between the raw patient data table and the calendar table, so calculations work correctly across both tables |
| Pivot Tables & Pivot Charts | Built on top of the data model to summarize admissions, wait times, and satisfaction scores |
| Slicers | Year and Month slicers connected through the data model, so all visuals filter together |
| Dashboard Design | KPI cards with sparklines, donut/pie charts, and bar charts combined into one MIS-style report |

**Why the data model matters:** connecting patient records to a separate calendar table (instead of just using raw dates) is what makes the Year/Month slicers filter everything on the dashboard correctly and consistently. This is the same basic idea behind time intelligence in BI tools like Power BI.

---

## 📊 Dashboard Highlights

**KPI Cards**
- 👥 No. of Patients
- ⏱️ Average Wait Time
- ⭐ Patient Satisfaction Score

📌 KPI cards update automatically based on whichever year and month is selected through the slicers, giving a quick, period-specific snapshot each time.

🖱️ Each KPI card also has a small embedded trend chart that's clickable. Clicking it opens a more detailed daily trend view (Patient Count, Wait Time, or Satisfaction Score) on a separate sheet, so users can drill down when needed instead of just seeing a summary number.

**Visual Breakdown**
| Chart | What it shows |
|---|---|
| 📅 Year & Month Slicers | Filters the entire dashboard across the 2023-2024 data model |
| 🥧 Patients Attended Within Time (Pie) | On-time vs. delayed treatment split |
| 🍩 Patients by Gender (Donut) | Gender distribution of patients |
| 📋 Admission Status Table | Admitted vs. Not Admitted with % breakdown |
| 📊 Patients by Age Group (Bar) | Volume distribution across 0-79 age bands |
| 📊 Patients by Department Referral (Bar) | Highest-demand departments |

---

## 🚀 Why This Project

I wanted to go beyond a basic "pivot table and chart" Excel project by actually applying data modeling concepts, the same relational thinking used in Power BI, but within Excel itself. This project reflects:

- Practical use of Power Query for building a table from scratch
- Setting up a relational data model (fact table + calendar table) instead of relying on a single flat table
- Turning a healthcare operations problem into a usable, decision-ready MIS report

---

## 📁 Repository Contents

```
├── Hospital_Emergency_Room_Project.xlsx     # Data model, calendar table, pivot analysis + dashboard
└── README.md                                 # Project documentation
```

---
