# Vendor Performance Analysis

## 📊 Project Overview

This project focuses on analyzing vendor performance using sales, purchasing, inventory, pricing, and freight data.

The project follows an end-to-end data analytics workflow:

**Raw Data → Data Ingestion → SQLite Database → Data Cleaning & Transformation → Vendor Analysis → Business Insights → Power BI Dashboard**

The objective is to identify vendor performance patterns, profitability, sales performance, inventory efficiency, and purchasing opportunities that can support better business decisions.

---

## 🎯 Objectives

- Analyze vendor sales and purchasing performance
- Identify high-performing and low-performing vendors
- Evaluate vendor profitability
- Analyze purchase and sales quantities
- Calculate profit margins
- Measure stock turnover
- Compare sales against purchasing costs
- Analyze freight costs
- Identify opportunities for improving vendor and inventory performance
- Present business insights through an interactive Power BI dashboard

---

## 🗂️ Project Structure

```text
Vendor-Performance-Analysis/
│
├── DATA/
│   ├── begin_inventory.csv
│   ├── end_inventory.csv
│   ├── purchase_prices.csv
│   ├── purchases.csv
│   ├── sales.csv
│   └── vendor_invoice.csv
│
├── DATABASE/
│   └── inventory.db
│
├── IMAGES/
│   ├── Executive Overview.png
│   └── Vendor Performance.png
│
├── NOTEBOOK/
│   ├── Exploratory Data Analysis.ipynb
│   └── Vendor_Performance_Analysis.ipynb
│
├── OUTPUT/
│   ├── Brand_performance.csv
│   ├── vendor_performance.csv
│   ├── Vendor_sales_summary.csv
│   └── Vendor_sales_summary_cleaned.csv
│
├── POWER BI/
│   └── Vendors_Performance_Analysis.pbix
│
├── SCRIPTS/
│   ├── ingestion_db.py
│   └── get_Vendor_summary.py
│
├── LICENSE
└── README.md
---

---

## 🛠️ Tools & Technologies

* **Python**
* **Pandas**
* **SQL**
* **SQLite**
* **Jupyter Notebook**
* **Power BI**
* **Git & GitHub**

---

## 📁 Dataset

The project uses multiple source datasets covering:

* Beginning inventory
* Ending inventory
* Purchase prices
* Purchases
* Sales
* Vendor invoices

These datasets are used as the raw input for the analysis and database pipeline.

> **Note:** The original `purchases` and `sales` files are very large, so they may not be included directly in this GitHub repository due to GitHub's individual file-size limitations.

---

## 🔄 Data Pipeline

### 1. Data Ingestion

The raw CSV files are read using Python and loaded into an SQLite database.

The ingestion process automatically reads CSV files from the `DATA` directory and creates corresponding database tables.

### 2. Data Preparation

The project performs data cleaning and transformation, including:

* Data type conversion
* Missing-value handling
* Removing unnecessary spaces from text fields
* Creating calculated business metrics

### 3. Vendor Summary

Purchase, sales, and freight information are combined to create a comprehensive vendor-level summary.

The analysis includes:

* Total Purchase Quantity
* Total Purchase Dollars
* Total Sales Quantity
* Total Sales Dollars
* Total Sales Price
* Total Excise Tax
* Freight Cost

### 4. Performance Metrics

The project calculates several important performance indicators:

**Gross Profit**

```text
Gross Profit = Total Sales Dollars - Total Purchase Dollars
```

**Profit Margin**

```text
Profit Margin = (Gross Profit / Total Sales Dollars) × 100
```

**Stock Turnover**

```text
Stock Turnover = Total Sales Quantity / Total Purchase Quantity
```

**Sales-to-Purchase Ratio**

```text
Sales-to-Purchase Ratio =
Total Sales Dollars / Total Purchase Dollars
```

---

## 📈 Exploratory Data Analysis

Exploratory Data Analysis is performed to understand:

* Vendor performance
* Brand performance
* Sales trends
* Purchasing behavior
* Profitability
* Inventory efficiency
* Vendor contribution to overall business performance

The analysis notebooks are available in the `NOTEBOOK` directory.

---

## 📊 Power BI Dashboard

The final analysis is presented through an interactive Power BI dashboard.

The dashboard is designed to provide a business-friendly view of:

* Vendor performance
* Sales performance
* Purchase performance
* Profitability
* Inventory-related metrics
* Vendor comparisons
* Key business insights

The Power BI file is available in the `POWER BI` directory.

---

## 💡 Key Business Questions

This project helps answer questions such as:

1. Which vendors generate the highest sales?
2. Which vendors generate the highest gross profit?
3. Which vendors have the best profit margins?
4. Which vendors have high purchasing costs but relatively low sales?
5. Which vendors have strong stock turnover?
6. Which brands contribute significantly to vendor performance?
7. How do sales compare with purchasing costs?
8. How do freight costs affect vendor profitability?
9. Which vendors may require further investigation or optimization?

---

## 🚀 How to Run the Project

### Step 1: Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/Vendor-Performance-Analysis.git
cd Vendor-Performance-Analysis
```

### Step 2: Install Required Libraries

```bash
pip install pandas sqlalchemy
```

### Step 3: Place Raw Data

Place the available raw CSV datasets inside:

```text
DATA/
```

### Step 4: Create the Database

Run:

```bash
python SCRIPTS/ingestion_db.py
```

This loads the CSV datasets into the SQLite database.

### Step 5: Generate Vendor Summary

Run:

```bash
python SCRIPTS/get_Vendor_summary.py
```

This creates the vendor summary and calculated performance metrics.

### Step 6: Explore the Analysis

Open the notebooks inside:

```text
NOTEBOOK/
```

### Step 7: View the Dashboard

Open:

```text
POWER BI/Vendors_Performance_Analysis.pbix
```

in Microsoft Power BI Desktop.

---

## 📌 Project Outputs

The project produces several analysis datasets, including:

* `Brand_performance.csv`
* `vendor_performance.csv`
* `Vendor_sales_summary.csv`
* `Vendor_sales_summary_cleaned.csv`

These files contain processed information used for further analysis and visualization.

---

## 📷 Dashboard Preview

Dashboard screenshots and other project visuals can be placed inside:

![Executive Overview](https://github.com/Shrey2503/Vendor-Performance-Analysis/blob/main/IMAGES/Executive%20Overview.png)

![Vendor Performance](https://github.com/Shrey2503/Vendor-Performance-Analysis/blob/main/IMAGES/Vendor%20Performance.png)
```

---

## 🔮 Future Improvements

Possible improvements include:

* Automating the complete data pipeline
* Adding scheduled data refresh
* Improving dashboard interactivity
* Adding more vendor-level KPIs
* Adding predictive sales analysis
* Developing vendor segmentation
* Adding automated anomaly detection
* Connecting Power BI directly to the database

---

## 👨‍💻 Author

**Shreyash Vats**

Data Analytics Project

---

## 📄 License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.
