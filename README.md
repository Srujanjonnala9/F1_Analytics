# 🏎️ F1 Race Analytics

An end-to-end Formula 1 data analytics project analyzing **Miami and Abu Dhabi Grand Prix data from 2023–2025** using **FastF1, Python, Jupyter Notebook, PostgreSQL, SQL, and Power BI**.

The project extracts Formula 1 race data, processes and analyzes it using Python, pushes the processed tables to PostgreSQL, creates a consolidated view by combining the required tables using `UNION`, and uses the consolidated view as the data source for interactive Power BI dashboards.

---

## 📌 Project Overview

Formula 1 generates a large amount of race and performance data. This project uses that data to analyze race performance across multiple seasons and Grand Prix events.

The project focuses on:

- 🏁 **Miami Grand Prix**
- 🏁 **Abu Dhabi Grand Prix**
- 📅 **2023–2025 seasons**

The complete data pipeline is:

**FastF1 → Jupyter Notebook / Python → PostgreSQL → Power BI**

Python and Jupyter Notebook handle the data extraction, processing, PostgreSQL integration, table upload, and consolidated-view creation.

---

# 🏗️ System Architecture

<p align="center">
  <img src="https://drive.google.com/uc?export=view&id=1HHEYujTVXl5BBUCKahZZ7WNS_9pj930u" alt="F1 Race Analytics System Architecture" width="900">
</p>

### Architecture Flow

**FastF1 → Jupyter Notebook → PostgreSQL → Power BI**

### FastF1

Used to extract Formula 1 race data for the selected Grand Prix events and seasons.

### Jupyter Notebook / Python

The main processing layer of the project.

Python is used to:

- Extract data using FastF1
- Process and prepare datasets
- Perform data analysis
- Connect to PostgreSQL
- Push processed datasets into PostgreSQL as tables
- Create the consolidated database view
- Combine the required tables using `UNION`

### PostgreSQL

Acts as the database layer.

It stores:

- Processed race-data tables
- Consolidated view
- Combined dataset used by Power BI

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
