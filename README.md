<div align="center">

# 🏥 Healthcare Data Cleaning, Analysis & Power BI Dashboard

**A portfolio project built with PostgreSQL, Python, Docker, and Power BI to load, clean, analyze, and visualize healthcare data end-to-end.**

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-336791?style=flat-square&logo=postgresql&logoColor=white)](https://www.postgresql.org/)
[![Docker](https://img.shields.io/badge/Docker-Compose-2496ED?style=flat-square&logo=docker&logoColor=white)](https://www.docker.com/)
[![Power BI](https://img.shields.io/badge/Power_BI-Dashboard-F2C811?style=flat-square&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)

[Overview](#-overview) · [Features](#-features) · [Tech Stack](#-tech-stack) · [Workflow](#-workflow) · [Getting Started](#-getting-started) · [Data Sources](#-data-sources) · [Files Included](#-files-included) · [Results](#-results) · [Author](#-author)

![Dashboard Preview](assets/dashboard sample image.png)

</div>

---

## 📌 Overview

This project was built to practice **Docker**, **PostgreSQL**, **data ingestion with Python**, and **Power BI dashboarding**.

The workflow starts by spinning up a **PostgreSQL** database and **PgAdmin4** with Docker, then using **Python (SQLAlchemy)** to load the healthcare dataset into the database. After that, the data is cleaned and explored in PostgreSQL, and finally connected to **Power BI** to build an interactive dashboard.

It is a practical end-to-end portfolio project focused on data engineering basics, SQL cleaning, and business intelligence visualization.

---

## ✨ Features

### 🗄️ Dockerized Database Setup
- PostgreSQL and PgAdmin4 run inside Docker containers
- Easy and repeatable local environment setup
- Convenient for learning container-based workflows

### 🐍 Python Data Ingestion
- Uses **Python + SQLAlchemy** to load CSV data into PostgreSQL
- Simple and reliable ingestion pipeline
- Designed for structured tabular healthcare data

### 🧹 Data Cleaning and Exploration in SQL
- Cleans and transforms the loaded dataset in PostgreSQL
- Adds useful derived columns such as:
  - **Days in hospital**
  - **Age group**
- Supports analysis directly in the database

### 📊 Power BI Dashboard
- Connects PostgreSQL to Power BI
- Visualizes patient and hospital data in an interactive dashboard
- Designed for exploration and reporting

### 📈 Healthcare Data Analysis
- Works with patient demographic and clinical data
- Useful for studying patterns such as:
  - Age distribution
  - Medical conditions
  - Billing amounts
  - Admission and discharge trends

---

## 🛠 Tech Stack

| Layer | Technology |
|---|---|
| **Language** | Python 3.x |
| **Database** | PostgreSQL |
| **Database UI** | PgAdmin4 |
| **Containerization** | Docker, Docker Compose |
| **Data Ingestion** | SQLAlchemy |
| **Visualization** | Power BI |

---

## 🔄 Workflow

The project follows this pipeline:

```text
healthcare_dataset.csv
        ↓
Python (SQLAlchemy ingestion)
        ↓
PostgreSQL database in Docker
        ↓
SQL cleaning and exploration in PgAdmin4
        ↓
Derived columns and analysis
        ↓
Power BI connection
        ↓
Interactive healthcare dashboard
```

The dataset is first loaded into PostgreSQL, then cleaned and enriched using SQL before being visualized in Power BI.

---

## 🚀 Getting Started

### 1️⃣ Clone the Repository

```bash
git clone <your-repository-link>
cd <your-project-folder>
```

### 2️⃣ Start PostgreSQL and PgAdmin4

```bash
docker-compose up -d
```

This starts the database services defined in `docker-compose.yml`.

### 3️⃣ Install Python Dependencies

```bash
pip install -r requirements.txt
```

### 4️⃣ Load the Dataset into PostgreSQL

```bash
python healthcare-ingest.py
```

### 5️⃣ Run SQL Cleaning and Exploration

Open `cleaning_exploration.sql` in PgAdmin4 or your SQL editor and run the queries to clean, analyze, and enrich the data.

### 6️⃣ Build or Refresh the Power BI Dashboard

Connect Power BI to the PostgreSQL database and import the cleaned tables or views.

---

## 📂 Data Sources

**`healthcare_dataset.csv`** is the main dataset used in this project.

The dataset was downloaded from **Kaggle** and contains **10,000 rows** of patient information, including:

- Name
- Age
- Gender
- Blood Type
- Medical Condition
- Date of Admission
- Doctor
- Hospital
- Insurance Provider
- Billing Amount
- Room Number
- Admission Type
- Discharge Date
- Medication
- Test Results

Additional columns created in PostgreSQL:

- **Days in hospital**
- **Age group**

---

## 📁 Files Included

### `docker-compose.yml`
Defines the Docker services required to run:
- PostgreSQL
- PgAdmin4

### `healthcare-ingest.py`
Python script used to:
- Read `healthcare_dataset.csv`
- Connect to PostgreSQL with SQLAlchemy
- Load the dataset into the database

### `cleaning_exploration.sql`
SQL script used to:
- Clean the data
- Perform analysis
- Add derived columns
- Prepare data for Power BI

---

## 🎯 Results

This project helped me strengthen my skills in:

- Docker and Docker Compose
- PostgreSQL cleaning and analysis
- Python-based data ingestion with SQLAlchemy
- Connecting PostgreSQL to Power BI
- Building an interactive healthcare dashboard

---

## 👩‍💻 Author

**Ria Chadha**

---
