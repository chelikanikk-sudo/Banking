# Banking Dashboard
### Dashboard Link : https://drive.google.com/file/d/1aQ0gwHqkZyBeHbLH8vHEkIUNXManGdW1/view?usp=sharing
## Dashboard Overview

This Banking Dashboard was developed using Power BI to analyze customer transactions, account balances, customer demographics, and account activity. The dashboard enables banking institutions to monitor business performance, identify customer behavior patterns, and make data-driven decisions.

The report consists of two interactive pages:

- Banking Performance Dashboard
- Customer Analytics Dashboard

---

## Problem Statement

Banks generate large volumes of customer and transaction data daily. Analyzing this data manually is time-consuming and inefficient.

This dashboard helps banking professionals:

- Monitor transaction activity across different transaction types.
- Analyze monthly transaction and balance trends.
- Identify high-value customers.
- Understand customer demographics.
- Track inactive accounts.
- Evaluate account type distribution.

By leveraging these insights, banks can improve customer engagement, optimize operations, and support strategic decision-making.

---

## Tools & Technologies Used

- SQL
- Power BI Desktop
- Power Query Editor
- DAX (Data Analysis Expressions)
- Data Modeling
- Interactive Visualizations

---

## Steps Followed

### Step 1: Data Loading

Used SQL to join multiple tables and imported the banking dataset into Power BI Desktop for data analysis and visualization.

### Step 2: Data Cleaning

Opened Power Query Editor and performed:

- Data validation
- Data type corrections
- Missing value checks
- Data quality verification

### Step 3: Data Profiling

Enabled:

- Column Quality
- Column Distribution
- Column Profile

to understand dataset characteristics.

### Step 4: Data Modeling

Created relationships and optimized the data model for reporting.

### Step 5: DAX Calculations

Created measures and calculated columns for:

- Transaction analysis
- Customer analysis
- Balance monitoring
- Inactive account tracking

### Step 6: Dashboard Design

Created multiple interactive visualizations for:

- Transaction trends
- Customer demographics
- Balance analysis
- Account analysis

### Step 7: Formatting

Applied report themes, formatting, and interactive filtering.


---

# Dashboard Visuals

## Page 1: Banking Performance Dashboard

### Transaction Type Distribution

**Visual:** Pie Chart

Shows the distribution of various transaction types.

### Monthly Transaction Amount Trend

**Visual:** Area Chart

Displays monthly transaction amount trends.

### Customer-wise Transaction Amount

**Visual:** Bar Chart

Highlights customers with the highest transaction volumes.

### Total Balance by Account Type

**Visual:** Clustered Column Chart

Compares balances across account categories.

### Monthly Balance Trend

**Visual:** Line Chart

Tracks balance changes over time.

---

## Page 2: Customer Analytics Dashboard

### Inactive Accounts Trend

**Visual:** Line Chart

Monitors inactive account growth over time.

### Gender Distribution

**Visual:** Donut Chart

Displays customer distribution by gender.

### Customer Age Group Analysis

**Visual:** Column Chart

Shows customer segmentation by age groups.

### Account Type Distribution

**Visual:** Treemap

Represents account type popularity.

---

# DAX Measures

## Transaction Count

```DAX
Transaction Count =
COUNTROWS(CombinedBankingDataset)
```

## Total Transaction Amount

```DAX
Total Transaction Amount =
SUM(CombinedBankingDataset[Amount])
```

## Total Balance

```DAX
Total Balance =
SUM(CombinedBankingDataset[Balance])
```

## Customer Count

```DAX
Customer Count =
DISTINCTCOUNT(CombinedBankingDataset[CustomerID])
```

## Inactive Accounts

```DAX
Inactive Accounts =
CALCULATE(
    DISTINCTCOUNT(CombinedBankingDataset[CustomerID]),
    CombinedBankingDataset[AccountStatus] = "Inactive"
)
```

## Customer Age Group

```DAX
Customer Age Group =
IF(
    CombinedBankingDataset[Age] <= 25,
    "18-25",
    IF(
        CombinedBankingDataset[Age] <= 40,
        "26-40",
        IF(
            CombinedBankingDataset[Age] <= 60,
            "41-60",
            "60+"
        )
    )
)
```

---

# Report Snapshots

## Banking Performance Dashboard

<img width="1275" height="724" alt="Image" src="https://github.com/user-attachments/assets/6776bfb3-0570-4a8e-b5fc-9f0303ec30a4" />
---

## Customer Analytics Dashboard

<img width="1128" height="729" alt="Image" src="https://github.com/user-attachments/assets/923dba7d-291c-4de1-a923-105d0c7e977b" />
---

# Key Insights

## Transaction Analysis

- Identifies the most commonly used transaction types.
- Tracks transaction growth and seasonal patterns.
- Highlights high-value customers.

## Balance Analysis

- Monitors balance trends over time.
- Compares balances across account types.

## Customer Analysis

- Provides demographic insights.
- Analyzes customer age distribution.
- Supports customer segmentation strategies.

## Account Analysis

- Tracks inactive accounts.
- Evaluates account type popularity.
- Supports customer retention initiatives.

---

# Business Benefits

- Improved decision-making through data-driven insights.
- Better understanding of customer behavior.
- Enhanced monitoring of banking operations.
- Identification of customer retention opportunities.
- Improved performance tracking.

---

# Future Enhancements

- Loan analysis dashboard
- Credit card performance tracking
- Branch-wise performance monitoring
- Customer churn prediction
- AI-powered customer segmentation

---

# Author

**Kamal Kishore**

Data Analyst

### Skills

- SQL
- Python
- Power BI
- Excel
- Tableau

---

## Project Files

- Banking.pbix
- README.md
- Dashboard Screenshots
