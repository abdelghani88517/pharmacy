# 💊 Pharmaceutical Sales Data Analysis & Power BI Dashboard

## 📌 Project Overview

This project focuses on analyzing **pharmaceutical sales data** to identify business insights related to revenue, costs, profit margins, products, brands, pharmacies, and geographical performance.

The project combines **Python Exploratory Data Analysis (EDA)** with an interactive **Power BI dashboard** to transform raw pharmaceutical sales data into meaningful business insights.

The main objective is to understand sales performance, identify high-performing products and brands, analyze profitability, and provide actionable insights through data visualization.

---

## 🎯 Business Objectives

The analysis aims to answer questions such as:

* What is the overall sales performance?
* Which countries generate the highest revenue?
* Which product categories perform best?
* Which brands generate the highest profit margin?
* How are revenues and costs distributed?
* Is there a significant difference in revenue between countries?
* Is there a statistical relationship between revenue and cost?
* Which pharmacies and products contribute most to business performance?

---

## 🗂️ Project Structure

```text
pharmaceutical-sales-analysis/
│
├── 📁 data/
│   ├── FactSales.xlsx
│   ├── DimPharmacy.xlsx
│   ├── DimProduct.xlsx
│   └── DimDate.xlsx
│
├── 📓 data_analysis.ipynb
│
├── 📊 pharmaceutical-sales-dashboard.pbix
│
├── 📄 README.md
│
└── 📄 requirements.txt
```

---

## 🧩 Dataset Architecture

The project uses a dimensional data model composed of a central fact table and several dimension tables.

### Fact Table

**FactSales**

Contains transactional sales information:

| Column       | Description              |
| ------------ | ------------------------ |
| `SalesID`    | Unique sales identifier  |
| `DateKey`    | Date identifier          |
| `PharmacyID` | Pharmacy identifier      |
| `ProductID`  | Product identifier       |
| `UnitsSold`  | Number of units sold     |
| `RevenueEUR` | Revenue generated in EUR |
| `CostEUR`    | Cost in EUR              |
| `MarginEUR`  | Profit margin in EUR     |
| `PromoFlag`  | Promotion indicator      |

### Dimension Tables

**DimProduct**

Contains product-related information such as:

* Product Name
* Category
* Brand
* List Price

**DimPharmacy**

Contains pharmacy-related information such as:

* Pharmacy Name
* Country
* Region
* City
* Pharmacy Type

**DimDate**

Contains date-related information used for temporal analysis.

---

# 🐍 Python Data Analysis

The exploratory analysis was performed using Python.

## 🛠️ Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* SciPy
* Jupyter Notebook
* Power BI

---

## 🔄 Data Preparation

The four Excel datasets were imported into Pandas DataFrames.

The tables were then merged using their corresponding keys:

```text
FactSales
    │
    ├── ProductID ──> DimProduct
    │
    ├── PharmacyID ──> DimPharmacy
    │
    └── DateKey ──> DimDate
```

This produced a consolidated dataset used for the exploratory analysis.

---

# 🔎 Exploratory Data Analysis

The EDA process includes:

### 1. Dataset Exploration

* Displaying the first records
* Checking dataset dimensions
* Inspecting column names
* Checking data types
* Generating descriptive statistics

### 2. Data Quality Analysis

* Missing values detection
* Duplicate records detection
* Data structure validation

### 3. Univariate Analysis

Categorical variables analyzed include:

* Pharmacy Type
* Brand
* Country

Numerical variables analyzed include:

* Revenue
* Cost
* Margin

### 4. Multivariate Analysis

The project analyzes relationships between:

* Revenue and Product Category
* Margin and Brand
* Revenue and Country
* Cost and Product Category
* Margin and Country
* Revenue and Cost

---

# 📊 Visualizations

Several visualizations were created using Matplotlib and Seaborn.

Examples include:

* Pharmacy Type Distribution
* Top 10 Brands
* Records by Country
* Revenue Distribution
* Cost Distribution
* Margin Distribution
* Average Revenue by Category
* Top 10 Brands by Total Margin
* Revenue by Country
* Cost Distribution by Category
* Margin Distribution by Country
* Revenue vs Cost
* Correlation Matrix

---

# 📐 Statistical Analysis

To go beyond simple visualization, statistical tests were performed.

## ANOVA Test

A one-way ANOVA test was used to investigate whether revenue differs significantly between countries.

### Hypotheses

**H₀:** The mean revenue is the same across countries.

**H₁:** At least one country's mean revenue differs significantly.

A significance level of:

```text
α = 0.05
```

was used.

---

## Pearson Correlation

Pearson correlation was used to analyze the statistical relationship between:

```text
RevenueEUR
      ↕
CostEUR
```

The test evaluates whether revenue and cost are significantly correlated.

### Hypotheses

**H₀:** There is no significant correlation between revenue and cost.

**H₁:** There is a significant correlation between revenue and cost.

---

# 📊 Power BI Dashboard

The cleaned and analyzed data was also used to create an interactive Power BI dashboard.

The dashboard provides a business-oriented view of:

* Sales performance
* Revenue
* Costs
* Profit Margin
* Units Sold
* Products
* Brands
* Pharmacies
* Countries
* Categories
* Time-based performance

### Interactive Filters

Users can interact with the dashboard using filters such as:

* Pharmacy
* Pharmacy Type
* Country
* Category
* Product
* Date

---

# 💡 Key Business Insights

The analysis is designed to help decision-makers:

### 📈 Sales Performance

Identify the markets and periods generating the highest revenue.

### 💰 Profitability

Compare revenue, costs, and margins to understand business profitability.

### 💊 Product Performance

Identify the most profitable product categories and brands.

### 🌍 Geographic Performance

Compare pharmaceutical sales performance across countries.

### 🏪 Pharmacy Performance

Analyze differences between pharmacy types and individual pharmacies.

### 📊 Data-Driven Decision Making

Use statistical analysis and interactive dashboards to support business decisions.

---

# 🚀 Skills Demonstrated

This project demonstrates practical skills in:

```text
Python
├── Pandas
├── NumPy
├── Matplotlib
├── Seaborn
└── SciPy

Data Analysis
├── Data Cleaning
├── EDA
├── Data Visualization
├── Statistical Analysis
├── Correlation Analysis
└── ANOVA

Business Intelligence
├── Power BI
├── KPI Analysis
├── Interactive Dashboards
└── Business Reporting
```

---

# 📁 Project Files

| File                                  | Description                       |
| ------------------------------------- | --------------------------------- |
| `data_analysis.ipynb`                 | Python exploratory data analysis  |
| `FactSales.xlsx`                      | Pharmaceutical sales transactions |
| `DimPharmacy.xlsx`                    | Pharmacy dimension                |
| `DimProduct.xlsx`                     | Product dimension                 |
| `DimDate.xlsx`                        | Date dimension                    |
| `pharmaceutical-sales-dashboard.pbix` | Power BI interactive dashboard    |

---

# ⚙️ Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/pharmaceutical-sales-analysis.git
cd pharmaceutical-sales-analysis
```

Install the required Python libraries:

```bash
pip install pandas numpy matplotlib seaborn scipy openpyxl jupyter
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Then open:

```text
data_analysis.ipynb
```

---

# 📌 How to Use

### Step 1 — Explore the Python Analysis

Open the Jupyter Notebook and run the cells to reproduce the EDA.

### Step 2 — Explore the Power BI Dashboard

Open the `.pbix` file using Power BI Desktop.

### Step 3 — Interact With the Dashboard

Use the available filters to analyze:

* Countries
* Pharmacies
* Products
* Categories
* Brands
* Dates

---

# 📷 Dashboard Preview

> Add screenshots of your Power BI dashboard here.

```markdown
![Power BI Dashboard](images/dashboard.png)
```

---

# 📈 Project Workflow

```text
Raw Excel Data
       ↓
Data Import
       ↓
Data Integration
       ↓
Data Quality Checks
       ↓
Exploratory Data Analysis
       ↓
Statistical Analysis
       ↓
Data Visualization
       ↓
Power BI Dashboard
       ↓
Business Insights
```

---

# 🎓 Project Purpose

This project was developed as a practical **Data Analytics & Business Intelligence portfolio project**, demonstrating the complete analytical workflow from raw data integration to business visualization.

It combines technical data analysis with business-oriented reporting to support data-driven decision making.

---

# 👤 Author

**Abdelghani Dahani**

Data Analyst | Python | SQL | Power BI

📍 Morocco

---

## ⭐ If you find this project useful

Feel free to ⭐ the repository and explore the analysis.

---

## 🔮 Future Improvements

Potential future improvements include:

* Automating the data pipeline
* Adding SQL data storage
* Creating an ETL pipeline
* Adding more advanced statistical analysis
* Building predictive sales models
* Adding sales forecasting
* Deploying the dashboard for real-time monitoring
* Adding automated data refresh

---

**#Python #DataAnalysis #PowerBI #EDA #Pandas #DataVisualization #BusinessIntelligence #DataAnalytics #PharmaceuticalSales**
