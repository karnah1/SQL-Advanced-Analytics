# SQL-Advanced-Analytics
This Project moves beyond basic Queries to implement **Advanced Analytics** ( Window Functions, CTEs, And Data Modeling ) to solve real world business questions 

### 📋 Executive Summary: 
This project demonstrates a full-lifecycle **SQL analytics workflow**. Starting from a raw Data Warehouse, I progressed through Advanced Analytics techniques to solve real-world business problems. The final output is a pair of Strategic Reporting Views designed for executive-level decision-making.

* **Business Problem** : The raw data warehouse contains sales, product, and customer tables but provides no visibility into growth trends, customer loyalty tiers, or product performance benchmarks.
* **Solution** : Developed a modular SQL framework using Common Table Expressions (CTEs) and Window Functions to derive KPIs and segment data.
* **Steps** : Data Warehouse Initialization &#8594; Change Over Time &#8594; Cumulative Analysis &#8594; Performance Comparison &#8594; Part-to-Whole &#8594; Data Segmentation &#8594; Final Reporting.
* **Impact** : Successfully identified revenue concentration in the "Bikes" category and established a 360° view of customer spending behavior.

### 🏗️ Methodology & Roadmap
     >  Change Over Time Analysis
>> * Concept : Analyzing how metrics evolve over periods (Year/Month).
>> * Action : Aggregated Total Sales, Customer Count, and Quantity by Order Year and Order Month.
>> * Insight  : Identified seasonal peaks (December) and tracked historical revenue declines.
    
    >  Cumulative Analysis (Running Totals)
>> * Concept  : Measuring business progression.
>> * Action : Applied SUM() OVER(ORDER BY...) to calculate running totals of sales.
>> * Insight : Visualized how total revenue accumulates throughout the fiscal year.

    >  Performance Analysis (Benchmarking)
>> * Concept : Comparing current performance against a target.
>> * Action : Used LAG() to compare current year sales to the previous year and AVG() OVER() to compare products against the global average.
>> * Insight : Flagged products as "Above Average" or "Below Average" performers.

    > Part-to-Whole Analysis
>> * Concept : Proportion of a part relative to the whole.
>> * Action : Calculated the percentage of total sales contributed by each category.
>> * Insight : Discovered that Bikes dominate 69% of the revenue, highlighting a high-dependency risk.

     > Data Segmentation 
>> * Concept : Grouping data based on specific behavior ranges.
>> * Action : Used CASE WHEN to bucket customers into VIP (Long lifespan + High spend), Regular, and New segments.
>> * Insight : Quantified the size of the loyal customer base vs. the acquisition funnel.


### 🛠️ Technical Skills
* **Advanced SQL** : Window Functions (PARTITION BY, ORDER BY, ROWS BETWEEN), CTEs, Subqueries.
* **Data Transformation** : DATEDIFF for lifespan, DATETRUNC for granularity, CAST for percentage accuracy.
* **Reporting** : Creating Database Views to consolidate complex logic for BI tools.

### 📊 Results & Recommendations
* **Customer Health** : The "New" segment is the largest (14k+), suggesting a need for better conversion strategies to move them into "Regular" status.
* **Revenue Risk** : The business is over-reliant on the Bikes category. Recommendation: Diversify inventory in "Accessories" and "Clothing" to balance the portfolio.
* **Operational Efficiency** : Automated the Customer and Product reports into views, reducing manual query time for the BI team by 100%.

### 🚀 Next Steps
* **Visual Integration** : Connect the **gold.report_customers** view to Power BI for interactive RFM (Recency, Frequency, Monetary) dashboards.
* **Advanced Logic**: Incorporate product **"Subcategory"** analysis into the segmentation logic for more granular inventory control.
