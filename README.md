# Bank Customer Churn Analysis

📌 **Project Overview**

This project analyzes customer churn data from a European bank to understand why customers leave and identify patterns that influence churn behavior. The analysis was performed using Excel, SQL, and Power BI to uncover business insights and build an interactive dashboard for decision-making.

The goal of the project is to help the bank:

- Understand customer demographics
- Identify high-risk churn customers
- Compare customer behavior across countries
- Discover customer segments
- Improve customer retention strategies

---

## 📋 Table of Contents

- [Tools Used](#-tools-used)
- [Dataset Information](#-dataset-information)
- [Repository Structure](#-repository-structure)
- [Getting Started](#-getting-started)
- [Business Questions](#-business-questions)
- [Data Cleaning Process](#-data-cleaning-process)
- [Analysis Performed](#-analysis-performed)
- [Analysis Results](#-analysis-results)
- [Key Insights](#-key-insights)
- [Dashboard Pages](#-power-bi-dashboard-pages)
- [Recommendations](#-recommendations)
- [Project Outcome](#-project-outcome)
- [Future Enhancements](#-future-enhancements)
- [Contact & Resources](#--contact--resources)

---

## 📊 Tools Used

| Tool | Purpose |
|------|---------|
| **Microsoft Excel** | Data cleaning and exploration |
| **SQL** | Data analysis and querying |
| **Power BI** | Interactive dashboard and visualization |

---

## 📁 Dataset Information

The dataset contains information for **10,000 bank customers** across 3 European countries, including the following attributes:

| Column | Description | Data Type |
|--------|-------------|-----------|
| CreditScore | Customer credit score | Numeric |
| Geography | Customer country (Germany, France, Spain) | Categorical |
| Gender | Male/Female | Categorical |
| Age | Customer age | Numeric |
| Tenure | Years with bank | Numeric |
| Balance | Account balance | Numeric |
| NumOfProducts | Number of bank products | Numeric |
| HasCrCard | Credit card ownership (0/1) | Binary |
| IsActiveMember | Active customer status (0/1) | Binary |
| EstimatedSalary | Estimated salary | Numeric |
| Exited | Customer churn status | Binary |

**Churn Definition:**
- `Exited = 1` → Customer churned
- `Exited = 0` → Customer retained

---

## 📂 Repository Structure

```
bank-churn-analysis/
├── data/
│   └── bank_churn_data.csv          # Raw dataset (10,000 records)
├── sql/
│   └── churn_analysis_queries.sql   # SQL queries for analysis
├── excel/
│   └── data_cleaning_and_exploration.xlsx  # Data prep workbook
├── power_bi/
│   └── bank_churn_dashboard.pbix    # Interactive dashboard
├── README.md                         # Project documentation
└── .gitignore
```

---

## 🚀 Getting Started

To explore this project:

1. **View the Dashboard**: Download and open `bank_churn_dashboard.pbix` in Power BI Desktop
2. **Review SQL Analysis**: Check `churn_analysis_queries.sql` for analysis methodology
3. **Examine Data Prep**: Open `data_cleaning_and_exploration.xlsx` for cleaning steps
4. **Explore Data**: Use `bank_churn_data.csv` for your own analysis

**Prerequisites:**
- Power BI Desktop (latest version)
- SQL Client (for running queries)
- Microsoft Excel 2016 or newer

---

## 🎯 Business Questions

The analysis focused on answering the following key questions:

1. What attributes are more common among churned customers?
2. Which customers are most likely to churn?
3. What do the bank's customer demographics look like?
4. Is there a significant difference between customers in Germany, France, and Spain?
5. What distinct customer segments exist within the dataset?

---

## 🧹 Data Cleaning Process

The dataset was cleaned and prepared using Excel and Power BI with the following steps:

**Data Quality Validation:**
- ✓ Checked for missing values across all 11 columns
- ✓ Removed duplicate records
- ✓ Validated data types for each column
- ✓ Identified and handled outliers

**Data Transformation:**
- ✓ Formatted numerical columns (Balance, Salary, Age)
- ✓ Standardized geographic naming conventions
- ✓ Created calculated columns:
  - Age Groups (18-30, 31-40, 41-50, 50+)
  - Product Categories (Single, Multi-Product)
  - Risk Segments (High, Medium, Low)

**Quality Metrics:**
- Missing Values: 0
- Duplicate Records: 0
- Data Completeness: 100%

---

## 🧠 Analysis Performed

### Customer Overview
- Total customers and distribution
- Average account balance and credit score
- Active vs. inactive customer breakdown
- Gender distribution

### Churn Analysis
- **Churn rate by country** (Germany, France, Spain)
- **Churn rate by age group** (4 age bands)
- **Churn by gender** (Male vs. Female)
- **Churn by activity status** (Active vs. Inactive)
- **Churn by number of products** (1, 2, 3, 4 products)

### Country Comparison
Detailed metrics across Germany, France, and Spain:
- Churn rate
- Average balance
- Product ownership patterns
- Customer activity levels
- Demographic profiles

### Customer Segmentation
Customers grouped into 4 distinct segments:
- **High Value Loyal Customers** → Low churn, high balance, multi-product
- **High Value Lost Customers** → High churn, high balance
- **Inactive At-Risk Customers** → High churn, inactive status
- **Low Engagement Users** → Single product, varying activity levels

---

## 📊 Analysis Results

| Metric | Value | Finding |
|--------|-------|---------|
| **Total Customers** | 10,000 | Complete dataset |
| **Overall Churn Rate** | 20.4% | ~2,040 customers churned |
| **Germany Churn Rate** | 32.8% | Highest churn (2x vs. France) |
| **France Churn Rate** | 16.2% | Lowest churn |
| **Spain Churn Rate** | 15.3% | Second-lowest churn |
| **Inactive Churn Rate** | 27.3% | 3.2x higher than active |
| **Active Churn Rate** | 8.5% | Significantly lower risk |
| **Single-Product Churn** | 27.7% | High risk segment |
| **Multi-Product Churn** | 9.6% | Low risk segment |
| **Age 50+ Churn Rate** | 56.0% | Highest age group risk |
| **Age <30 Churn Rate** | 7.6% | Lowest age group risk |

---

## 🔍 Key Insights

1. **🇩🇪 Germany's Churn Crisis**
   - Germany shows the highest churn rate at 32.8% (vs. 16.2% France, 15.3% Spain)
   - This represents a significant revenue risk for the bank

2. **😴 Inactivity = High Risk**
   - Inactive customers are 3.2x more likely to churn (27.3% vs. 8.5% for active)
   - Largest opportunity for intervention

3. **📦 Product Adoption Gap**
   - Single-product customers churn at 27.7% vs. 9.6% for multi-product users
   - Multi-product engagement drives loyalty

4. **💰 The Wealth Paradox**
   - High account balance does NOT guarantee loyalty
   - Customers with $0 balance have higher churn (20.1%) vs. balances >$150K (16.5%)
   - Suggests disengagement across all income levels

5. **👴 Age Factor is Critical**
   - 50+ age group shows 56% churn rate vs. 7.6% for under-30s
   - Age is one of the strongest predictors of churn

6. **👩‍👦 Gender Differences Exist**
   - Female customers show slightly different churn patterns vs. male customers
   - Should inform retention campaign targeting

---

## 📈 Power BI Dashboard Pages

### **Page 1 — Executive Overview**
High-level KPIs for stakeholder decision-making:
- Total customers count
- Overall churn rate
- Average account balance
- Active customers percentage
- Churn distribution by country (visual)

### **Page 2 — Churn Driver Analysis**
Deep-dive into factors influencing churn:
- Age vs. churn (trend analysis)
- Product usage vs. churn (correlation)
- Activity status vs. churn (comparison)
- Balance vs. churn (scatter plot)
- Tenure vs. churn (trend)

### **Page 3 — Customer Segmentation**
Segment performance and characteristics:
- Customer segments breakdown
- Segment churn behavior comparison
- Country-level segment analysis
- Demographics by segment
- Actionable segment insights

---

## 📌 Recommendations

Based on the analysis, the following actions are recommended:

1. **🎯 Improve Engagement Strategies for Inactive Customers**
   - Launch targeted re-engagement campaigns
   - Offer personalized incentives for inactive members
   - Priority: **High** (27.3% churn rate)

2. **💎 Introduce Loyalty Programs for High-Value Customers**
   - Create tiered loyalty rewards for multi-product users
   - Focus on customers with high balance to reduce paradox effect
   - Priority: **High** (Revenue protection)

3. **📱 Encourage Multi-Product Adoption**
   - Develop cross-sell strategies
   - Offer bundled product discounts
   - Target single-product customers for product upsells
   - Priority: **Critical** (3x churn difference)

4. **🎭 Create Country-Specific Retention Campaigns**
   - Germany-focused intervention strategy (32.8% churn)
   - Investigate root causes in Germany vs. other countries
   - Localize retention messaging by country
   - Priority: **Critical** (Regional disparity)

5. **🔔 Target High-Risk Age Segments**
   - Develop 50+ customer retention program
   - Tailor communication for different age groups
   - Consider life stage relevant offerings
   - Priority: **High** (56% churn for 50+)

6. **📊 Continuous Monitoring of Churn Trends**
   - Set up monthly churn monitoring dashboard
   - Create early-warning system for at-risk customers
   - Track campaign effectiveness
   - Priority: **Medium** (Ongoing)

---

## 🚀 Project Outcome

This project demonstrates expertise in:

- **Data Cleaning & Preparation** — Ensuring 100% data quality
- **SQL Analysis** — Complex queries for multi-dimensional analysis
- **Business Intelligence** — Professional Power BI dashboard design
- **Data Storytelling** — Clear communication of insights to stakeholders
- **Dashboard Design** — Interactive, user-friendly visualizations
- **Customer Segmentation** — Advanced analytical techniques
- **Business Acumen** — Translation of data to actionable recommendations

**Impact:** This analysis provides the bank with clear, data-driven strategies to reduce churn and improve customer retention, potentially protecting significant revenue.

---

## 🔮 Future Enhancements

Potential extensions to this project:

- 🤖 **Predictive Churn Model** — Machine learning model to predict churn probability
- 📈 **RFM Analysis** — Recency, Frequency, Monetary value segmentation
- 🔄 **Cohort Analysis** — Track customer behavior by acquisition period
- 📅 **Seasonal Trends** — Identify seasonal churn patterns
- 💰 **CLV Modeling** — Customer Lifetime Value predictions
- 🎯 **Campaign Attribution** — Measure retention campaign effectiveness
- 🌍 **Geographic Deep-Dive** — Root cause analysis for Germany's high churn
- 📱 **Real-Time Dashboard** — Live data integration for continuous monitoring

---

## 👤 Contact & Resources

**Author:** Matthew Mordi  
**Title:** Aspiring BI / Data Analyst  
**GitHub:** [@mattmordi](https://github.com/mattmordi)

**Built with:**
- Excel | SQL | Power BI

**Last Updated:** May 8, 2026

---

**If you found this project helpful, please consider giving it a ⭐ on GitHub!**
