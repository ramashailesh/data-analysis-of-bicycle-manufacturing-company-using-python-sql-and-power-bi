# Data Analysis of Bicycle Manufacturing Company Using Python, SQL and Power BI
 
## Overview

This project provides a comprehensive Production and Inventory Analysis of the Microsoft AdventureWorks Database. Adventure Works is a fictional bicycle manufacturing company, and this database contains standard transactions data from an Enterprise Resource Planning (ERP) System. It encompasses data from various company scenarios: Human Resources, Product Management, Manufacturing, Purchasing, Inventory, Sales, and Admin. 

This analysis focuses specifically on the Manufacturing and Inventory segments of the data. Microsoft Power BI was utilized to create an interactive dashboard, pulling data directly from SQL Server to provide actionable insights.

## Data Source

[Data Source](https://docs.microsoft.com/en-us/sql/samples/adventureworks-install-configure?view=sql-server-ver15&tabs=ssms)

## Data Model

Defining an effective data structure is critical for dashboard performance. This project incorporates a star schema model to ensure efficient design and faster data refresh rates. The image below illustrates the tables utilized in the model:

<img width="1024" alt="DataModel" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/DataModel.png">

### Tables used in the model:

- Production Location - Contains production assembly data (e.g., parts used to manufacture each product defined by assembly location category)
- Production Product - Data related to products, including physical details and pricing
- Production ProductCategory - Products and their defined categories
- Production ProductSubcategory - Products and their specific subcategories
- Production ProductInventory - Inventory data for produced products
- Production ScrapReason - Waste data related to manufacturing processes
- Production WorkOrder - Production transactions and related operational data
- Production WorkOrderRouting - Production work order scheduling details
- Sales SalesOrderDetail - Transactional Sales Data

## Built With

- Python
- Power BI
- SQL Server

## Analysis

### Main Page

The dashboard analyzes manufacturing and inventory operations through an app-like navigational interface. The main page serves as a hub leading to two primary areas: Production Overview and Inventory Overview. Each section breaks down specific details and KPIs on dedicated pages.

<img width="1024" alt="Main Page" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Main%20Page.png">

### Production Overview

<img width="1024" alt="Production Overview Page" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Production%20Overview%20Page.png">

The dashboard is structured according to fiscal year terms. A custom date table was created using DAX to automatically generate fiscal year segregations, assuming the fiscal year starts on October 1st and ends on September 30th.

This page provides a high-level manufacturing overview. Custom measures were developed in Power BI to establish specific KPIs. All charts and KPIs are described below:

<img width="1024" alt="Production Overview KPI" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Production%20Overview%20KPI.png">

### Charts on the page

* Cumulative Multiline chart: Shows production totals to help compare fiscal year production trends and identify manufacturing bottlenecks.

<img width="1024" alt="Cumulative Multiline chart" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Cumulative_Monthly_totals_by_fiscal_year.jpg">

* Donut Chart: Displays actual cost distribution across different parts of the assembly line. This helps determine which components drive costs and where improvements are needed to reduce production expenses.

<img width="1024" alt="Donut Chart" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Actual%20Cost%20of%20production%20by%20Assembly%20location.jpg">

* Waste cost by year line chart: A visualization showing the financial impact of discarded products and the associated trends over time.

<img width="1024" alt="Donut Chart" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Waste%20cost%20by%20the%20Year.jpg">

### Category Analysis

The Product Category Page allows for a more granular analysis to identify specific issues within the manufacturing system. This section consists of four charts providing in-depth analysis of production components.

<img width="1024" alt="Production Category Analysis" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Production%20Category%20Analysis.png">

**Pareto Charts**

The Pareto charts represent frequency or cost, with the most significant categories on the left. An overlapping line shows the cumulative percentage contribution. There are two Pareto charts on this page: one for components required to manufacture a bike and another for finished bike products.

<img width="1024" alt="Pareto Charts" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Pareto_Charts.jpg">

**Waste Cost - Product Matrix Visual**

This matrix visual identifies exactly where waste is costing the company money. The first column provides the reason for waste, while the subsequent columns categorize the costs into Bikes and Components. Conditional formatting highlights the most significant cost drivers.

<img width="1024" alt="Waste Cost" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Waste_Cost_Matrix.jpg">

**Bar chart**

A bar chart illustrating the volume of product categories produced on time.

<img width="1024" alt="Bar chart" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/On_time_production_by_category.jpg">

### Inventory Overview

The Inventory Overview analyzes stock levels and value. This analysis assumes a centralized location for the distribution supply chain.

**Main Page**

The overview includes three KPIs, three filters for data slicing, and two primary charts.

<img width="1024" alt="Inventory data overview" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Inventory%20data%20overview.png">

**KPIs**

<img width="1024" alt="Inventory data overview KPI" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Inventory%20Overview%20KPI.png">

**Area Charts**

These charts show inventory quantity and value by assembly location. They highlight which parts of the manufacturing process hold the most capital. Users can toggle between quantity and value views using the integrated button.

**Inventory Turnover Multiline chart**

Comparing inventory turnover across fiscal years reveals trends in inventory utilization, aiding in the planning of future production processes.

<img width="1024" alt="Inventory Turnover Multiline chart" src="https://raw.githubusercontent.com/ritik8801/Data-Analysis-of-Bicycle-Manufacturing-Company-Using-Python-SQL-and-PowerBI/main/Dashboard%20Screenshots%20and%20Features/Inventory_tunrover_chart.jpg">

## About the Developer

Dasari Ramashailesh is an Analytics Engineer with over 6 years of experience building analytics datasets, SQL pipelines, and data warehouse solutions. He specializes in SQL, data modeling, and ETL/ELT pipelines to support operational and financial analysis. By leveraging tools like Power BI and Tableau, he focuses on delivering reliable datasets and optimized queries that drive enterprise-level decision making.

## Contact

- Name: Dasari Ramashailesh
- Email: ramashaileshd@gmail.com
- LinkedIn: https://www.linkedin.com/in/ramashaileshd