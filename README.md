# Omnichannel Retail Sales and Inventory Analytics Dashboard

## Project Overview
This project focuses on building an **Executive Overview Dashboard** for retail sales analysis using a transactional retail dataset. The dashboard is designed to help business users monitor key performance indicators such as revenue, orders, customers, average order value, monthly revenue trend, customer segment contribution, shipping mode distribution, and average shipping delay.

The current version of the project includes:
- Data cleaning in **Google Colab**
- SQL analysis in **MySQL**
- Power BI **Page 1 Executive Overview Dashboard**
- Insight generation and reporting
- GitHub documentation for final submission

This project is built as the **foundation of a larger Omnichannel Retail Analytics solution**, with future expansion planned for product analysis, geographic analysis, and inventory-focused insights.

---

## Business Objective
The objective of this project is to create a simple and interactive executive-level dashboard that answers the following questions:

- What is the total revenue generated?
- How many orders and customers are there?
- What is the average order value?
- How does revenue change over time?
- Which customer segments contribute the most revenue?
- How is revenue distributed across shipping modes?
- What is the average shipping delay?

---

## Dataset Information

### Files Used
- `train.csv` → Raw dataset
- `cleaned_train.csv` → Cleaned dataset used for analysis

### Dataset Type
Retail transactional order dataset (Superstore-style)

### Key Columns Used in Current Dashboard
- `Order ID`
- `Order Date`
- `Ship Date`
- `Ship Mode`
- `Customer ID`
- `Segment`
- `Sales`

### Additional Columns Available for Future Expansion
- `Region`
- `State`
- `City`
- `Category`
- `Sub-Category`
- `Product Name`
- `Product ID`
- `Postal Code`

---

## Dataset Limitations
The dataset does **not** contain:
- Profit
- Quantity
- Actual inventory stock levels
- Return / refund details
- Cost or margin data

Because of this:
- Profitability analysis is not included
- Quantity-based demand analysis is not included
- Inventory-related insights are conceptual and planned for future versions

> Inventory-related insights in this project are inferred at a conceptual level using sales trends and operational indicators, since the current dashboard version is focused on executive sales monitoring and the dataset does not include direct stock-level or quantity information.

---

## Tools & Technologies
- **Google Colab** – Data cleaning and preprocessing
- **Python (Pandas, NumPy)** – Data transformation and validation
- **MySQL** – SQL queries and metric extraction
- **Power BI** – Dashboard creation
- **GitHub** – Version control and documentation

---

## Project Workflow

### Week 1: Data Cleaning and Preprocessing
- Loaded `train.csv` in Google Colab
- Checked data structure using `df.info()`
- Verified missing values
- Converted `Order Date` and `Ship Date` to proper date format
- Cleaned formatting issues such as `Postal Code`
- Exported final cleaned file as `cleaned_train.csv`

### Week 2: SQL Analysis in MySQL
- Imported `cleaned_train.csv` into MySQL
- Created working table: `cleaned_train`
- Calculated:
  - Total Revenue
  - Total Orders
  - Total Customers
  - Average Order Value
  - Revenue by Segment
  - Revenue by Ship Mode
  - Monthly Revenue Trend
  - Average Shipping Delay

### Week 3: Power BI Dashboard Development
Built **Page 1 – Executive Overview Dashboard** containing:
- KPI Cards:
  - Total Revenue
  - Total Orders
  - Total Customers
  - Average Order Value
  - Average Shipping Delay
- Visuals:
  - Monthly Revenue Trend
  - Revenue by Segment
  - Revenue by Ship Mode
- Slicers / Filters (based on final dashboard design)

### Week 4: Insight Generation and Final Submission
- Interpreted the completed dashboard
- Extracted executive-level insights
- Wrote business recommendations
- Captured dashboard screenshots
- Finalized GitHub documentation

---

## Completed Dashboard Scope

### ✅ Completed
**Page 1 – Executive Overview Dashboard**

### Included KPIs
- Total Revenue
- Total Orders
- Total Customers
- Average Order Value
- Average Shipping Delay

### Included Visuals
- Monthly Revenue Trend
- Revenue by Segment
- Revenue by Ship Mode

---

## Dashboard Preview

### Page 1 – Executive Overview
_Add your Power BI screenshot here after uploading it to GitHub._

Example:
```md
![Executive Overview Dashboard](dashboard/screenshots/page1_executive_overview.png)
```

---

## Key Metrics
- **Total Revenue** = `SUM(Sales)`
- **Total Orders** = `DISTINCTCOUNT(Order ID)`
- **Total Customers** = `DISTINCTCOUNT(Customer ID)`
- **Average Order Value** = `Total Revenue / Total Orders`
- **Average Shipping Delay** = Average days between `Order Date` and `Ship Date`

---

## Key Insights (Page 1 Only)
- The dashboard provides a centralized executive summary of retail performance in a single page.
- Monthly revenue trend shows that demand changes over time rather than remaining constant.
- Customer segment contribution is not evenly distributed, indicating that some segments are more valuable than others.
- Revenue by ship mode provides operational visibility into fulfillment patterns.
- Including average shipping delay improves the business usefulness of the dashboard beyond pure sales reporting.

---

## Business Recommendations
- Use the dashboard as the first layer of executive business monitoring.
- Review monthly revenue patterns regularly to identify strong and weak periods.
- Focus retention and marketing efforts on the highest-performing customer segments.
- Evaluate ship mode usage from both revenue and delivery efficiency perspectives.
- Expand the dashboard into product, geography, and inventory-focused analytical pages.

---

## Current Scope vs Future Scope

### Current Scope
- Data cleaning in Google Colab
- SQL metric extraction in MySQL
- Power BI Page 1 Executive Overview dashboard
- Insight generation and reporting

### Future Scope
Planned future dashboard pages:
- **Page 2:** Product and Category Analysis
- **Page 3:** Geographic Sales Analysis
- **Page 4:** Inventory and Operations Insights

This project is intentionally structured as a scalable analytics solution, where the current version focuses on building a strong executive summary dashboard as the foundation.

---

## Repository Structure

```bash
Omnichannel-Retail-Sales-and-Inventory-Analytics-Dashboard/
│── README.md
├── data/
│   ├── raw/
│   │   └── train.csv
│   └── processed/
│       └── cleaned_train.csv
│
├── notebooks/
│   └── data_cleaning_and_eda.ipynb
│
├── sql/
│   ├── schema.sql
│   └── week2_business_queries.sql
│
├── dashboard/
│   ├── Omnichannel_Retail_Dashboard.pbix
│   └── screenshots/
│       └── page1_executive_overview.png
│
├── reports/
│   └── final_project_report.pdf
│

```

---

## How to Reproduce This Project

1. Open the notebook in **Google Colab**
2. Run the data cleaning steps on `train.csv`
3. Export the cleaned dataset as `cleaned_train.csv`
4. Import `cleaned_train.csv` into **MySQL**
5. Create the table: `cleaned_train`
6. Run the SQL queries for business metrics
7. Load `cleaned_train.csv` into **Power BI**
8. Build **Page 1 – Executive Overview Dashboard**
9. Save the `.pbix` file
10. Capture the dashboard screenshot and upload it to GitHub

---

## Limitations
- Only **Page 1 (Executive Overview)** is completed in the current version
- The dataset does not include Profit
- The dataset does not include Quantity
- The dataset does not include real inventory stock levels
- Product-level and geography-level pages are planned for future versions

---

## Conclusion
This project successfully delivers a clean and interactive **Executive Overview Dashboard** for retail sales monitoring using Google Colab, MySQL, and Power BI.

The current version provides a strong foundation for:
- executive KPI tracking
- sales trend monitoring
- customer segment analysis
- shipping mode analysis
- operational visibility through shipping delay

It also creates a clear roadmap for future expansion into:
- product analysis
- geographic analysis
- inventory and operational planning
