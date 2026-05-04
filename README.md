# Automated Sales Data Sanitization Pipeline

## 📌 Project Overview
This project demonstrates a robust Python-based solution for cleaning and normalizing a messy retail dataset. As a Data Analyst with a CS background, I focused on building a script that ensures data integrity for accurate business reporting.

## 🛠️ The Challenge (Data Issues Identified)
The `raw_data.csv` file contained several critical issues that would lead to incorrect business insights:
- **Geographic Fragmentation:** "Addis Ababa," "addis," and "AA" were used for the same city.
- **Date Inconsistency:** Mixed formats (DD/MM/YYYY, YYYY/DD/MM, and YYYY-MM-DD).
- **Missing Values:** Null values in `quantity`, `price`, and `email` columns.
- **Casing Errors:** Inconsistent capitalization in customer names.

## 🧪 The Solution (Cleaning Logic)
I developed a Python pipeline using **Pandas** to perform the following:
1. **Date Normalization:** Forced all date entries into a standard ISO 8601 format.
2. **City Standardization:** Implemented a mapping dictionary to unify regional names (e.g., all variations of Addis Ababa were merged).
3. **Statistical Imputation:** Used the **Median** to fill missing quantities to maintain data distribution without introducing outlier bias.
4. **Data Deduplication:** Removed duplicate records based on `order_id` to prevent revenue overestimation.

## 🚀 How to Run
1. Ensure you have Python or Anaconda installed.
2. Clone this repository.
3. Run the script:
   ```bash
   python clean_data.py
