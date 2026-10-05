# 💳 Credit Card Customer Analytics & Churn Analysis | Power BI

An interactive **4-page Power BI dashboard** built to analyze credit card customer behavior, spending, payment activity, credit utilization, churn, retention, and customer risk across **2021–2026**.

The project focuses on multi-table data modeling, DAX-based KPI development, segmentation, churn analysis, and interactive business intelligence reporting.

> **Data Note:** This is an independent portfolio project using non-sensitive portfolio data. It does not contain any proprietary or confidential banking data.

---

## 📊 Dashboard Overview

The report contains four analytical sections:

### 1. Executive Overview

Provides a consolidated view of customer and portfolio performance.

Key KPIs include:

- Total Spend
- Total Customers
- Average Transactions per Customer
- Churn Rate
- Average Transaction Value
- Credit Utilization
- Spend by Segment
- Customers by Region

The page provides an executive-level view of customer activity and portfolio trends.

---

### 2. Customer Behavior

Analyzes how customers interact with their credit cards.

Key analyses include:

- Average Customer Spend
- Transactions per Customer
- Average Transaction Value
- Spend by Category
- Transactions by Customer Segment
- Income Band Distribution
- Customer spending by state
- Top customers by total spend

The analysis helps identify high-value customer groups and changes in customer activity over time.

---

### 3. Churn & Retention

Focuses on customer lifecycle and churn behavior.

Key KPIs:

- Total Churn
- Churn Rate
- Customer Retention Rate
- Retained Customers

Key analyses:

- Churn trends over time
- Retained customer trends
- Churn by customer segment
- Churn by region
- Geographic distribution of churn

This page is designed to identify segments and regions requiring customer-retention strategies.

---

### 4. Credit Risk

Analyzes financial exposure and repayment behavior.

Key KPIs:

- Average Credit Limit
- Average Balance
- Payment Rate
- Average Utilization

Key analyses:

- Credit Limit vs. Balance
- Total Payments
- High-risk customers
- Payment type distribution
- Customer-level utilization
- Customer-level payment ratio
- Risk-level segmentation

---

## 🗂️ Dataset

The project uses approximately **87K records across five related datasets**.

| Dataset | Records | Purpose |
|---------|--------:|---------|
| `customers.csv` | **5,000** | Customer demographics, segmentation and churn |
| `transactions.csv` | **30,000** | Customer spending and transaction behavior |
| `payments.csv` | **15,000** | Repayment behavior |
| `usage_metrics.csv` | **37,000** | Monthly customer usage and credit metrics |
| `regions.csv` | **10** | State-to-region mapping |

The dashboard therefore combines customer-level, transaction-level and monthly usage information rather than relying on a single flat table.

---

## 🔗 Data Model

The Power BI model connects customer-level and transactional data through common keys.

### Core Relationships

```text
                    ┌───────────────┐
                    │   Customers   │
                    │ customer_id   │
                    └───────┬───────┘
                            │
          ┌─────────────────┼─────────────────┐
          │                 │                 │
          ▼                 ▼                 ▼
   Transactions         Payments       Usage Metrics
          │
          │
          ▼
       Regions
     state → region
