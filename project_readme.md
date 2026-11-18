# E-Commerce Dataset Cleaning, Sales Analysis & Visualization Challenge

**Internship Program:** Data Science Internship — Week 1 Assignment  
**Organization:** WeIntern Pvt Ltd  
**Author:** Prajwal Vilas Khake  

---

## 📌 Project Overview & Objective
The objective of this Week 1 project is to develop disciplined data cleaning, structured exploratory analysis, visualization, and professional reporting habits. Using a raw online retail transaction dataset, this repository walks through the end-to-end analytical workflow: resolving data quality issues, calculating core business Key Performance Indicators (KPIs), uncovering seasonal and customer-level trends, and presenting actionable business recommendations.

---

## 📊 Dataset Description
The dataset (`cleaned_online_retail_data.xlsx`) contains global e-commerce transaction records spanning **December 1, 2010 to December 9, 2011** across **37 countries**.

* **Total Cleaned Records:** 392,732 valid transaction line items
* **Unique Products (`StockCode`):** 3,665 SKUs
* **Unique Customers (`CustomerID`):** 4,339 buyers
* **Key Fields:**
  * `InvoiceNo`: Unique order transaction identifier
  * `StockCode` & `Description`: Product code and item name
  * `Quantity` & `UnitPrice`: Units purchased and price per unit
  * `InvoiceDate`: Date and timestamp of the transaction
  * `CustomerID` & `Country`: Customer identifier and geographic market
  * `TotalRevenue`: Engineered field ($\text{Quantity} \times \text{UnitPrice}$)
  * `Month`, `Month_no`, `Week`: Extracted time-series grouping columns
  * `order_status`: Standardized transaction status (`non-cancelled`)

---

## 🛠️ Tools & Libraries Used
* **Programming Language:** Python 3.x
* **Data Manipulation & Analysis:** `pandas`, `numpy`
* **Data Visualization:** `matplotlib`, `seaborn`
* **Business Intelligence / Dashboarding:** Power BI / Static Executive Mockup
* **Environment:** Jupyter Notebook / Anaconda

---

## 🔄 Key Steps Performed
1. **Data Inspection & Cleaning (Task 1):**
   * Preserved the raw dataset separately and inspected column types, distributions, and missingness.
   * Resolved missing `CustomerID` and `Description` records (achieving 0 null values in the final dataset).
   * Filtered out cancelled invoices (`order_status`) and validated that all quantities and unit prices are strictly positive.
   * Converted `InvoiceDate` to standard datetime format and engineered `TotalRevenue`, `Month`, and `Week` features.
2. **Sales & Customer Analysis (Task 2):**
   * Computed core KPIs including Total Revenue, Total Orders, Average Order Value (AOV), and Total Units Sold.
   * Analyzed monthly revenue trajectories to identify seasonal growth and recurring low-season dips.
   * Segmented repeat vs. one-time buyers and evaluated regional export performance.
3. **Data Visualization & Dashboarding (Task 3):**
   * Built labeled line charts (monthly trends), horizontal/vertical bar charts (top products and international markets), and pie charts (customer revenue share).
   * Compiled visuals and KPI cards into a clean executive dashboard layout and formal analytical report.

---

## 💡 Major Findings & Business Insights
* **Core Performance:** Generated **$8,887,208.89** in total revenue across **18,536** unique orders (**5,165,886** units sold), with an Average Order Value (AOV) of **$479.46**.
* **Q4 Seasonal Surge:** Sales remain steady from January to August ($446K–$677K/month) before surging **+47.6% MoM in September ($950.7K)** and peaking in **November 2011 ($1.16M)**.
* **Repeat Customer Dominance:** **65.57%** of customers (2,845 buyers) made repeat purchases, driving **$8,273,219.33 (93.09%)** of total company revenue.
* **Geographic Distribution:** While the **United Kingdom** leads total revenue (**81.97%** / $7.29M), European markets—specifically the **Netherlands ($285.4K)**, **EIRE ($265.3K)**, **Germany ($228.7K)**, and **France ($208.9K)**—show strong high-value export demand.
* **Top SKU:** *PAPER CRAFT , LITTLE BIRDIE* is the top revenue-generating product at **$168,469.60** (80,995 units).

---

## 📁 Repository Structure
```text
data-science-week1-assignment/
├── data/
│   ├── raw/                        # Original untouched dataset
│   └── cleaned/
│       └── cleaned_online_retail_data.xlsx
├── notebooks/
│   └── week1_analysis.ipynb        # Data cleaning, KPI computation & visualization code
├── outputs/
│   ├── charts/                     # Saved individual chart exports
│   └── dashboard/
│       └── sales_analysis_visuals.png
├── reports/
│   └── week1_analytical_report.pdf # Final formatted analytical report
├── screenshots/                    # Supporting notebook & dashboard screenshots
├── README.md                       # Project documentation
└── requirements.txt                # Python package dependencies
```

---

## 🚀 Execution Instructions
1. **Clone the repository:**
   ```bash
   git clone <your-github-repo-link>
   cd data-science-week1-assignment
   ```
2. **Install required dependencies:**
   ```bash
   pip install -r requirements.txt
   ```
3. **Run the analysis notebook:**
   * Launch Jupyter Notebook or JupyterLab:
     ```bash
     jupyter notebook notebooks/week1_analysis.ipynb
     ```
   * Run all cells sequentially from top to bottom (`Kernel` $\rightarrow$ `Restart & Run All`) to reproduce the cleaned dataset, KPI tables, and charts.