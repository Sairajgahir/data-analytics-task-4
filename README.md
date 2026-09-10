📊 Task 4 – Data Modeling, DAX & Executive BI Dashboard
📌 Project Overview
This project is part of my Data Analytics & Business Intelligence Task 4, focused on building a professional Power BI Business Intelligence solution using data modeling, DAX calculations, time intelligence, and executive-level dashboard design.
The main objective of this task was to transform structured sales data into meaningful business insights that can support strategic decision-making.
🎯 Objectives
Build a proper Star Schema data model
Create relationships between Orders, Customers, and Products
Develop calculated DAX measures
Perform time intelligence analysis
Analyze sales growth and profitability
Create an interactive executive dashboard
Present important business insights through data storytelling
🗂️ Dataset Structure
Fact Table – Orders
Order_ID
Order_Date
Customer_ID
Product_ID
Sales
Profit
Quantity
Dimension Table – Customers
Customer_ID
Customer_Name
Region
Segment
Dimension Table – Products
Product_ID
Category
Sub_Category
Calendar Table
A separate Calendar table was created to perform time-based analysis.
🔗 Data Modeling
The following relationships were created:
Customers
    │
    │ Customer_ID
    ▼
Orders
    │
    │ Product_ID
    ▼
Products

Calendar
    │
    │ Date
    ▼
Orders
The model follows a Star Schema, where Orders acts as the fact table and Customers, Products, and Calendar act as dimension tables.
🧮 DAX Measures
Some of the important measures created are:
Total Sales = SUM(Orders[Sales])
Total Profit = SUM(Orders[Profit])
Profit Margin = DIVIDE([Total Profit], [Total Sales])
Previous Month Sales =
CALCULATE(
    [Total Sales],
    PREVIOUSMONTH(Calendar[Date])
)
Growth % =
DIVIDE(
    [Total Sales] - [Previous Month Sales],
    [Previous Month Sales]
)
Category Contribution % =
DIVIDE(
    [Total Sales],
    CALCULATE(
        [Total Sales],
        ALL(Products[Category])
    )
)
📈 Dashboard
The executive dashboard contains:
KPI Cards
Total Sales
Total Profit
Profit Margin
Growth %
Total Orders
Visualizations
📈 Monthly Sales Trend
📊 Sales by Region
📊 Profit by Category
👥 Top 10 Customers
🍩 Customer Segment Distribution
Interactive Filters
Year
Month
Region
Category
Segment
💡 Business Insights
The dashboard can be used to identify:
Whether the business is growing consistently
Which region generates the highest revenue
Which category provides the highest profit margin
Seasonal sales trends
The most valuable customer segment
Customers contributing significantly to overall sales
Areas where management should focus for future growth
🛠️ Tools & Technologies
Power BI
DAX
Power Query
Data Modeling
Microsoft Excel/CSV
Business Intelligence
📁 Project Deliverables
Task4_PowerBI.pbix – Power BI project file
Data_Model.png – Data model screenshot
Dashboard.png – Executive dashboard screenshot
DAX_Measures.txt – List of DAX calculations
Executive_Business_Report.pdf – Business insights report
🚀 Learning Outcomes
Through this project, I strengthened my skills in:
Data modeling and relationships
Star schema design
DAX calculations
Time intelligence
KPI development
Interactive dashboard creation
Business intelligence
Executive-level data storytelling
👨‍💻 Conclusion
This project helped me understand how raw business data can be transformed into an interactive Business Intelligence solution. By combining data modeling, DAX, time-based analysis, and dashboard design, I developed a more practical understanding of how data analysts and BI developers use data to support business decisions.
#PowerBI #DataAnalytics #BusinessIntelligence #DAX #DataModeling #Dashboard #DataAnalyst #Analytics #GitHub #LearningJourney
