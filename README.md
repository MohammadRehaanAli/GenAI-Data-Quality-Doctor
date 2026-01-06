

---

# GenAI Data Quality Doctor

GenAI Data Quality Doctor is a web-based data quality tool that helps analyze, diagnose, and clean messy datasets using automated checks and GenAI-powered recommendations.

The idea behind this project came from a very real problem I noticed while working on data analytics projects — **most of the time is spent cleaning data**, not analyzing it. Before building dashboards or insights, analysts usually deal with missing values, inconsistent categories, wrong data types, duplicates, and outliers. This project focuses on solving that exact problem.

Instead of manually switching between Python scripts, notebooks, and spreadsheets, this tool provides **one place to upload a dataset, identify issues, and understand how to fix them**.

---

## What This Project Does

The application allows users to upload a CSV file and automatically performs:

* Dataset profiling (rows, columns, data types)
* Detection of common data quality issues
* Generation of human-readable cleaning recommendations using GenAI
* Calculation of a data quality score
* Before–after comparison after applying fixes
* Export of cleaned datasets and reports

The goal is not just to clean data once, but to **standardize and automate the data quality checking process**.

---

## Key Features

### Dataset Upload

Users can upload any CSV file through a simple drag-and-drop interface. The file is parsed and analyzed on the backend.

### Automated Data Quality Checks

The system detects common real-world data problems such as:

* Missing or empty values
* Duplicate rows or identifiers
* Invalid numeric values (e.g., text in numeric columns)
* Outliers in numerical data
* Inconsistent categorical values (case or spelling variations)

### GenAI-Based Recommendations

Using Gemini AI, the app generates:

* A natural-language summary of detected issues
* Clear cleaning recommendations at dataset and column level
* Practical suggestions that explain *why* a fix is needed

### Data Quality Scoring

Each dataset is assigned a quality score (0–100) based on the number and severity of detected issues. This makes it easy to understand how clean or risky a dataset is at a glance.

### Auto-Fixes (Basic)

For common issues, the user can apply simple automated fixes such as:

* Removing duplicate rows
* Handling missing values
* Re-evaluating numeric columns

After applying fixes, the dataset is re-analyzed to show improvements in quality.

### Dashboard-Style UI

The app uses a professional dark-themed dashboard layout with:

* Summary cards (rows, columns, issues, quality score)
* Tabs for issues, profiling, AI recommendations, and fixes
* Clear visual feedback for before–after comparisons

### History Tracking

Uploaded datasets and analysis results are stored so users can view previous runs and compare results over time.

---

## Tech Stack

* **Frontend:** React, TypeScript, Tailwind CSS
* **Backend:** FastAPI (Python)
* **Database:** MongoDB (for upload history and metadata)
* **AI / GenAI:** Gemini AI (via Emergent LLM integration)
* **Data Processing:** Pandas, basic statistical checks
* **Deployment:** Emergent platform

---

## Why This Project Is Different

Many AI tools can *suggest* how to clean data, but they usually work as one-time interactions. This project focuses on building a **repeatable, automated system**:

* No manual prompt writing for every dataset
* Structured issue detection instead of ad-hoc analysis
* Clear separation between profiling, validation, and recommendations
* Designed like an internal analytics tool, not a demo notebook

This makes it closer to how data quality is handled in real teams and companies.

---

## Example Use Cases

* Data analysts preparing datasets before building dashboards
* Business teams validating CSV reports before decision-making
* Students learning real-world data quality challenges
* Small teams that don’t have a dedicated data engineer

---

## Limitations & Future Improvements

This project is still evolving. Planned improvements include:

* Stronger categorical similarity detection
* Configurable validation rules per dataset
* Scheduled data quality checks
* Deeper Power BI integration
* More advanced auto-fix strategies

The current version focuses on building a solid foundation and realistic workflow.

---

## How to Run (High Level)

1. Clone the repository
2. Install frontend and backend dependencies
3. Configure environment variables (if needed for AI)
4. Run the FastAPI backend
5. Start the React frontend
6. Upload a CSV file and explore the analysis

(Exact commands depend on your local setup and are intentionally kept flexible.)

---

## Final Note

This project reflects how I think about data problems in practice — **clean data first, insights later**.
It combines data analysis, automation, and GenAI in a way that mirrors real-world analytics workflows rather than isolated scripts.


Just tell me 👍
