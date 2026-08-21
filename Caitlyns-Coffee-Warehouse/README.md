# ☕ Caitlyn's Coffee Warehouse
## End-to-End Power BI Business Intelligence Project

![Power BI](https://img.shields.io/badge/Power%20BI-Data%20Visualization-F2C811?logo=powerbi&logoColor=black)
![Power Query](https://img.shields.io/badge/Power%20Query-Data%20Transformation-217346)
![DAX](https://img.shields.io/badge/DAX-Business%20Intelligence-5A5A5A)
![Excel](https://img.shields.io/badge/Excel-Source%20Data-217346?logo=microsoftexcel&logoColor=white)

---

## 📊 Project Overview

**Caitlyn's Coffee Warehouse** is an end-to-end Power BI portfolio project designed to simulate a business intelligence solution for a growing coffee wholesale, retail, and e-commerce operation.

The project began with raw operational data stored in Excel and progressed through data review, cleaning, transformation, modeling, DAX measure development, dashboard design, and business analysis.

The final Power BI report provides management with three analytical views:

1. **Executive Overview**
2. **Invoice & Expense Operations**
3. **Sales & Customer Performance**

The goal was not simply to create visualizations, but to develop a reporting solution capable of answering practical business questions related to profitability, revenue trends, expenses, invoice performance, customers, products, and sales channels.

---

# 📈 Final Business Intelligence Solution

The completed report provides leadership with a high-level view of company performance while allowing deeper analysis of operational and customer activity.

### Key Performance Indicators

| KPI | Result |
|---|---:|
| Net Revenue | **$494K** |
| Gross Revenue | **$521.3K** |
| Total Costs | **$288.5K** |
| Net Profit | **$205.5K** |
| Discount Impact | **$27.3K** |
| Total Units Sold | **34K** |
| Customer Count | **10** |
| Total Invoice Count | **140** |
| Average Invoice Amount | **$2.06K** |
| Average Days to Pay | **17 Days** |
| Open Invoice Count | **5** |
| Overdue Invoice Count | **3** |
| Overdue Amount | **$6.7K** |

---

# 🛠️ Tools & Skills Demonstrated

### Power BI
- Interactive dashboard development
- KPI reporting
- Data visualization
- Cross-filtering and slicers
- Report page design
- Business-focused visual selection
- Data modeling
- Relationship management

### Power Query
- Data cleaning and transformation
- Conditional columns
- Business-rule mapping
- Column standardization
- Data type management
- Value replacement
- Column removal and reordering
- Query preparation

### DAX
- Revenue calculations
- Cost calculations
- Profit calculations
- Invoice counts
- Open and overdue balances
- Discount analysis
- Customer counts
- Unit counts
- Average invoice calculations
- Payment lifecycle analysis
- Date-based calculations using `DATEDIFF`

### Excel
- Raw source data preparation
- Pivot-table validation
- Revenue review
- Cost review
- Source-data quality checks

---

# 🎯 Business Questions

The report was designed to answer questions such as:

- How much revenue is the business generating?
- What are total operating costs?
- Is the company profitable?
- How does revenue compare with costs throughout the year?
- Which sales channels generate the most revenue?
- Which products and product categories drive sales?
- Which customers contribute the most revenue?
- Which locations generate the strongest performance?
- Which vendors and suppliers account for the most spending?
- Which departments generate the greatest costs?
- How many invoices remain open or overdue?
- How quickly are invoices typically paid?
- How does invoice activity change throughout the year?
- What financial impact are customer discounts having?

---

# 1️⃣ Raw Data Review

Before building the Power BI model, I reviewed the revenue and cost datasets to understand the structure, identify inconsistencies, and determine which fields would be required for analysis.

Pivot tables were used during the initial review process to examine the raw data and validate totals.

## Revenue Data Review

![Revenue Raw Pivot Table 1](./images/CC%20Warehouse%20Rev%20Raw%20Pivot%20Table%201.png)

![Revenue Raw Pivot Table 2](./images/CC%20Warehouse%20Rev%20Raw%20Pivot%20Table%202.png)

## Cost Data Review

![Cost Raw Pivot Table](./images/CC%20Warehouse%20Cost%20Raw%20Pivot%20Table.png)

This stage helped establish the business logic that would later be incorporated into Power Query transformations and DAX measures.

---

# 2️⃣ Data Cleaning & Transformation

The raw datasets required multiple transformations before they could support reliable reporting.

Power Query was used to create a repeatable transformation process rather than manually modifying the source data.

Transformation work included:

- Standardizing field names
- Correcting inconsistent values
- Assigning customer identifiers
- Mapping business categories
- Standardizing payment information
- Reordering and removing unnecessary columns
- Creating conditional columns
- Applying appropriate data types
- Preparing revenue and cost tables for the data model

## Conditional Mapping

Business rules were translated into conditional logic to standardize fields and assign identifiers.

For example, customer names were mapped to standardized Customer IDs.

![Conditional Column Mapping](./images/Conditonal%20Column%20Mapping.png)

Additional conditional logic was used throughout the transformation process.

![Conditional Column Mapping 2](./images/Conditonal%20Column%20Mapping%202.png)

## Transformation Workflow

Rather than making one-time manual edits, the transformation logic was captured as repeatable **Applied Steps** in Power Query.

This allows the same cleaning and transformation process to be applied when the underlying data is refreshed.

---

# 3️⃣ Data Modeling

After transformation, the datasets were loaded into the Power BI data model.

The model includes:

- **Revenue Table**
- **Costs Table**
- **Date Table**
- **Dedicated Measures Table**

A shared Date table supports time-based reporting across revenue and cost activity.

![Power BI Model View](./images/Model%20View.png)

The model separates transactional data from calculated measures, helping keep the report organized and making KPI development easier to maintain.

---

# 4️⃣ DAX Measure Development

A dedicated Measures table was created to centralize business calculations.

Measures developed during the project include:

- Gross Revenue
- Net Revenue
- Total Costs
- Net Profit
- Discount Rate
- Discount Impact
- Total Invoice Count
- Paid Invoice Count
- Open Invoice Count
- Overdue Invoice Count
- Paid Amount
- Open Amount
- Overdue Amount
- Average Invoice Amount
- Average Days to Pay
- Customer Count
- Total Units Sold
- Invoices Created
- Invoices Due
- Invoices Paid

## Measure Development & Validation

Measures were developed incrementally and tested before being incorporated into the final dashboard.

![Measures Table Test](./images/Measures%20Table%20Test.png)

![Measures Test Table](./images/Measures%20Test%20Table%202.png)

As additional business requirements were identified, the measure set was expanded.

![Measures Table Update](./images/Measures%20Table%20Update%203.png)

Invoice-specific measures were then added to support operational reporting.

![Measures Table Invoice Update](./images/Measures%20Table%20Update%20for%20Invoices.png)

---

# 5️⃣ Payment Lifecycle Analysis

One objective of the project was to move beyond basic revenue reporting and evaluate operational performance.

A DAX measure using `DATEDIFF` was developed to calculate the average number of days between invoice creation and payment for paid invoices.

![DATEDIFF Formula](./images/DATEDIFF%20FORMULA.png)

This produced an **Average Days to Pay of 17 days**, providing management with a straightforward indicator of payment-cycle performance.

---

# 6️⃣ Dashboard Development Process

The dashboard was developed iteratively.

Instead of immediately focusing on visual styling, I first validated the measures, filters, relationships, and visual behavior.

## Phase 1 — Initial Dashboard

The first phase established the report structure and core visuals.

![Phase One](./images/PHASE%20ONE%20OF%20DASHBOARD.png)

## Phase 2 — Visual Development

Additional visualizations were introduced to evaluate revenue, costs, sales channels, and other business dimensions.

![Phase Two](./images/PHASE%202%20WITH%20VISUALS.png)

## Phase 3 — Filtering & Interaction Review

Filtering behavior and visual interactions were reviewed before moving into final design.

![Phase Three](./images/PHASE%203%20DASHBOARDING-SHOWS%20FILTERING%20AFTER%20REVIEW.png)

## Phase 4 — KPI Development

The KPI set was completed before final formatting and layout decisions were made.

![Phase Four](./images/PHASE%204%20ALL%20KPIS%20CREATED%20BEFORE%20EDITING.png)

## Phase 5 — Layout Refinement

Visuals and KPI cards were reorganized to create a clearer reporting hierarchy.

![Phase Five](./images/PHASE%205%20REORDER%20OF%20TILES%20FOR%20VISUALS.png)

## Phase 6 — Executive Dashboard Design

The Executive Overview was redesigned into a management-focused dashboard.

![Phase Six](./images/PHASE%206%20FINAL%20DESIGN.png)

## Phase 7 — Expanded Sales & Customer Reporting

The project was expanded with dedicated Sales & Customer Performance reporting.

![Phase Seven](./images/PHASE%207%20DASHBOARD%20FINAL%20DESIGN%20S%20AND%20C.png)

---

# 📊 Report Page 1 — Executive Overview

The **Executive Overview** provides leadership with an immediate snapshot of overall business performance.

Key KPIs include:

- Net Revenue
- Total Costs
- Net Profit
- Overdue Amount
- Open Invoice Count

Supporting visualizations allow users to evaluate:

- Monthly revenue versus costs
- Revenue by sales channel
- Costs by category
- Performance by location
- Monthly performance through interactive filtering

The page is intended to answer the first question an executive or manager would ask:

> **How is the business performing overall?**

![Executive Overview](./images/PHASE%206%20FINAL%20DESIGN.png)

---

# 🧾 Report Page 2 — Invoice & Expense Operations

The **Invoice & Expense Operations** page focuses on the operational side of the business.

It provides visibility into:

- Total invoice volume
- Average invoice amount
- Average payment time
- Open invoices
- Overdue invoices
- Vendor and supplier spending
- Payment status
- Department expenses
- Monthly invoice lifecycle
- Individual invoice details

This page allows users to move from high-level financial performance into the operational activity contributing to those results.

---

# 👥 Report Page 3 — Sales & Customer Performance

The **Sales & Customer Performance** page analyzes where revenue is coming from and how customers interact with the business.

![Sales and Customer Performance](./images/PHASE%207%20DASHBOARD%20FINAL%20DESIGN%20S%20AND%20C.png)

Analysis includes:

- Revenue by Product ID
- Revenue by Product Category
- Revenue by Location
- Revenue by Customer
- Product activity by customer
- Net Revenue
- Gross Revenue
- Total Units Sold
- Discount Impact
- Customer Count

This page allows management to identify the customers, products, categories, and locations contributing most heavily to business performance.

---

# 💡 Business Insights

The completed analysis highlights several important business observations.

### Revenue & Profitability

The business generated approximately **$521.3K in gross revenue** and **$494K in net revenue**.

Against approximately **$288.5K in total costs**, the company generated approximately **$205.5K in net profit**.

This represents a net profit margin of approximately **41.6% of net revenue**.

### Sales Channel Performance

Wholesale activity represents the largest source of net revenue, significantly exceeding online and retail café activity.

This indicates that wholesale relationships are a major component of the company's revenue model.

### Product Performance

Wholesale beans represent the strongest product category by revenue.

The **CF-BEAN-05** product is particularly prominent in the product-level revenue analysis.

### Discount Impact

Customer discounts reduced gross revenue by approximately **$27.3K**, representing a discount rate of approximately **5.24%**.

Tracking discount impact provides management with visibility into how pricing decisions affect realized revenue.

### Expense Concentration

Inventory-related spending represents the largest cost category.

At the department level, **Retail/Sales Admin** accounts for approximately **$143K**, or roughly half of total costs.

This makes inventory and sales-related operating expenses important areas for continued monitoring.

### Accounts Payable / Invoice Performance

The dataset contains **140 invoices**, with an average invoice value of approximately **$2.06K**.

Invoices are paid in approximately **17 days on average**.

At the reporting point shown in the dashboard:

- **5 invoices remain open**
- **3 invoices are overdue**
- Approximately **$6.7K is overdue**

These KPIs provide a concise operational view of outstanding obligations and payment performance.

---

# 📅 Revenue & Cost Trend Analysis

Daily revenue and cost activity was also evaluated during development.

![Revenue and Total by Date](./images/rev%20and%20total%20by%20date.png)

Reviewing the data at different levels of granularity helped determine that monthly aggregation provided a clearer executive-level trend while detailed transaction data remained available for deeper analysis.

---

# 🔄 Project Workflow

The overall project followed the following BI development process:

**Raw Excel Data**  
↓  
**Initial Data Review & Validation**  
↓  
**Power Query Cleaning & Transformation**  
↓  
**Business Rule Mapping**  
↓  
**Data Modeling**  
↓  
**Date Table & Relationships**  
↓  
**DAX Measure Development**  
↓  
**KPI Validation**  
↓  
**Dashboard Development**  
↓  
**Filter & Interaction Testing**  
↓  
**Layout & Design Refinement**  
↓  
**Business Analysis**  
↓  
**Final Three-Page Power BI Report**

---

# 📁 Repository Structure

```text
Caitlyns-Coffee-Warehouse/
│
├── README.md
│
├── Caitlyns-Coffee-Warehouse.pbix
│
├── data/
│   └── Caitlyns Coffee Warehouse Data.xlsx
│
├── images/
│   ├── Raw data validation screenshots
│   ├── Power Query transformation screenshots
│   ├── Data model screenshot
│   ├── DAX development screenshots
│   ├── Dashboard development screenshots
│   └── Final dashboard screenshots
│
└── documentation/
    └── Caitlyns-Coffee-Warehouse-Portfolio.pdf
```

---

# 📂 Project Files

### Power BI Report
The `.pbix` file contains the complete interactive Power BI report, data model, DAX measures, Power Query transformations, and dashboard pages.

### Source Data
The `data` folder contains the Excel workbook used as the project's source dataset.

### Screenshots
The `images` folder documents the development process from raw-data review through final dashboard design.

### Portfolio Documentation
The `documentation` folder contains a PDF portfolio version of the project for convenient review without Power BI Desktop.

---

# 🧠 What I Learned

This project allowed me to practice the complete Power BI development lifecycle rather than focusing only on visualization.

Key areas of development included:

- Translating raw operational data into a structured analytical model
- Identifying and applying business rules during transformation
- Building repeatable Power Query workflows
- Creating and validating DAX measures
- Designing KPIs around actual business questions
- Creating a shared Date table for time-based analysis
- Evaluating data at different levels of granularity
- Troubleshooting model and calculation issues
- Designing dashboards for different audiences
- Separating executive reporting from operational analysis
- Using visual hierarchy to improve dashboard usability
- Translating technical analysis into business insights

One of the most important lessons from the project was that effective business intelligence requires more than creating charts. The data must first be understood, cleaned, structured, modeled, validated, and connected to meaningful business questions.

---

# 🚀 Future Enhancements

Potential future enhancements include:

- SQL-based source data
- Automated data refresh
- Additional time-intelligence measures
- Year-over-year comparisons
- Budget versus actual analysis
- Profit margin by product and customer
- Customer segmentation
- Vendor performance metrics
- Drill-through reporting
- Additional tooltip pages
- Forecasting
- Power BI Service deployment

---

# 👩‍💻 About This Project

This project was created as part of my transition into **Data Analytics and Business Intelligence**.

My professional background includes financial services, operational reporting, process improvement, employee training, workflow development, and business problem solving. I am currently expanding that experience through hands-on projects using Power BI, Power Query, DAX, Excel, data modeling, and data visualization.

The goal of this portfolio is to demonstrate not only technical skills, but my ability to take a business problem from raw data through analysis and communicate the results in a format that supports decision-making.

---

### Built with
**Power BI • Power Query • DAX • Excel • Data Modeling • Data Visualization • Business Intelligence**

⭐ Thank you for viewing Caitlyn's Coffee Warehouse!
