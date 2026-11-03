# 📊 Credit Operations MIS Dashboard
### Excel | Power Query | Power BI | DAX

An interactive **Credit Operations Management Information System (MIS) Dashboard** built to analyse loan application processing, monitor operational performance, and generate meaningful business insights.

This project simulates a financial services reporting environment, transforming raw loan application data into an interactive dashboard that helps management monitor application volumes, loan amounts, processing turnaround time (TAT), and analyst productivity.

---

## 📌 Project Overview

Credit Operations teams handle large volumes of loan applications and need accurate reporting to monitor daily operations, identify processing delays, and track team performance.

The objective of this project was to simulate that reporting process by cleaning raw application data, performing operational analysis, and developing an interactive Power BI dashboard.

## 🎯 Project Objectives

- Monitor overall loan application volumes.
- Analyse application statuses and approval trends.
- Track loan amounts across different cities.
- Monitor monthly application volumes.
- Evaluate analyst-wise workload and productivity.
- Measure average processing turnaround time (TAT).
- Highlight applications with unassigned analysts.

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| Microsoft Excel | Data inspection and initial analysis |
| Power Query | Data cleaning and transformation |
| Power BI Desktop | Interactive dashboard development |
| DAX | Calculated measures and KPIs |
| Pivot Tables | Operational summaries and analysis |

## 🧹 Data Cleaning & Preparation

The simulated dataset contains approximately 10,000 loan application records.

Data preparation was performed using Excel Power Query.

Key activities included:

- Removed duplicate application records.
- Standardized city names, analyst names, and application statuses.
- Cleaned currency values and converted loan amounts into numeric format.
- Standardized application date formats.
- Identified and handled missing values.
- Retained unassigned analyst records under the category **Unassigned**.
- Verified appropriate data types for analysis.

After duplicate removal, the dataset contained 9,990 records.

## 📈 Dashboard Features

The Power BI dashboard provides an overview of credit operations through the following visualizations:

| Visualization | Business Purpose |
|---|---|
| Total Applications | Monitor overall application volume |
| Total Loan Amount | Track the value of loan applications |
| Approved Applications | Monitor approval volumes |
| Average TAT | Measure average processing time |
| Application Status | Analyse approved, pending, rejected, and on-hold applications |
| Loan Amount by City | Compare loan amounts across locations |
| Monthly Application Trend | Track application volumes over time |
| Analyst Performance | Compare application workloads across analysts |
| Average TAT by Analyst | Evaluate processing turnaround time by analyst |

### Interactive Filters

The dashboard includes interactive filtering capabilities to explore data across different business dimensions, including loan product, city, and application status.

## 🧮 Key DAX Measures

Examples of the measures developed for the dashboard:

**1. Total Applications**
```dax
Total Applications =
DISTINCTCOUNT(Clean_data[Application_ID])
```

**2. Total Loan Amount**
```dax
Total Loan Amount =
SUM(Clean_data[Loan_Amount_INR])
```

**3. Average Processing TAT**
```dax
Average TAT =
AVERAGE(Clean_data[Processing_TAT_Days])
```

**4. Approved Applications**
```dax
Approved Applications =
CALCULATE(
    [Total Applications],
    Clean_data[Application_Status] = "Approved"
)
```

**5. Unassigned Applications**
```dax
Unassigned Applications =
CALCULATE(
    [Total Applications],
    Clean_data[Assigned_Analyst] = "Unassigned"
)
```

## 💡 Business Insights

The dashboard helps identify and monitor operational patterns such as:

- Application distribution across different cities.
- Approval, rejection, pending, and on-hold application volumes.
- Differences in analyst workloads.
- Average processing turnaround time across analysts.
- Applications requiring analyst allocation.
- Monthly fluctuations in application volumes.

These insights can support workload monitoring, operational reviews, and management reporting.

## 📂 Dataset Structure

The dataset contains the following fields:

| Column | Description |
|---|---|
| Application_ID | Unique application reference |
| Application_Date | Date of application |
| Applicant_City | Applicant's city |
| Loan_Product | Type of loan |
| Loan_Amount_INR | Loan amount in INR |
| Assigned_Analyst | Analyst responsible for processing |
| Application_Status | Current application status |
| Processing_TAT_Days | Processing turnaround time in days |

## 📁 Project Structure

```text
Credit-Operations-MIS/
│
├── Dataset/
│   └── Credit_Operations_Data.xlsx
│
├── Dashboard/
│   └── Credit_Operations_MIS.pbix
│
├── Screenshots/
│   └── Dashboard_Preview.png
│
└── README.md
```

*Adjust the filenames and folders to match your actual GitHub repository.*

## ⚠️ Disclaimer

This project uses entirely synthetic, mock data created for learning and portfolio demonstration purposes. It does not contain actual customer records or represent the operational performance of any financial institution.

## 👨‍💻 Skills Demonstrated

- Data Cleaning & Transformation
- Microsoft Excel
- Power Query
- Power BI Dashboard Development
- DAX Calculations
- Data Visualization
- MIS Reporting
- Operational Performance Analysis
- Business Intelligence

---

**Project Type:** Data Analytics | Financial Services | Credit Operations MIS

**Status:** Completed

*Built as a practical portfolio project to demonstrate data preparation, reporting, and business intelligence capabilities.*
