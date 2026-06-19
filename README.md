#  Cafe Sales Performance & Data Cleaning Analysis (2023)

##  Project Overview
This repository contains an end-to-end data analytics project using a 2023 cafe sales dataset. The project demonstrates the entire data lifecycle: moving from a highly chaotic, error-ridden raw dataset (`dirty_cafe_sales.csv`) containing **10,000 rows**, to a fully optimized, cleaned, and modeled spreadsheet (`Cafe Sales Performance Analysis (2023).xlsx`) supporting automated business insights.

---

##  Data Analytics Workflow & Business Questions

### 1. The Ask (Business Objectives)
The analysis was driven by four critical business questions aimed at optimizing cafe operations and revenue:
1. **What is the top-selling product** by volume to optimize inventory?
2. **What is the least-selling product** to evaluate menu changes?
3. **What is the total revenue (Total Spent)** generated across all branches in 2023?
4. **Which location** drives the highest sales performance?

---

##  Deep-Dive Data Cleaning & Processing (The Core Effort)
Data integrity was the highest priority. The raw file (`dirty_cafe_sales.csv`) suffered from massive formatting issues, structural anomalies, and missing elements. The following data cleaning steps were executed directly to ensure professional-grade analysis:

* **Handling Null & Missing Values:** 
  * Identified and handled missing structural metrics: **138 rows** missing `Quantity`, **179 rows** missing `Price Per Unit`, and **173 rows** missing `Total Spent`.
  * Resolved **159 rows** with missing or corrupted `Transaction Dates` to secure chronological accuracy.
* **Filtering Irrepairable Records:** Safely removed **71 completely corrupted rows** that lacked essential primary key fields, reducing the dataset to a clean **9,929 rows**.
* **Resolving Product Name Errors (`ERROR` & `UNKNOWN`):**
  * The raw dataset contained severe text errors in the `Item` column: **292 rows** explicitly labeled as `ERROR`, **344 rows** labeled as `UNKNOWN`, and **333 blank fields**.
  * **The Solution:** Rather than deleting these records and losing valuable revenue data, a thorough cross-examination of item unit prices was conducted. These anomalies were carefully resolved, cleaned, and aggregated into a structured category named **`Other`**, preserving the financial integrity of the dashboard.
* **Financial Standardizing:** Formatted all financial representations (`Price Per Unit`, `Total Spent`) into a standardized Currency format (`$ USD`) to establish seamless numeric compatibility for subsequent equations.

---

##  Business Insights & Findings

Using advanced **Pivot Tables** and structured filtering, the aggregated data revealed the definitive financial performance of 2023:

* ** Total Revenue Generated (Grand Total):** **`$88,067.50`** 
* ** Top-Performing Product:** **Salad** emerged as the absolute best-seller with **3,892 units** sold, yielding a high financial return of **$17,035.50**. *Coffee* followed closely in second place with **3,868 units** sold ($8,937.00).
* ** Lowest-Performing Product:** **Smoothie** was identified as the lowest core performing item on the menu, generating **3,292 units** sold.

###  Interactive Dashboard & Visualization
The analysis includes a customized Horizontal Bar Chart showcasing the volume sales and revenue velocity to grasp the cafe's financial landscape in seconds:

![Sales Performance Chart](Sales%20Performance%20&%20Total%20Revenue%20per%20Item%20(2023).png)

---

##  Repository Structure
* `dirty_cafe_sales.csv`: The initial raw, unformatted dataset containing 10,000 entries with text bugs and missing data.
* `Cafe Sales Performance Analysis (2023).xlsx`: The finalized, multi-tab executive workbook structured as follows:
  * `Raw_Data`: A backup of the untouched dataset.
  * `Clean_Data`: The finalized, 9,929 fully cleaned transactions.
  * `Pivot Table 1`: The functional analytical workspace housing the final metrics, currency formatting, and the visualization chart.

---

##  How to Review This Project
1. Download or clone this repository.
2. Open `Cafe Sales Performance Analysis (2023).xlsx` in Microsoft Excel or upload it to Google Sheets.
3. Switch to the `Pivot Table 1` tab to explore the automated metrics and interact with the finalized revenue charts.
