# 🛍️ Product Analysis Dashboard

This Power BI dashboard was developed to analyze product performance, identify key sales trends, and support data-driven decision-making for product strategy and inventory planning.

## ⚙️ Tools Used

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
  - SQL Code in the folder [SQLCode](https://github.com/Angelo-77/ProductAnalysis/blob/4f16eaff580793891e8fcf898b310ce9a3d3db7b/SQLCode)
 
> 📸 FactSales Diagram and View:
  - ![Image](https://github.com/user-attachments/assets/f6f3175a-50ff-4b67-8151-5d46bc0b930e)
  - ![Image](https://github.com/user-attachments/assets/51b5bc65-1e68-4f15-b90f-be633ea9e578)

> 📸 DimCalendar as procedure:
  - ![Image](https://github.com/user-attachments/assets/f3294313-1ef7-4ce3-98d9-6e695b3c9d18)
> Dim Calendar code in the folder [DimCalendar_Procedure](https://github.com/Angelo-77/ProductAnalysis/blob/4f16eaff580793891e8fcf898b310ce9a3d3db7b/DimCalendar_Procedure)

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

> 📸 Folder Display:
  - ![Image](https://github.com/user-attachments/assets/4e7e5c3c-3e31-4629-b20d-2141b497ab65)

> 🏹 To see these measures in dax syntax - click in this folder ['DaxMeasures'](https://github.com/Angelo-77/ProductAnalysis/blob/4f16eaff580793891e8fcf898b310ce9a3d3db7b/DaxMeasures)
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
    
> 📸 Figma Display:
  - ![Image](https://github.com/user-attachments/assets/c64c561a-9a62-4e2e-9a32-a1426e35f02f)


---

### 5. 📈 Dashboard Pages
  - All pages have 5 filters: Year, Month, Seller, Territory, Continent

- **General**  
  KPIs, Revenue, Gross Margin, Growth %, Highlights, Manager, Category and Region View
  
> 📸 General Page:
![Image](https://github.com/user-attachments/assets/5ef84557-67db-488d-a29f-153268560448)

- **Analytical**  
  Full Continent decomposition: Gross Revenue, $ Gross Margin, % Gross Margin, QtySold, Product Positivation, % Product Positivation, Coverage, %Coverage

> 📸 Analytical Page:
![Image](https://github.com/user-attachments/assets/664edc29-4b8a-4023-b6b3-18d0db0aac64)
   
- **HeatMap**  
  Full decomposition: Gross Revenue and Running Totals (distribuited daily and weekly)

> 📸 HeatMap Page:
![Image](https://github.com/user-attachments/assets/7f3dc2cd-1c6f-4f86-992c-e13e6a9e2cdd)
  
- **Sellers**  
  Full decomposition: Gross Revenue, $ Gross Margin, % Gross Margin vs goal open by sellers

> 📸 Sellers Page:
![Image](https://github.com/user-attachments/assets/35f5d973-4016-4a3a-8c4b-091f8cdc5c46)
  
- **PVM Analysis**  
  Full decomposition: Price, Volume, Mix – Sales & Margin Impact
  
> 📸 PVM Page:
![Image](https://github.com/user-attachments/assets/4fb108a2-8abf-4924-bce2-84cb032e0314)
  
- **Pareto Contribution**  
  Pareto 80/20 charts, Category share, Market movement
  
> 📸 Pareto Page:
![Image](https://github.com/user-attachments/assets/38e210d9-65de-4ab6-8c62-cee1f28a8966)

- **Statistical Insights**  
  Elasticity Index, Z-Score, Mean, Median, Std Dev, Moving AVG

> 📸 Statistical Page:
![Image](https://github.com/user-attachments/assets/6ebb0a72-c201-4b34-bb1f-280ca30ff51e)

  
 ✅ Outcomes and future strategies

## 📊 Business Analysis Summary — FY2014
🚨 Revenue Performance Breakdown
In FY2014, the company faced a global revenue decline of 54%, impacting all major regions:

**🔻Region	Revenue Decrease**

  - North America	–59%
  - Europe	–47%
  - Pacific	–35%
  - The Components category saw a 62.5% drop in sales.
  - Clothing sales declined by 39%, indicating category pressure.
  - Insight: These figures highlight product-level weaknesses and regional performance gaps, especially for discretionary or seasonal categories.

**🏆 MVP Product Alert: Mountain Bikes**

  - In the Northeast, Mountain Bike sales fell by 83%.
  - As our Most Valuable Product (MVP), this represents a critical commercial concern.
  - **Action Needed**: Regional campaign boosts, product repackaging, and customer reactivation efforts.
    
**⚠ Cost Management Cushion**
  - Despite revenue loss, Gross Margin improved due to:
  - 58% reduction in overall costs, outpacing revenue decline.
  - This cost agility helped protect margins, reflecting operational resilience.
  
## 📐 PVM (Price, Volume, Mix) Analysis

  - PVM Driver	Margin Impact
  - Volume	– €2M
  - Price / Mix	Balanced / Stable
  - The largest driver of margin decline was customer churn — clients who stopped buying entirely.
  - Recommendation: Launch retention & re-engagement campaigns using churn probability models.

## 📦 ABC & Pareto – Revenue Concentration Risk
  - Just 2 products generate ~60% of Global Revenue.
  - This creates over-reliance on specific SKUs (e.g., Mountain Bikes, Touring Bikes).
  -  Risk Alert: Any downturn in these can severely impact overall performance.

## 🧮 Statistical Outlier Analysis (Z-Score)
  - Average Z-Score across 27 subcategories: –0.33
  - Top 3 products Z-Scores: 3.11, 3.08, 2.80
  - These values confirm that a few categories dominate the business — a classic right-skewed outlier distribution.

## 🧠 Final Strategic Recommendations
✅ Diversify Revenue
→ Invest in mid-tier and low-performing segments to normalize contribution distribution.

✅ Prioritize Customer Retention
→ Reactivate high-value churned customers through CRM-driven marketing.

✅ Stabilize MVP Sales
→ Improve logistics, inventory, and vendor performance for flagship products.

✅ Expand Analytics
→ Leverage Z-score, price elasticity, and PVM trends in monthly performance reviews.



## 🔗 Dashboard Access  
📊[Dashboard](https://app.powerbi.com/view?r=eyJrIjoiOTA3YzlmM2MtNGRlOC00OWM2LWE3OGUtZmVjN2EwMzFlOTQ1IiwidCI6IjE0Y2JkNWE3LWVjOTQtNDZiYS1iMzE0LWNjMGZjOTcyYTE2MSIsImMiOjh9)


## 👤 About Me

I’m a results-driven **Data Analyst and Business Intelligence professional** with a strong foundation in **Power BI, SQL, Excel (including VBA), and KPI Management**. With experience spanning engineering, tax, and commercial sectors, I bring a unique blend of technical expertise and business strategy to every project I take on.

My career journey includes working at industry-leading companies like **Deloitte** and **Ambev**, where I automated processes, built dashboards, and translated complex data into meaningful insights. At **Deloitte**, I specialized in **Direct and Indirect Tax**, developing critical control workpapers and delivering the firm’s **first Power BI dashboard for Direct Taxes**. At **Ambev**, part of **AB InBev** (the world’s largest brewery), I created automated controls and VBA tools to evaluate sales and product performance.

Most recently, at **Draft Solutions**, an engineering consulting firm, I served as a **Senior Planning Analyst**. I managed engineering contracts, developed dashboards to monitor project KPIs, and designed macros for revenue forecasting and goal tracking. I also conducted **CAPEX calculations for Conceptual Engineering Projects**.

I hold a degree in **Accounting from PUC Minas**—recognized as the **largest Catholic university in the world**. While there, I received an academic award for developing a VBA tool to analyze the J150 block of the ECD, representing a company’s **Income Statement structure**.

I’m passionate about creating powerful BI solutions that improve decision-making, automate workflows, and drive measurable results.

**🔧 Technical Skills**:  
Power BI | SQL | Excel | VBA | ETL | Business Intelligence | KPI Development  

---

**📬 Let’s connect! - Feel free to reach out to me if you’d like to connect, collaborate, or discuss data!**
- 📧 angeloanalises@gmail.com  
- 💼 [LinkedIn](https://www.linkedin.com/in/miguel-angelo-015782198/)









