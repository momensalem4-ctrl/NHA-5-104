
# Multi-Source Job Market Data Analysis (Team: NHA-5-S2-104)

An end-to-end **Data Engineering, Data Warehousing, and Business Intelligence** project analyzing **28,211 job postings** across multiple platforms (**Greenhouse, Lever, and RemoteOK**) to uncover hiring trends, in-demand skills, salary benchmarks, and work-mode distributions.

---

## Project Architecture & Workflow

**Raw Data (`Api_df_Max_Live.csv`)** ➔ **Python ETL Pipeline (Cleaning & Skill Parsing)** ➔ **SQL Server Star-Schema Warehouse (Medallion: Bronze / Silver / Gold)** ➔ **SQL Analytical Views** ➔ **Interactive Power BI Dashboard**

---

## Technologies Used

* **Python (`pandas`, `NumPy`, `SQLAlchemy`, `pyodbc`, `matplotlib`, `seaborn`):** Data profiling, cleaning, skill extraction, EDA, and automated database loading.
* **SQL Server 2022 & SSMS (T-SQL):** Medallion architecture (`Bronze`, `Silver`, `Gold`), Star Schema design (`Fact_JobPosting`, `Dim_Date`, `Dim_Job`, `Dim_Company`, `Dim_Location`, `Dim_Skill`, `Dim_Source`, `Bridge_JobSkill`), Stored Procedures, and Reporting Views.
* **Microsoft Power BI:** Semantic data modeling, DAX measures, interactive dashboards, and drill-through job details.
* **Git & GitHub:** Version control and collaborative workflow.

---

## Repository Structure

```text
NHA-5-104/
├── data/
│   ├── raw/          # Original dataset (Api_df_Max_Live.csv)
│   └── processed/    # Cleaned datasets ready for warehouse loading
├── notebooks/        # Data profiling & Python EDA notebooks
├── scripts/          # Modular Python ETL scripts
├── sql/
│   ├── ddl/          # Star-schema table creation scripts
│   ├── procedures/   # Warehouse load stored procedures
│   └── analysis/     # Business question queries & reporting views
├── powerbi/          # Power BI dashboard file (.pbix)
└── docs/             # Project proposal, data dictionary, & final report
```
