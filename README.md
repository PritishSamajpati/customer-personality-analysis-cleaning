# Customer Personality Analysis — Excel Data Cleaning

This repository documents the process of **data cleaning** for the *Customer Personality Analysis* dataset using **Microsoft Excel only**. The cleaned data prepares the dataset for future analysis such as customer segmentation, clustering, or business intelligence reporting.

---

## 📄 Overview

The original dataset contains marketing and demographic information for over 2,200 customers. However, raw data is rarely ready for analysis, and this project focuses on **cleaning** it manually using Excel.

---

## 🧽 Data Cleaning Steps (in Excel)

### 1️⃣ Handle Missing Values
- Used **Filter** to identify missing entries.
- Found 24 missing values in the `Income` column.
- Filled missing `Income` values using the **median**.

### 2️⃣ Remove Duplicate Rows
- Selected full dataset → **Data** tab → **Remove Duplicates** to eliminate any repeated entries.

### 3️⃣ Standardize Text Values
- Cleaned text columns like `Education` and `Marital_Status`:
  - Converted to **lowercase**
  - Removed leading/trailing spaces using Excel formulas like `=LOWER(TRIM(A2))`.

### 4️⃣ Convert Date Format
- Standardized `Dt_Customer` column to **dd-mm-yyyy** using:
  - Format Cells → Date → Custom Format
  - Verified consistency throughout

### 5️⃣ Rename Columns
- Renamed headers to:
  - Be in **lowercase**
  - Replace spaces with **underscores** (e.g., `Year_Birth` → `year_birth`)

### 6️⃣ Fix Data Types
- Ensured numerical columns (e.g., `Income`, `Kidhome`, `Teenhome`) are set to **Number** format.
- Calculated new **`Age`** column using:
  ```excel
  =YEAR(TODAY()) - B2  // Assuming Year_Birth is in column B
  ```

---

## ✅ Summary of Cleaning Actions

| Step | Action                 | Description |
|------|------------------------|-------------|
| 1️⃣   | Handled Missing Values | Filled 24 missing values in `Income` using median. |
| 2️⃣   | Removed Duplicates     | Checked and removed duplicate rows. |
| 3️⃣   | Standardized Text      | Cleaned `education` and `marital_status` values. |
| 4️⃣   | Formatted Dates        | Standardized `Dt_Customer` to dd-mm-yyyy. |
| 5️⃣   | Renamed Columns        | Converted all column headers to lowercase with underscores. |
| 6️⃣   | Fixed Data Types       | Ensured numeric/date columns were correctly formatted. Added `age` column. |

---

## ⚠️ Common Problems Solved
- Mixed or missing text formatting in categorical columns.
- Inconsistent date formats breaking sorting/filtering.
- Ambiguous or duplicate entries.
- Numeric columns stored as text.
- Missing values affecting calculations.

---

## 📊 Conclusion

By performing all cleaning in Excel:
- The dataset is now **clean, consistent, and analysis-ready**
- It is suitable for loading into Power BI, Tableau, Python, or R for deeper insights
- Ideal for performing EDA, customer segmentation, and targeting strategies


**Prepared by:** Pritish Samajpati  
**Date:** April 2025
