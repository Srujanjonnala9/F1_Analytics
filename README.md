# 🏎️ F1 Race Analytics

An end-to-end Formula 1 data analytics project analyzing **Miami and Abu Dhabi Grand Prix data from 2023–2025** using **FastF1, Python, Jupyter Notebook, PostgreSQL, SQL, and Power BI**.

The project extracts Formula 1 race data, processes and analyzes it using Python, pushes the processed tables to PostgreSQL, creates a consolidated view by combining the required tables using `UNION`, and uses the consolidated view as the data source for interactive Power BI dashboards.

---

## 📌 Project Overview

Formula 1 generates a large amount of race and performance data. This project uses that data to analyze race performance across multiple seasons and Grand Prix events.

The project focuses on:

* 🏁 **Miami Grand Prix**
* 🏁 **Abu Dhabi Grand Prix**
* 📅 **2023–2025 seasons**

The complete data pipeline is:

**FastF1 → Jupyter Notebook / Python → PostgreSQL → Power BI**

Python and Jupyter Notebook handle the data extraction, processing, PostgreSQL integration, table upload, and consolidated-view creation.

---

# 🏗️ System Architecture

<p align="center">
  <img src="images/architecture.png" alt="F1 Race Analytics System Architecture" width="900">
</p>

### Architecture Flow

**FastF1 → Jupyter Notebook → PostgreSQL → Power BI**

### FastF1

Used to extract Formula 1 race data for the selected Grand Prix events and seasons.

### Jupyter Notebook / Python

The main processing layer of the project.

Python is used to:

* Extract data using FastF1
* Process and prepare datasets
* Perform data analysis
* Connect to PostgreSQL
* Push processed datasets into PostgreSQL as tables
* Create the consolidated database view
* Combine the required tables using `UNION`

### PostgreSQL

Acts as the database layer.

It stores:

* Processed race-data tables
* Consolidated view
* Combined dataset used by Power BI

### Power BI

Connects to the consolidated PostgreSQL view and provides the interactive visualization layer.

---

# 🔄 Data Pipeline

```text
F1 Race Data
      │
      ▼
   FastF1
      │
      ▼
Jupyter Notebook / Python
      │
      ├── Data Extraction
      ├── Data Processing
      ├── Data Analysis
      │
      ├── PostgreSQL Connection
      ├── Push Tables
      │
      └── Create Consolidated View
                 │
                 └── UNION Required Tables
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
* Perform exploratory and analytical operations using Jupyter Notebook.
* Connect Python to PostgreSQL.
* Push processed datasets into PostgreSQL as tables.
* Create a consolidated database view through Python.
* Combine the required tables using `UNION`.
* Use the consolidated view as the Power BI data source.
* Build interactive dashboards for Formula 1 race analysis.
* Analyze race, lap, sector, speed, and driver performance.

---

# 🛠️ Technologies Used

| Technology              | Purpose                                             |
| ----------------------- | --------------------------------------------------- |
| 🐍 **Python**           | Data processing, analysis, and database integration |
| 🏎️ **FastF1**          | Formula 1 data extraction                           |
| 📓 **Jupyter Notebook** | Development, processing, and analysis               |
| 🐘 **PostgreSQL**       | Data storage and consolidated database view         |
| 🗄️ **SQL**             | Database operations and table consolidation         |
| 📊 **Power BI**         | Interactive data visualization                      |
| 📐 **DAX**              | Power BI calculations and measures                  |

---

# 📊 Data Source

The project uses Formula 1 data extracted through the **FastF1 Python library**.

### Grand Prix Events

* Miami Grand Prix
* Abu Dhabi Grand Prix

### Seasons

* 2023
* 2024
* 2025

The extracted data is processed in Python before being pushed into PostgreSQL.

---

# 🔧 Data Processing & Database Integration

The data-processing workflow is performed directly through Python in Jupyter Notebook.

### Step 1 — Data Extraction

FastF1 is used to retrieve the required Formula 1 race data.

### Step 2 — Data Processing

The extracted data is processed and prepared using Python.

### Step 3 — PostgreSQL Connection

The Python code establishes a connection to PostgreSQL using the required database credentials.

### Step 4 — Push Tables

The processed datasets are pushed from Python into PostgreSQL as database tables.

### Step 5 — Create Consolidated View

The Python workflow creates a PostgreSQL view.

The view uses `UNION` to combine the required tables into a single consolidated dataset.

### Step 6 — Power BI Connection

Power BI connects directly to the consolidated PostgreSQL view.

---

# 📈 Dashboard Analysis

The consolidated PostgreSQL view is used to build interactive Power BI dashboards.

The dashboard covers multiple areas of Formula 1 analysis.

## 🏁 Race Performance Analysis

Provides race-level performance insights and enables comparisons across drivers and races.

## ⏱️ Lap Analysis

Analyzes lap-level performance and lap times to understand race pace.

## 📐 Sector Analysis

Analyzes performance across the three circuit sectors:

* Sector 1
* Sector 2
* Sector 3

## ⚡ Speed Analysis

Analyzes speed-related metrics to understand performance across different parts of the circuit.

## 👤 Driver Comparison

Provides comparison of driver performance using different race and performance metrics.

---

# 📊 Power BI Dashboard

The PostgreSQL consolidated view is connected to Power BI to create interactive dashboards.

The dashboard includes:

* Interactive filters
* Driver comparisons
* Race-level analysis
* Lap analysis
* Sector analysis
* Speed analysis
* Interactive visualizations

### Dashboard Preview

<p align="center">
  <img src="<img width="1375" height="764" alt="Architecture Diagram_F1" src="https://github.com/user-attachments/assets/84d8b55c-ed14-4b39-95bc-1ae96cb499dd" />
" alt="F1 Race Analytics Dashboard" width="900">
</p>

> Add additional dashboard screenshots to the `images` folder as needed.

---

# 🔗 End-to-End Workflow

```text
┌──────────────┐
│    FastF1    │
└──────┬───────┘
       │
       │ Extract F1 Data
       ▼
┌──────────────────────┐
│ Jupyter / Python     │
│                      │
│ • Process Data       │
│ • Analyze Data       │
│ • Connect PostgreSQL │
│ • Push Tables        │
│ • Create View        │
│ • UNION Tables       │
└──────────┬───────────┘
           │
           ▼
┌──────────────────────┐
│     PostgreSQL       │
│                      │
│ • Store Tables       │
│ • Store View         │
│ • Consolidated Data  │
└──────────┬───────────┘
           │
           │ Consolidated View
           ▼
┌──────────────────────┐
│       Power BI       │
│                      │
│ • Race Analysis      │
│ • Lap Analysis       │
│ • Sector Analysis    │
│ • Speed Analysis     │
│ • Driver Comparison  │
└──────────────────────┘
```

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
    └── dashboard-overview.png
```

> Update the filenames to match the actual files in your repository.

---

# 🚀 How to Run the Project

## 1. Run the Jupyter Notebook

Open the `.ipynb` file in Jupyter Notebook or JupyterLab.

Run the Python workflow to:

1. Extract Formula 1 data using FastF1.
2. Process the datasets.
3. Perform the required analysis.
4. Connect to PostgreSQL.
5. Push the processed tables into PostgreSQL.
6. Create the consolidated view.
7. Combine the required tables using `UNION`.

## 2. PostgreSQL

Ensure PostgreSQL is running and the required database is available.

The Python code establishes the database connection and creates/populates the required tables and consolidated view.

## 3. Power BI

Open the Power BI `.pbix` file and connect/refresh the PostgreSQL data source if required.

The dashboard uses the consolidated PostgreSQL view for visualization.

---

# 🔐 Credentials & Security

The project requires database credentials to establish the Python-to-PostgreSQL connection.

**Never commit real passwords, API keys, database credentials, or other sensitive information to a public GitHub repository.**

Use your own local credentials when running the project.

---

# ⭐ Key Features

* 🏎️ Formula 1 race data extraction using FastF1
* 📅 Miami and Abu Dhabi Grand Prix analysis
* 📊 2023–2025 race data
* 🐍 Python-based data processing
* 📓 Jupyter Notebook analysis
* 🐘 PostgreSQL database integration
* 🔄 Automated table upload from Python
* 🔗 Consolidated PostgreSQL view
* 🔀 Multiple-table `UNION`
* 📊 Power BI interactive dashboards
* ⏱️ Lap analysis
* 📐 Sector analysis
* ⚡ Speed analysis
* 👤 Driver comparison

---

# 📚 Project Outcome

This project demonstrates an end-to-end data analytics pipeline that transforms Formula 1 race data into an interactive analytical solution.

The workflow combines:

**FastF1 → Python/Jupyter → PostgreSQL → Power BI**

Python handles the data extraction, processing, analysis, PostgreSQL connection, table upload, and consolidated-view creation.

PostgreSQL provides the structured database layer for storing the processed tables and consolidated view, while Power BI uses the consolidated view to deliver interactive Formula 1 analytics.

---

# 👤 Author

**Srujan**

B.Tech — Computer Science Engineering

* GitHub: [Add your GitHub profile link]
* LinkedIn: [Add your LinkedIn profile link]
