# 🏥 Hospital Emergency Room Dashboard

An interactive Excel MIS dashboard built to monitor hospital emergency
room performance: patient volume, wait times, treatment delays, and
satisfaction scores. The project uses a proper Power Pivot data model
instead of flat pivot tables, so the reporting is dynamic and time-based
filtering works correctly.

![Excel](https://img.shields.io/badge/Tool-Microsoft%20Excel-217346?style=flat&logo=microsoft-excel&logoColor=white) ![Power Pivot](https://img.shields.io/badge/Engine-Power%20Pivot-2C5F91?style=flat) ![VBA](https://img.shields.io/badge/Automation-VBA-217346?style=flat) ![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

------------------------------------------------------------------------

## 📌 Overview

Hospitals collect a huge amount of patient-level data every day:
admissions, wait times, treatment delays, and satisfaction feedback. On
their own, these raw records do not help staff make quick decisions.
This project converts 2023--2024 ER patient data into a live, filterable
MIS dashboard so hospital administrators can track service quality by
month and year without touching a single formula.

The main part of this project is the backend setup. Instead of using
flat pivot tables directly on raw data, I built a proper data model
using Power Query and Power Pivot, following the same relational
approach commonly used in BI tools such as Power BI. This allows
accurate, relationship-based time analysis instead of relying only on
raw date columns.

The dashboard also includes a **custom VBA-based interaction layer**.
Custom Excel Shapes are used as visual filter controls, and VBA code
connects those shape clicks to the underlying PivotTable/Slicer
filtering logic. This creates a cleaner and more customized dashboard
experience than relying only on the default Excel slicer interface.

------------------------------------------------------------------------

## 🎯 Objective

-   Track core ER performance metrics (patient volume, average wait
    time, satisfaction score, admission status) in one dashboard
-   Enable proper year and month level analysis using a dedicated
    calendar table
-   Build a dashboard that helps hospital management make faster
    staffing and resource decisions
-   Create a customized, interactive filtering experience using Excel
    Shapes and VBA

------------------------------------------------------------------------

## 🛠️ Tools & Techniques

  -----------------------------------------------------------------------
  Technique                           Purpose
  ----------------------------------- -----------------------------------
  **Power Query**                     Built a standalone calendar table
                                      (Date, Month, Year) from scratch
                                      and used it as the base for
                                      time-based filtering

  **Power Pivot (Data Model)**        Created relationships between the
                                      raw patient data table and the
                                      calendar table so calculations work
                                      correctly across both tables

  **Pivot Tables & Pivot Charts**     Built analysis for admissions, wait
                                      times, satisfaction scores, patient
                                      volume, and other ER metrics

  **Slicers**                         Used slicer functionality for
                                      interactive filtering across
                                      dashboard components

  **VBA (Macros)**                    Connected custom dashboard Shapes
                                      to PivotTable/Slicer filtering
                                      logic so clicking a Shape updates
                                      the selected period and refreshes
                                      the dashboard

  **Dashboard Design**                Combined KPI cards, sparklines,
                                      donut/pie charts, bar charts,
                                      tables, and custom filter controls
                                      into one MIS-style report
  -----------------------------------------------------------------------

### Why the Data Model Matters

Connecting patient records to a separate calendar table instead of
relying only on raw date columns makes the Year/Month filtering more
reliable and consistent across the dashboard.

This follows the same basic relational and time-intelligence concepts
used in BI tools such as Power BI.

------------------------------------------------------------------------

## 💻 VBA Automation & Custom Shape-Based Filters

One of the key features of this project is the use of **VBA to create a
custom slicer-like filtering experience**.

Instead of relying entirely on the default Excel slicer buttons, I
designed custom **Shapes** directly on the dashboard and assigned VBA
macros to them. These Shapes act as interactive controls for selecting
Year and Month.

When a user clicks a Shape:

1.  The assigned VBA macro identifies the selected filter.
2.  The corresponding PivotTable/Slicer filter is updated
    programmatically.
3.  The underlying PivotTable analysis is refreshed.
4.  Connected dashboard visuals update automatically.
5.  KPI cards, charts, and trend views reflect the newly selected
    period.

### Why VBA Was Used

The default Excel slicer interface provides limited control over the
visual design. Using **Shapes + VBA** makes it possible to create a more
customized MIS dashboard interface while keeping the underlying Power
Pivot data model intact.

The VBA layer essentially acts as an **interaction layer between the
dashboard UI and the underlying Excel data model**.

### Dashboard Interaction Flow

``` text
Shape Click
    ↓
VBA Macro
    ↓
PivotTable / Slicer Filter
    ↓
Data Refresh
    ↓
KPI & Charts Update
    ↓
Interactive Dashboard
```

This approach combines Excel's analytical capabilities with a
lightweight custom user interface.

------------------------------------------------------------------------

## 📊 Dashboard Highlights

### 📌 KPI Cards

-   👥 No. of Patients
-   ⏱️ Average Wait Time
-   ⭐ Patient Satisfaction Score

KPI cards update automatically based on the selected year and month,
providing a quick period-specific snapshot.

Each KPI card also includes a small embedded trend chart that can be
used to access a more detailed daily trend view for:

-   Patient Count
-   Wait Time
-   Satisfaction Score

This allows users to move from a high-level summary to a more detailed
analysis when required.

------------------------------------------------------------------------

### 🖱️ Custom Shape-Based Filters

The Year and Month controls are custom-designed **Excel Shapes** rather
than standard slicer buttons.

Each Shape is connected to a VBA macro. When the user clicks a Shape,
the macro updates the corresponding PivotTable/Slicer filter and the
dashboard refreshes automatically.

This provides:

-   Cleaner dashboard navigation
-   Customized filter design
-   Better control over dashboard appearance
-   Programmatic interaction with PivotTables
-   A more application-like Excel experience

------------------------------------------------------------------------

### 📈 Visual Breakdown

  -----------------------------------------------------------------------
  Chart / Control                     What it shows
  ----------------------------------- -----------------------------------
  📅 Year & Month Controls            Filters the dashboard across the
                                      2023--2024 data model

  🥧 Patients Attended Within Time    On-time vs. delayed treatment split

  🍩 Patients by Gender               Gender distribution of patients

  📋 Admission Status Table           Admitted vs. Not Admitted with
                                      percentage breakdown

  📊 Patients by Age Group            Patient volume distribution across
                                      age bands

  📊 Patients by Department Referral  Highest-demand departments

  📈 KPI Trend Charts                 Daily trends for patient count, wait time, and satisfaction

------------------------------------------------------------------------

## 🔄 Dashboard Architecture

The project follows a layered architecture that separates data
preparation, data modeling, analysis, and user interaction.

``` text
Raw Patient Data
       ↓
Power Query
       ↓
Calendar Table
       ↓
Power Pivot Data Model
       ↓
Relationships & Measures
       ↓
PivotTables / Pivot Charts
       ↓
VBA Interaction Layer
       ↓
Custom Shape-Based Filters
       ↓
Interactive MIS Dashboard
```

This architecture makes the dashboard more structured and maintainable
than a traditional formula-heavy Excel report.

------------------------------------------------------------------------

## 🚀 Why This Project

I wanted to go beyond a basic "pivot table and chart" Excel project by
applying data modeling concepts and VBA automation within Excel itself.

This project demonstrates:

-   Practical use of **Power Query**
-   Creation of a standalone **Calendar/Date table**
-   Building a relational **Power Pivot Data Model**
-   Fact table + calendar table architecture
-   PivotTables and Pivot Charts built on top of the data model
-   Interactive dashboard filtering
-   **VBA automation**
-   Custom Shape-based controls
-   Dynamic KPI reporting
-   Dashboard UI/UX design
-   Healthcare operations analysis
-   Decision-ready MIS reporting

The combination of **Power Query + Power Pivot + PivotTables + VBA +
Dashboard Design** makes this more than a basic Excel reporting project.

------------------------------------------------------------------------

## 📁 Repository Contents

``` text
├── Hospital_Emergency_Room_Project.xlsm
│   # Excel dashboard containing the data model, calendar table,
│   # PivotTables, dashboard, custom Shapes, and VBA automation
│
└── README.md
   # Project documentation
```

> **Important:** Because the project contains VBA macros, the workbook
> should be saved as **`.xlsm` (Excel Macro-Enabled Workbook)** rather
> than `.xlsx`. The `.xlsx` format does not preserve embedded VBA
> macros.

------------------------------------------------------------------------

## ▶️ How to Use

1.  Download the `.xlsm` workbook from this repository.
2.  Open the file in Microsoft Excel.
3.  If Excel displays a security warning, click **Enable Content /
    Enable Macros** if you trust the workbook.
4.  Open the dashboard sheet.
5.  Use the custom Year and Month Shapes to filter the dashboard.
6.  Click the available KPI/trend controls to explore detailed views.
7.  All connected PivotTables and dashboard visuals update based on the
    selected period.

------------------------------------------------------------------------

## 🧩 Key Learning Outcomes

Through this project, I applied several concepts that are useful beyond
traditional Excel reporting:

-   Data transformation with Power Query
-   Relational data modeling
-   Calendar table design
-   Power Pivot relationships
-   Pivot-based analytics
-   Interactive dashboard design
-   VBA event/macro-driven interaction
-   Custom Shape-based UI controls
-   Dynamic filtering and dashboard refresh
-   MIS reporting and business decision support

------------------------------------------------------------------------

## 📌 Project Summary

**Hospital Emergency Room Dashboard** is an Excel-based healthcare MIS
solution that combines data preparation, relational modeling, analytics,
visualization, and VBA automation into a single interactive reporting
system.

The goal was not only to visualize hospital data, but to build a
dashboard where the **data model handles the analysis and VBA handles
the user interaction**, creating a more dynamic and professional Excel
BI experience.
