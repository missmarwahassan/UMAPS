Here’s a clean, GitHub-ready `README.md` in your voice—structured, concise, and polished for a project repo.

---

# UMAPS Scholars Explorer

An interactive data exploration app for the **University of Michigan African Presidential Scholars (UMAPS)** program. This tool allows users to explore scholar participation over time, filter by country and cohort, and analyze trends in the program’s global reach.

---

## Overview

This project builds a full data pipeline and interactive app:

* Cleans and standardizes alumni and survey data
* Constructs a relational database using DuckDB
* Provides a Streamlit interface for filtering and exploration
* Visualizes participation trends across countries and cohorts

The goal is to make UMAPS data more accessible, searchable, and analyzable for program staff and stakeholders.

---

## Features

* Search scholars by name or email
* Filter by cohort year range
* Filter by country of origin
* View participation counts and summary metrics
* Explore country-level participation trends over time
* Interactive table and chart views

---

## Tech Stack

* **Python**
* **Streamlit** (frontend app)
* **DuckDB** (database)
* **Pandas** (data cleaning + transformation)
* **Altair** (visualization)
* **pycountry** (country standardization)

---

## Project Structure

```bash
umaps_app/
│
├── app.py                  # Streamlit application
├── build_db.py             # Data pipeline and database builder
├── umaps.db                # Built DuckDB database (generated)
├── requirements.txt
│
└── data/
    ├── UMAPS Alumni Data-3.xlsx
    └── UMAPS Alumni_February 28, 2026_22.02.xlsx
```

---

## Setup & Installation

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/umaps-app.git
cd umaps-app
```

### 2. Create and activate a virtual environment

```bash
python -m venv venv
source venv/bin/activate  # macOS/Linux
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

---

## Build the Database

Run the data pipeline to generate the DuckDB database:

```bash
python build_db.py
```

This will:

* Clean and normalize alumni data
* Parse cohort years and metadata
* Link survey responses to scholars
* Output `umaps.db`

---

## Run the App

```bash
streamlit run app.py
```

The app will open in your browser.

---

## Deployment

This app is designed for deployment via **Streamlit Community Cloud**.

### Key Notes:

* Ensure `umaps.db` is included in the repository
* The app reads directly from the database (no rebuild in cloud)
* All paths are handled relative to the project directory

---

## Data Notes

* Cohort year is extracted from text fields (e.g., “Fall 2024”)
* Country names are standardized using `pycountry`
* Scholar identities are deduplicated using email or name + cohort

---

## Future Improvements

* Add choropleth world map (with ISO country codes)
* Improve survey response linking
* Add cohort semester filtering
* Build search indexing for faster queries
* Expand visualizations (time series, host networks)

---

## Author

Marwa Hassan
MSI Candidate, University of Michigan School of Information
Academic Program Specialist, African Studies Center

---

## Acknowledgments

* University of Michigan African Studies Center
* UMAPS Program
* Data sources: internal alumni records + Qualtrics survey

---

If you want, I can tighten this further for a portfolio version or add a “✨ Key Insight / Impact” section (which looks really strong for recruiters).
