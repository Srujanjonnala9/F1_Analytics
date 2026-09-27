# F1_Analytics
# 🏎️ F1 Race Analytics

An end-to-end Formula 1 data analytics project analyzing **Miami and Abu Dhabi Grand Prix data from 2023–2025** using **FastF1, Python, Jupyter Notebook, PostgreSQL, SQL, and Power BI**.

The project extracts Formula 1 race data, processes and analyzes it using Python, pushes the processed tables to PostgreSQL, creates a consolidated database view by combining the required tables, and uses that view as the data source for interactive Power BI dashboards.

---

## 📌 Project Overview

Formula 1 produces a large amount of race and performance data. This project uses that data to analyze race performance across multiple seasons and Grand Prix events.

The project focuses on:

* **Miami Grand Prix**
* **Abu Dhabi Grand Prix**
* **2023–2025 seasons**

The complete workflow is:

**FastF1 → Jupyter Notebook → PostgreSQL → Power BI**

Python and Jupyter Notebook are responsible for both the data processing and the PostgreSQL integration.

---

# 🏗️ System Architecture

```text
┌──────────────────────────────┐
│           FastF1             │
│                              │
│   Formula 1 Race Data        │
│   Miami & Abu Dhabi          │
│   2023 – 2025                │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│     Jupyter Notebook         │
│          Python              │
│                              │
│ • Data Extraction            │
│ • Data Processing            │
│ • Data Analysis              │
│ • PostgreSQL Connection      │
│ • Push Tables to PostgreSQL  │
│ • Create Consolidated View   │
│ • UNION Multiple Tables      │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│         PostgreSQL           │
│                              │
│ • Stores Processed Tables    │
│ • Stores Consolidated View   │
│ • Central Data Source        │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│           Power BI           │
│                              │
│ • Interactive Dashboards     │
│ • Race Analysis              │
│ • Lap Analysis               │
│ • Sector Analysis            │
│ • Speed Analysis             │
│ • Driver Comparison          │
└──────────────────────────────┘
```

### Architecture Explanation

#### 1. FastF1

FastF1 is used to retrieve Formula 1 race data for the selected Grand Prix events and seasons.

**Data covered:**

* Miami Grand Prix — 2023–2025
* Abu Dhabi Grand Prix — 2023–2025

#### 2. Jupyter Notebook / Python

The main data workflow is performed in Python inside Jupyter Notebook.

Python is used to:

* Extract data using FastF1
* Process and prepare the datasets
* Perform data analysis
* Establish a connection to PostgreSQL using database credentials
* Push the processed datasets into PostgreSQL as tables
* Create a consolidated PostgreSQL view
* Use `UNION` to combine the required tables into a single dataset

Therefore, the PostgreSQL upload and consolidated-view creation are automated through the Python/Jupyter workflow.

#### 3. PostgreSQL

PostgreSQL acts as the database layer where the processed tables and consolidated view are stored.

The database contains:

* Processed race-data tables
* Consolidated view
* Combined dataset used for Power BI

#### 4. Power BI

Power BI connects to the **consolidated PostgreSQL view** and uses it as the primary data source for the interactive dashboards.

---

# 🔄 Data Pipeline

```text
F1 Race Data
     │
     ▼
   FastF1
     │
     ▼
Python / Jupyter Notebook
     │
     ├── Extract Data
     ├── Process Data
     ├── Analyze Data
     │
     ├── Connect to PostgreSQL
     │
     ├── Push Tables
     │
     └── Create View
            │
            └── UNION Tables
                    │
                    ▼
               PostgreSQL
                    │
                    │ Consolidated View
                    ▼
                 Power BI
                    │
                    ▼
            Interactive Dashboard
```

---

# 🎯 Project Objectives

* Extract Formula 1 race data using FastF1.
* Analyze Miami and Abu Dhabi Grand Prix data from 2023–2025.
* Process and prepare race datasets using Python.
* Automate the transfer of processed data into PostgreSQL.
* Create a consolidated PostgreSQL view using Python and SQL.
* Combine multiple tables using `UNION`.
* Use the consolidated view as a Power BI data source.
* Build interactive dashboards for Formula 1 race analysis.
* Analyze race, lap, sector, speed, and driver performance.

---

# 🛠️ Technologies Used

| Technology           | Purpose                                             |
| -------------------- | --------------------------------------------------- |
| **Python**           | Data processing, analysis, and database integration |
| **FastF1**           | Formula 1 data extraction                           |
| **Jupyter Notebook** | Development and analysis environment                |
| **PostgreSQL**       | Data storage and consolidated database view         |
| **SQL**              | Database operations and table consolidation         |
| **Power BI**         | Interactive data visualization                      |
| **DAX**              | Power BI calculations and measures                  |

---

# 📊 Data Analysis

The project analyzes Formula 1 data from multiple perspectives.

### 🏁 Race Performance

Analysis of race-level performance and comparison between drivers and races.

### ⏱️ Lap Analysis

Analysis of lap-level performance and lap times to understand race pace.

### 📐 Sector Analysis

Comparison of performance across:

* Sector 1
* Sector 2
* Sector 3

### ⚡ Speed Analysis

Analysis of speed-related metrics to understand performance across the circuit.

### 👤 Driver Comparison

Comparison of driver performance using different race and performance metrics.

---

# 📈 Power BI Dashboard

The consolidated PostgreSQL view is connected to Power BI to create interactive dashboards.

The dashboard provides:

* Interactive filters
* Driver comparisons
* Race-level analysis
* Lap analysis
* Sector performance analysis
* Speed analysis
* Interactive visualizations



---

# 🔗 Database Workflow

The PostgreSQL integration is automated through Python.

The workflow is:

```text
Python Code
     │
     │ PostgreSQL Credentials
     ▼
PostgreSQL Connection
     │
     ▼
Push Processed Tables
     │
     ▼
Create Consolidated View
     │
     ▼
UNION Required Tables
     │
     ▼
Consolidated View
     │
     ▼
Power BI
```

The consolidated view provides a single structured dataset for the Power BI dashboard.

---

# 📁 Project Structure

```text
F1-Race-Analytics/
│
├── README.md
│
├── notebooks/
│   └── F1_Race_Analytics.ipynb
│
├── sql/
│   └── queries.sql
│
├── powerbi/
│   └── F1_Race_Analytics.pbix
│
└── images/
    ├── architecture.png
    ├── dashboard-overview.png
    ├── race-performance.png
    ├── lap-analysis.png
    └── sector-speed-analysis.png
```

> Update the filenames above to match the actual files uploaded to the repository.

---

# 🚀 How the Project Works

### Step 1 — Extract Data

Run the Jupyter Notebook to retrieve the required Formula 1 data using FastF1.

### Step 2 — Process Data

The extracted datasets are processed and prepared using Python.

### Step 3 — Connect to PostgreSQL

The Python code establishes a PostgreSQL connection using the required database credentials.

### Step 4 — Push Tables

The processed datasets are pushed from Python into PostgreSQL as database tables.

### Step 5 — Create Consolidated View

The Python workflow creates a PostgreSQL view that combines the required tables using `UNION`.

### Step 6 — Connect Power BI

Power BI connects to the consolidated PostgreSQL view.

### Step 7 — Analyze and Visualize

The consolidated data is used to create interactive Power BI dashboards for race, lap, sector, speed, and driver analysis.

---

# 🔐 Database Credentials

Database credentials are required to execute the Python-to-PostgreSQL workflow.

**Do not publish real database passwords, API keys, or other sensitive credentials in the GitHub repository.**

Use your own local credentials when running the notebook.

---

# 📌 Key Features

* Formula 1 data extraction using FastF1
* Miami and Abu Dhabi Grand Prix analysis
* 2023–2025 data
* Python-based data processing
* Automated PostgreSQL table upload
* Automated consolidated-view creation
* Multiple-table `UNION`
* PostgreSQL-based data storage
* Power BI integration
* Interactive race analytics
* Lap, sector, speed, and driver analysis

---

# 📚 Project Outcome

This project demonstrates an end-to-end data analytics pipeline that transforms Formula 1 race data into an interactive analytical solution.

The workflow combines:

**FastF1 → Python/Jupyter → PostgreSQL → Power BI**

Python handles the data extraction, processing, PostgreSQL integration, table upload, and consolidated-view creation, while PostgreSQL provides the structured database layer and Power BI provides the final interactive visualization layer.

---

# 👤 Author

**Sai Srujan**


GitHub: https://github.com/Srujanjonnala9/

LinkedIn: https://www.linkedin.com/in/srujanj05/
