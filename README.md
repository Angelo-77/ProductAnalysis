# 🛍️ Product Analysis Dashboard

This Power BI dashboard was developed to analyze product performance, identify key sales trends, and support data-driven decision-making for product strategy and inventory planning.

## 🧰 Tools Used

- SQL (Data extraction, Data modeling and transformation)
- Power BI (DAX and Visualization)
- Figma (Backgrounds and Design)


## 📊 Key KPIs and Insights

- 🔝 **Top-Selling Products**: Identify best-performing items by revenue and volume (ABC/Pareto).
- 📉 **Sales Trends**: Monthly/weekly views to understand performance over time.
- 💰 **Profitability Analysis**: Margin tracking per product category.
- 📍 **Regional Performance**: Compare product sales across locations.
- 📈 **Growth Metrics**: Analyze YoY and MoM growth per product.
- 💹 **Statistical KPIs**: Analyze outliers and distorcions 

## 🖼️ Dashboard Preview

> 📸 General Page:

![Image](https://github.com/user-attachments/assets/5ef84557-67db-488d-a29f-153268560448)

## 🧠 Business Impact

This dashboard enables managers to:

- Make informed pricing and stock decisions
- Identify underperforming products
- Allocate marketing efforts effectively
- Track category-level contribution to total revenue
- Evaluate PVM - Price, Volume, Mix changes
- Outlier behaviour

## 📂 Project Structure

### 1. 📂 Data Modeling with SQL
- Modeled **16 SQL views** to handle all business logic, joining, and enrichment.
- Views cover:
  - Sales (`vwFactSales`)
  - Inventory & Cost (`vwFactStock`, `vwFactProdCosts`)
  - Shipping, Discounts, Currency
  - Calendar (`vwdCalendar`)
  - Bridge tables (e.g. `vwDimStoreBridge`)
  - Dimensions (Product, Customer, Employee, Territory...)
 
> 📸 FactSales Diagram and View:
  - ![Image](https://github.com/user-attachments/assets/f6f3175a-50ff-4b67-8151-5d46bc0b930e)
  - ![Image](https://github.com/user-attachments/assets/51b5bc65-1e68-4f15-b90f-be633ea9e578)

> 📸 DimCalendar as procedure:
  - ![Image](https://github.com/user-attachments/assets/f3294313-1ef7-4ce3-98d9-6e695b3c9d18)

### 2. 🔗 Power BI Data Model
- Imported all views using **Import Mode** for performance.
- Created a **star schema** structure with:
  - Fact tables: Sales, Stock, Shipping, Costs, Exchange Rates
  - Dimension tables: Products, Stores, Calendar, Employees, Customers
- Managed complex hierarchies using **bridge tables** and custom keys.

---

### 3. 🧠 DAX Measures (Grouped in Folders)
All measures are organized into **logical folders** for clarity:

| 📁 Folder                | Description                                                                 |
|-------------------------|-----------------------------------------------------------------------------|
| General Measures         | Core metrics: Revenue, Costs, Qty, Discounts                               |
| Time Intelligence        | LY, YoY, MTD, QTD, Rolling Metrics, Moving Averages                        |
| Comparative              | Delta vs LY, % Differences, Growth Factors                                 |
| KPIs                     | Revenue/Cost per Unit, Margin %, Volume Growth                             |
| PVM (Price, Volume, Mix) | Breakdown of revenue/margin variation over time                            |
| Statistical Analysis     | Mean, Median, StdDev, Coef. of Variation, Elasticity Index, Z-Score        |
| Pareto Measures          | Top 20% product/customer contributions                                     |
| SVG & Icons              | Symbols for growth/decline/neutral cards                                   |
| Auxiliary Measures       | Formatting, flags, slicer sync, headers                                    |

---

### 4. 🎨 UI/UX Design with Figma
- Custom-designed layout using **primary colors**:
  - `#5D8C89` (Base)
  - `#25C9C1` (Accent)
- Visual identity aligned with analytics purpose: **clean, tech, and executive**.
- Responsive layout and custom visuals:
  - SVG-enhanced cards
  - Gradient and flat-designed backgrounds
  - Branded icon navigation

---

### 5. 📈 Dashboard Pages

- **Executive Summary**  
  KPIs, Revenue, Gross Margin, Growth %, Highlights

- **PVM Analysis**  
  Full decomposition: Price, Volume, Mix – Sales & Margin Impact

- **Statistical Insights**  
  Elasticity Index, Z-Score, Mean, Median, Std Dev, Moving AVG

- **Category Contribution**  
  Pareto 80/20 charts, Category share, Market movement

- **Seller Analysis**  
  Sales breakdown by Employee, Store, Territory

---

## ✅ Outcomes

This dashboard allows:
- Strategic decision-making for sales and marketing
- Analysis of trends, price sensitivity, and performance breakdown
- A **professional, modern layout** with deep statistical insights
- Executives to **track margin gains/losses by root cause**







