# 💼 Sales-Margin-Performance-Suite-A-Data-Driven-Approach-to-Product-and-Segment-Intelligence
#  

## 📌 Introduction  
The **Executive Sales & Margin Report** provides business stakeholders with a powerful visual dashboard for tracking sales, profit, and margin performance across product lines, customer segments, and time periods. Built with Power BI, this interactive report leverages key performance indicators (KPIs) such as **Sales YTD**, **Sales MTD**, **Sales PY**, and **Profit Margin %** to uncover insights into seasonal patterns, product performance, and customer profitability. This analysis supports strategic decision-making and drives growth through data-informed actions.

## 🚨 Problem Statement  
In many business settings, decision-makers lack a unified view of sales and profitability trends broken down by customer segments and product categories. Challenges include:

- Identifying underperforming vs. high-performing customer segments.
- Tracking profit margin fluctuations over time.
- Detecting seasonal or cyclical performance patterns.
- Understanding how product and shipping strategies impact returns and profits.

The goal of this report is to solve these challenges using dynamic Power BI visualizations and advanced data modeling techniques.

---

## 🔍 1. Key Business Questions  
To guide the analysis, I posed the following questions to our key stakeholders:

- Which customer segments generate the highest total profit and margins?
- What is the quarter-over-quarter and month-over-month sales momentum?
- Are there seasonal trends or consistent patterns in monthly performance?
- Which products contribute most to sales, profit, and unit volume?
- How do shipping, discounts, and customer types influence return rates and net profit?

---

## 🗃️ 2. Dataset Overview  
The report leverages a star schema consisting of multiple dimension tables and a central fact table. Key tables include:

### 📦 `Fact Table`
- `Sales`, `Profit`, `Discount`, `COGS`, `Manufacturing Price`, `Month Name`, `Product`, `Date`
- Central source for transactional metrics and derived financial KPIs

### 🛍️ `DimProduct`
- `Product`, `Product_ID`
- Provides product metadata for category analysis

### 🌍 `DimCountry`
- `Country`, `Country_ID`
- Enables country-level filtering and analysis

### 👥 `DimSegment`
- `Segment`, `Segment_ID`
- Supports segmentation (Enterprise, Small Business, Government, etc.)

### 📅 `DimDate`
- `Date`, `MonthName`, `MonthNumber`
- Allows time-based aggregations (YTD, QTD, MTD, PY)

### 🧮 `Core Financial Measures` & `Time-Based Insight Measures`
- Includes DAX-calculated fields such as:
  - `Total Sales`, `Total Profit`, `Profit Margin`, `Sales Growth %`, `Sales YTD`, `Sales MTD`, `Sales PY`, `Sales QTD`

---

## 🧹 3. Data Cleaning & Transformation  
Key transformation steps in Power Query and DAX:

- Removed nulls and duplicates in date and product columns
- Created time-based aggregations (YTD, MTD, QTD, PY)
- Segmented customer data into predefined categories
- Derived new metrics like Profit Margin %, Average Profit per Unit
- Standardized text fields and numeric formatting for dashboard usability
- Built relationships between all tables using keys (Product_ID, Country_ID, Segment_ID, Date)

---

## 🧠 4. Data Modelling  
 
The model was designed using a star schema structure, ensuring high performance and clarity in DAX calculations. It supports slicing data by country, segment, month, and product while aggregating performance metrics dynamically.
![Modelling Sales](https://github.com/user-attachments/assets/444edc52-e7c6-40e1-bd24-9514092e4b2a)

---

## 📈 5. Data Analysis & Visualizations

### 🔹 Executive Summary - Page 1  

<img width="1453" height="807" alt="Executive Summary Page 1" src="https://github.com/user-attachments/assets/e7f858e4-9220-4cb8-a497-8440c4eb0cc7" />

#### Key Metrics:
- **Total Sales**: $118.73M  
- **Total Profit**: $16.89M  
- **Profit Margin %**: 14.23%  
- **Units Sold**: 1.13M

#### Insights:
- **Quarter-wise Profit Trend**: Profit increased from Q1 (13.51%) to Q4 (14.56%)
- **Customer Segment Breakdown**: Government segment contributed ~$11M in profit, Small Business around $4M
- **Monthly Trend Analysis**: Seasonality observed with peaks in Q4 sales
- **Product & Segment Table**: 
  - Top product: *Montana*, *Carretera*, *Velo*
  - Segment with highest margin: *Midmarket* (up to 73%)

---

### 🔹 Executive Summary - Page 2  
<img width="1447" height="803" alt="Executive Summary Page 2" src="https://github.com/user-attachments/assets/d7ee056a-c6e8-4ad7-828b-7689c1f9617f" />


#### Key Metrics:
- **Sales YTD**: $92.31M  
- **Sales MTD**: $12.00M  
- **Sales PY**: $26.42M  
- **Sales Growth %**: 349.46%

#### Insights:
- **Quarterly Performance**: Sales increased steadily from Q1 ($19M) to Q4 ($92M)
- **Profit by Product Segment**: *Paseo*, *VTT*, and *Amarilla* lead in profitability
- **Time-Based Sales Report**: Q4 saw a dramatic surge in sales—crucial for holiday marketing strategy
- **Monthly Profit Growth**: Steady increase, peaking in December

---

## 📌 6. Recommendations  
1. **Double down on Government and Midmarket segments** – consistently high profit margins.
2. **Optimize Q4 campaigns** – proven seasonal growth.
3. **Promote top-performing products** like *Paseo* and *Montana*.
4. **Adjust discounting strategies** to avoid margin erosion in Enterprise segment.
5. **Monitor product-return patterns** to improve margin and customer satisfaction.

---

## 🧪 7. Tools Used  
- **Power BI Desktop**
- **DAX (Data Analysis Expressions)**
- **Power Query (ETL Transformations)**
- **Star Schema Modeling**

---
