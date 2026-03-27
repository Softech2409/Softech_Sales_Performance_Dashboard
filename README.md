# Sales Performance Dashboard | Power BI Portfolio Project

An end-to-end **Power BI analytics solution** built to support executive decision-making across sales performance, customer segmentation, product performance, target attainment, and geographical analysis.

This project was designed to move beyond static reporting and deliver **actionable business intelligence** through interactive dashboards, strong data modeling, and advanced DAX.

---

## Project Overview

This dashboard suite answers key business questions such as:

- How is the business performing against revenue, profit, and margin targets?
- Which products, categories, and regions are driving growth?
- Where is the business underperforming?
- What customer segments contribute most to revenue?
- How can leaders prioritize actions based on performance insights?

The solution is structured into multiple report pages for focused decision-making:

1. **Executive Overview**
2. **Sales Trends Analysis**
3. **Product & Category Performance**
4. **Geographical Analysis**
5. **Customer Segmentation**
6. **Target Attainment**

---

## Business Objectives

The dashboard was built to support:

- Executive performance monitoring
- Revenue, profit, and margin analysis
- Target vs actual performance tracking
- Customer segmentation and retention analysis
- Product and category profitability analysis
- Regional and country-level performance review
- Action-oriented business recommendations

---

## Key Insights Delivered

- Revenue reached **$12.98M** with strong year-over-year growth
- Orders increased significantly, signaling strong demand expansion
- Revenue remained **below target**, highlighting a performance gap
- **Electronics** emerged as the leading category by contribution
- **Europe** was the strongest revenue region
- Customer base showed high retention, with a **99.5% repeat rate**
- Approximately **73% of customers placed 16–25 orders**, indicating a strong mid-frequency customer base
- Late-year performance improved, with the strongest monthly results in Q4

---
## Data Model (Semantic Model Design)

The solution is built on a **star schema model** optimized for performance and scalability.

![Data Model](images/data-model.png)

### Model Highlights:
- Central **FactSales** table (transactional grain)
- Dimension tables:
  - DimCustomer
  - DimProduct
  - DimRegion
  - Date (Calendar table)
  - DimMonth
- Target tables:
  - TargetsByCategory
  - TargetsOverall_Monthly

### Design Approach:
- One-to-many relationships (dimension → fact)
- Single-direction filtering for performance
- Separate target tables for flexible variance analysis
- Time intelligence enabled via dedicated calendar table

---

## Dashboard Screenshots

### Executive Overview
![Executive Overview](images/executive-overview.png)

---

### Sales Trends Analysis
![Sales Trends](images/sales-trends-analysis.png)

---

### Product & Category Performance
![Product Performance](images/product-category-performance.png)

---

### Geographical Analysis
![Geographical Analysis](images/geographical-analysis.png)

---

### Customer Segmentation
![Customer Segmentation](images/customer-segmentation.png)

---

### Target Attainment
![Target Attainment](images/target-attainment.png)

## Dashboard Pages

### 1. Executive Overview
Provides a high-level summary of revenue, profit, margin, growth, and executive decision points.

**Highlights:**
- KPI cards
- decision panel
- best/worst month annotations
- trend summary
- top category breakdown

---

### 2. Sales Trends Analysis
Focuses on monthly, quarterly, and year-over-year performance patterns.

**Highlights:**
- revenue and profit trend analysis
- monthly performance matrix
- quarterly underperformance vs target
- profit margin trend

---

### 3. Product & Category Performance
Analyzes product, brand, and category contribution to revenue and profitability.

**Highlights:**
- top category and top brand
- product profitability quadrant
- brand revenue rank trend
- product performance table

---

### 4. Geographical Analysis
Examines sales performance by region and country.

**Highlights:**
- top revenue region
- top growth region
- country performance quadrant
- monthly revenue heatmap by region
- regional performance summary

---

### 5. Customer Segmentation
Segments customers based on behavior and value to support retention and growth strategy.

**Highlights:**
- repeat rate analysis
- revenue per customer
- customer performance quadrant
- top customers by revenue
- customer distribution by order frequency

---

### 6. Target Attainment
Measures revenue performance against targets and highlights where the business is over- or under-performing.

**Highlights:**
- revenue attainment, profit attainment, and margin attainment
- revenue variance by category
- revenue vs target by month
- best/worst month logic
- category-level attainment analysis

---

## Tools & Technologies

- **Power BI Desktop**
- **Power Query**
- **DAX**
- **Excel / CSV data sources**
- **Star schema data modeling**

---

## Data Model

The solution follows a **star schema** design for performance and scalability.

### Core model components:
- **Fact table**
  - sales / transactional data
- **Dimension tables**
  - date
  - customer
  - product
  - brand
  - category
  - region
  - country
  - segment

### Modeling approach:
- one-to-many relationships from dimensions to fact
- single-direction filtering for clarity and performance
- reusable dimensions for slicing and drill-down
- date intelligence support through dedicated calendar structure

---

## DAX Highlights

This project uses advanced DAX to support dynamic business analysis, including:

- target attainment %
- revenue variance %
- year-over-year growth
- month-over-month growth
- top/bottom N ranking
- best/worst month detection
- customer segmentation logic
- revenue vs average month logic
- dynamic label formatting
- quadrant classification logic

### Example use cases:
- identifying strongest and weakest performing months
- ranking categories and customers dynamically
- comparing revenue against target and against average
- classifying customers into behavioral segments
- surfacing executive-level insight statements

---

## Design Approach

This project was intentionally designed for **executive readability**.

### Design principles used:
- clean page hierarchy
- KPI-first storytelling
- limited but meaningful color use
- insight cards with action-oriented commentary
- dynamic annotations for peaks, risk, and opportunity
- focused visuals instead of cluttered reporting pages

---

## Business Value

This solution helps decision-makers:

- identify growth drivers quickly
- spot underperformance early
- assess whether growth is sustainable
- understand customer behavior and retention
- allocate resources across product lines and regions
- make data-driven strategic decisions

---

## Repository Structure

```text
Sales-Performance-Dashboard/
│
├── README.md
├── /pbix
│   └── Sales Performance Dashboard.pbix
├── /images
│   ├── executive-overview.png
│   ├── sales-trends-analysis.png
│   ├── product-category-performance.png
│   ├── geographical-analysis.png
│   ├── customer-segmentation.png
│   └── target-attainment.png
├── /dataset
│   └── source-data.xlsx
└── /case-study
    └── Oil_Gas_Case_Study.pptx
