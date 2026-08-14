# 📊 Vendor Performance Analysis

An end-to-end **Data Analytics project** analyzing vendor sales, purchasing, profitability, inventory efficiency, and freight costs using **Python, SQL, SQLite, and Power BI**.

The project follows a complete analytics workflow:

**Raw Data → Data Ingestion → SQLite Database → Data Cleaning & Transformation → Vendor Analysis → Business Insights → Power BI Dashboard**

---

## 🎯 Project Objective

The objective of this project is to evaluate vendor performance and identify opportunities for improving **sales, profitability, purchasing efficiency, inventory management, and vendor relationships**.

### Key objectives

* Analyze vendor sales and purchasing performance
* Identify high- and low-performing vendors
* Evaluate vendor profitability and profit margins
* Analyze purchase and sales quantities
* Measure stock turnover
* Compare sales against purchasing costs
* Analyze freight costs
* Evaluate brand-level performance
* Identify potential purchasing and inventory optimization opportunities
* Present insights through an interactive Power BI dashboard

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
├── README.md
└── requirements.txt
```

---

## 🛠️ Tools & Technologies

| Category        | Tools                |
| --------------- | -------------------- |
| Programming     | Python               |
| Data Analysis   | Pandas, NumPy        |
| Database        | SQLite, SQL          |
| Visualization   | Power BI, Matplotlib |
| Development     | Jupyter Notebook     |
| Version Control | Git, GitHub          |

---

## 📁 Dataset

The project uses multiple datasets covering:

* Beginning inventory
* Ending inventory
* Purchase prices
* Purchases
* Sales
* Vendor invoices

These datasets form the raw input for the data ingestion, transformation, and analysis pipeline.

> **Note:** The original `purchases` and `sales` datasets are large and may not be included directly in the repository because of GitHub file-size limitations.

---

## 🔄 Data Analytics Pipeline

### 1. Data Ingestion

Raw CSV files are read using Python and loaded into an **SQLite database**.

The ingestion script automatically processes the available datasets from the `DATA` directory and creates the corresponding database tables.

### 2. Data Cleaning & Transformation

The project performs data preparation tasks including:

* Data type conversion
* Missing-value handling
* Text cleaning
* Data aggregation
* Joining multiple datasets
* Creating calculated business metrics

### 3. Vendor-Level Analysis

Purchase, sales, and freight information are combined to create a comprehensive vendor-level dataset.

Key metrics include:

* Total Purchase Quantity
* Total Purchase Dollars
* Total Sales Quantity
* Total Sales Dollars
* Total Sales Price
* Total Excise Tax
* Freight Cost

### 4. Performance Metrics

#### Gross Profit

```text
Gross Profit = Total Sales Dollars - Total Purchase Dollars
```

#### Profit Margin

```text
Profit Margin = (Gross Profit / Total Sales Dollars) × 100
```

#### Stock Turnover

```text
Stock Turnover = Total Sales Quantity / Total Purchase Quantity
```

#### Sales-to-Purchase Ratio

```text
Sales-to-Purchase Ratio =
Total Sales Dollars / Total Purchase Dollars
```

---

## 📈 Exploratory Data Analysis

Exploratory Data Analysis is used to investigate:

* Vendor performance
* Brand performance
* Sales performance
* Purchasing behavior
* Profitability
* Inventory efficiency
* Vendor contribution to overall business performance

The analysis notebooks are available in the `NOTEBOOK` directory.

---

## 📊 Power BI Dashboard

The final analysis is presented through an interactive **Power BI dashboard**.

The dashboard provides a business-focused view of:

* Vendor performance
* Sales performance
* Purchase performance
* Gross profit
* Profit margin
* Inventory efficiency
* Vendor comparisons
* Key performance indicators

### Dashboard Preview

#### Executive Overview

![Executive Overview](./IMAGES/Executive%20Overview.png)

#### Vendor Performance

![Vendor Performance](./IMAGES/Vendor%20Performance.png)

---

## 💡 Business Questions

This project helps answer questions such as:

1. Which vendors generate the highest sales?
2. Which vendors generate the highest gross profit?
3. Which vendors have the strongest profit margins?
4. Which vendors have high purchasing costs relative to sales?
5. Which vendors have strong stock turnover?
6. Which brands contribute significantly to vendor performance?
7. How do sales compare with purchasing costs?
8. How do freight costs affect vendor profitability?
9. Which vendors may require further investigation or optimization?

---

## 📦 Project Outputs

The analysis produces processed datasets including:

* `Brand_performance.csv`
* `vendor_performance.csv`
* `Vendor_sales_summary.csv`
* `Vendor_sales_summary_cleaned.csv`

These outputs are used for further analysis and Power BI visualization.

---

## 🚀 How to Run the Project

### 1. Clone the repository

```bash
git clone https://github.com/Shrey2503/Vendor-Performance-Analysis.git
cd Vendor-Performance-Analysis
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Add the raw datasets

Place the available CSV files inside:

```text
DATA/
```

### 4. Create the SQLite database

Run:

```bash
python SCRIPTS/ingestion_db.py
```

This loads the available CSV datasets into the SQLite database.

### 5. Generate the vendor summary

Run:

```bash
python SCRIPTS/get_Vendor_summary.py
```

This generates the vendor-level summary and calculated performance metrics.

### 6. Explore the analysis

Open the notebooks inside:

```text
NOTEBOOK/
```

### 7. Open the Power BI dashboard

Open:

```text
POWER BI/Vendors_Performance_Analysis.pbix
```

using **Microsoft Power BI Desktop**.

---

## 🔮 Future Improvements

Potential improvements include:

* Automating the complete data pipeline
* Adding scheduled data refresh
* Improving dashboard interactivity
* Adding additional vendor-level KPIs
* Developing vendor segmentation
* Adding predictive sales analysis
* Implementing automated anomaly detection
* Connecting Power BI directly to the database

---

## 👨‍💻 Author

**Shreyash Vats**

Aspiring Data Analyst
**SQL | Python | Power BI | Excel**

[GitHub](https://github.com/Shrey2503) · [LinkedIn](https://www.linkedin.com/in/shreyash-vats-1a22232a4/)

---

## 📄 License

This project is licensed under the **MIT License**. See the `LICENSE` file for details.
