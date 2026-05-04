# Automated Data Cleaning Pipeline (Retail Sales)

## 📌 Project Overview
In the real world, 80% of data work is cleaning. This project demonstrates a professional approach to transforming "dirty" raw data into a "business-ready" format. I used Python (Pandas) to build a repeatable script that fixes common data entry errors, saving hours of manual Excel work.

## 🛠️ Tech Stack
- **Language:** Python 3.x
- **Library:** Pandas (Data Manipulation)
- **Environment:** Jupyter Notebook / VS Code

## 📉 The Problem (Before Cleaning)
The raw dataset (`dirty_sales_data.csv`) contained several issues that would break any analysis:
- **Inconsistent Dates:** Mixed formats (e.g., `2026-01-15` and `16/01/2026`).
- **Duplicates:** Identical transaction IDs appearing multiple times.
- **Data Integrity:** Negative values in the `Amount` column.
- **Naming Issues:** Inconsistent casing (e.g., `sara tadesse` vs `Sara Tadesse`).

## 🧪 The Solution (Cleaning Steps)
1. **Deduplication:** Identified and removed duplicate rows based on `Transaction_ID`.
2. **Standardization:** Converted all date strings into a uniform `YYYY-MM-DD` datetime object.
3. **Validation:** Created a logic check to convert negative sales amounts to absolute values.
4. **Formatting:** Applied title-casing to all string columns for professional reporting.

## 🚀 How to Use
1. Clone this repo: `git clone https://github.com/your-username/repo-name.git`
2. Install dependencies: `pip install pandas`
3. Run the script: `python clean_data.py`

## 📊 Results
- **Initial Row Count:** 500
- **Cleaned Row Count:** 482
- **Data Accuracy:** Increased from 72% to 100% based on format validation.
