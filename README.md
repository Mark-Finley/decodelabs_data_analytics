# DecodeLabs Data Analytics Projects

A practical data analytics portfolio project completed as part of the **DecodeLabs Data Analytics Internship Program**. The project demonstrates an end-to-end analytical workflow, from raw data cleaning and preparation through exploratory analysis and SQL-based business analysis.

---

## 📌 Project Overview

This repository contains the analysis performed on a **sales dataset** as part of the first three DecodeLabs Data Analytics projects.

The analysis follows a structured progression:

1. **Project 1 — Data Cleaning & Preparation**
2. **Project 2 — Exploratory Data Analysis (EDA)**
3. **Project 3 — SQL Data Analysis**

The overall objective was to transform raw sales data into a reliable, structured, and business-ready dataset capable of supporting meaningful insights and decision-making.

The project emphasizes not only technical execution but also the ability to explain **what the data says, why the finding matters, and how it can support business decisions**.

---

## 🎯 Project Objectives

The main objectives of this project were to:

- Clean and prepare raw sales data for analysis.
- Identify and handle missing values.
- Detect and remove duplicate records.
- Validate unique identifiers.
- Standardize dates, text, and numerical values.
- Explore the structure and characteristics of the dataset.
- Calculate descriptive statistics.
- Identify patterns, trends, and relationships within the data.
- Detect and investigate potential outliers.
- Apply SQL to answer business-oriented questions.
- Practice writing efficient and logically structured SQL queries.
- Translate analytical results into actionable business insights.

---

# 📂 Repository Structure

```text
decodelabs-data-analytics/
│
├── .venv/
│   └── Python virtual environment
│
├── dataset/
│   └── Dataset.xlsx
│
├── notebooks/
│   ├── 00_Data_Cleaning.ipynb
│   ├── 01_Data_Exploration.ipynb
│   └── 02_Exploratory_Data_Analysis.ipynb
│
├── sql-analysis/
│   └── sql_fundamentals.sql
│
├── .gitignore
├── README.md
└── requirements.txt
```

### Directory Description

| Directory/File | Purpose |
|---|---|
| `dataset/` | Contains the source sales dataset |
| `notebooks/00_Data_Cleaning.ipynb` | Data cleaning and preparation workflow |
| `notebooks/01_Data_Exploration.ipynb` | Initial exploration and understanding of the dataset |
| `notebooks/02_Exploratory_Data_Analysis.ipynb` | Statistical analysis, patterns, relationships, and visualizations |
| `sql-analysis/sql_fundamentals.sql` | SQL queries used for structured sales data analysis |
| `requirements.txt` | Python dependencies required to reproduce the analysis |
| `.gitignore` | Files and directories excluded from version control |
| `.venv/` | Local Python virtual environment |

---

# 🧹 Project 1 — Data Cleaning & Preparation

The first stage focused on transforming the raw sales dataset into a reliable analytical dataset.

## Objectives

The cleaning process focused on:

- Understanding the dataset structure.
- Inspecting column names and data types.
- Identifying missing values.
- Handling missing values using appropriate statistical techniques(in our case replacing nulls in coupon code column with No Coupon).
- Detecting duplicate records.
- Validating unique identifiers.
- Standardizing text values.
- Standardizing numerical precision.
- Converting dates into a consistent format.
- Preparing the dataset for downstream analysis.

## Data Quality Principles

Rather than simply deleting incomplete records, missing values were assessed based on their context and potential impact on the analysis.

Appropriate approaches included:

- **Mean imputation** for suitable approximately symmetrical numerical variables.
- **Median imputation** for skewed numerical variables.
- **Mode or logical replacement** for appropriate categorical variables.
- **Record removal** only where the record could not be reliably recovered or retained.

Duplicate records were also investigated to prevent double-counting and inaccurate aggregations.

### Verification

The cleaned dataset was evaluated against key integrity requirements:

- Unique identifiers should contain no errors.
- Dates should follow a consistent format.
- Numerical values should use consistent precision.
- Categorical/text values should follow standardized conventions.

The resulting dataset provides a cleaner foundation for exploratory analysis and SQL querying.

---

# 🔎 Project 2 — Exploratory Data Analysis

The second stage focused on understanding the sales dataset and discovering patterns, trends, distributions, and relationships.

EDA was approached as a **discovery process**, rather than simply producing charts.

The analytical framework followed:

> **Input → Process → Output**

Where:

- **Input** = Evidence contained in the dataset.
- **Process** = Statistical or mathematical analysis applied to the evidence.
- **Output** = A business-oriented interpretation or verdict.

---

## Exploratory Analysis

The dataset was initially explored to understand:

- Number of records and variables.
- Data types.
- Numerical and categorical variables.
- Distribution of important measures.
- Central tendencies.
- Potential data quality issues.
- Relationships between variables.

Descriptive statistics such as:

- Mean
- Median
- Minimum
- Maximum
- Count
- Standard deviation

were used where appropriate.

---

## Outlier Analysis

Potential outliers were investigated rather than automatically removed.

This distinction is important because an extreme value may represent:

- A data-entry error.
- An unusual transaction.
- A legitimate high-value sale.
- An exceptional business event.

Statistical techniques such as the **Interquartile Range (IQR)** and **Z-score** methods can be used to identify potential outliers.

The objective was therefore not simply to eliminate unusual observations, but to determine whether they represented **noise or meaningful business signals**.

---

## Relationship Analysis

Relationships between numerical variables were investigated using statistical techniques such as the **Pearson correlation coefficient**.

Correlation analysis helps determine whether two numerical variables have a positive, negative, or weak linear relationship.

Importantly, correlation was interpreted as an indication of association rather than proof of causation.

---

## Data Visualization

Visualizations were used to communicate findings clearly.

The analysis followed several visualization principles:

- Avoid unnecessary 3D effects.
- Minimize visual clutter.
- Use appropriate chart types.
- Maintain readable labels.
- Highlight important patterns.
- Use meaningful titles.
- Focus charts on business questions rather than decoration.

Where appropriate, chart titles and accompanying explanations were designed to communicate the insight rather than merely describe the chart.

---

# 🗄️ Project 3 — SQL Data Analysis

The third stage focused on using SQL to analyze the sales data and answer business-oriented questions.

The SQL analysis was designed to strengthen understanding of the **declarative nature of SQL**.

Instead of describing every step required to retrieve information, SQL queries specify the desired result while the database engine determines how to execute the query.

---

## SQL Concepts Applied

The analysis covered fundamental SQL concepts including:

### SELECT

Used to select required columns and create calculated fields or aliases.

### WHERE

Used to filter individual records before aggregation.

### GROUP BY

Used to organize records into categories for aggregated analysis.

### Aggregate Functions

Functions such as:

```sql
COUNT()
SUM()
AVG()
```

were used to calculate business metrics.

### HAVING

Used to filter aggregated groups after `GROUP BY`.

### ORDER BY

Used to organize the final result set.

---

# ⚙️ SQL Logical Execution Order

A major concept explored during the SQL analysis was the difference between the order SQL is **written** and the order it is **logically processed**.

The logical execution order is:

```text
1. FROM / JOIN
2. WHERE
3. GROUP BY
4. HAVING
5. SELECT
6. ORDER BY
```

Understanding this order helps explain common SQL errors, such as attempting to reference a `SELECT` alias inside a `WHERE` clause before that alias logically exists.

---

# 📊 Business Analysis Approach

The analysis was designed around the principle that a data analyst should not simply produce numbers.

The analytical process should answer:

### What happened?

Identify measurable patterns and trends in the sales data.

### Why does it matter?

Interpret the statistical or SQL result in a business context.

### What could the business do?

Translate the finding into a potential decision, recommendation, or area for further investigation.

This approach helps transform technical analysis into actionable business intelligence.

---

# 🛠️ Tools & Technologies

The project uses the following technologies:

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Jupyter Notebook**
- **SQL**
- **Excel**
- **Git & GitHub**
- **WSL / Ubuntu**

Python was used for data cleaning, exploration, statistical analysis, and visualization, while SQL was used to demonstrate structured querying and business analysis.

---

# 📦 Python Environment

Python dependencies are documented in:

```text
requirements.txt
```

To create the virtual environment:

```bash
python3 -m venv .venv
```

Activate it on Ubuntu/WSL:

```bash
source .venv/bin/activate
```

Install the required packages:

```bash
pip install -r requirements.txt
```

---



# 📈 Analytical Workflow

The complete workflow can be summarized as:

```text
Raw Sales Dataset
       │
       ▼
Data Inspection
       │
       ▼
Data Cleaning & Preparation
       │
       ├── Missing Values
       ├── Duplicates
       ├── Data Types
       ├── Dates
       ├── Text Standardization
       └── Identifier Validation
       │
       ▼
Clean Dataset
       │
       ▼
Exploratory Analysis
       │
       ├── Descriptive Statistics
       ├── Distributions
       ├── Outliers
       ├── Correlations
       └── Visualizations
       │
       ▼
Business Insights
       │
       ▼
SQL Analysis
       │
       ├── Filtering
       ├── Aggregation
       ├── Grouping
       ├── Conditional Analysis
       └── Sorting
       │
       ▼
Actionable Business Intelligence
```

---

# 🎓 Key Learning Outcomes

Through these projects, the following skills were developed and demonstrated:

- Data cleaning and preparation.
- Data quality assessment.
- Missing-value treatment.
- Duplicate detection.
- Data validation.
- Data standardization.
- Exploratory data analysis.
- Descriptive statistics.
- Outlier detection.
- Correlation analysis.
- Data visualization.
- SQL querying.
- Aggregation and grouping.
- Business-oriented analytical thinking.
- Translating quantitative findings into business insights.

---

# 💡 Key Takeaway

The project demonstrates the progression from **raw data to business intelligence**.

Rather than treating data analysis as simply creating charts or writing SQL queries, the workflow emphasizes the complete analytical lifecycle:

> **Clean the data → Understand the data → Analyze the data → Interpret the findings → Support better decisions**

Projects 1–3 therefore establish the foundation for more advanced data analytics work, where the focus can move from data preparation and exploration toward deeper business intelligence, dashboarding, predictive analysis, and data-driven decision-making.

---

## 📌 Project Status

| Project | Focus | Status |
|---|---|---|
| Project 1 | Data Cleaning & Preparation | ✅ Completed |
| Project 2 | Exploratory Data Analysis | ✅ Completed |
| Project 3 | SQL Data Analysis |  In-Progress |

---

## 👤 Author

**Mark Finley**

Data Analyst | Software Engineer

This project was completed as part of the **DecodeLabs Data Analytics Internship Program**.