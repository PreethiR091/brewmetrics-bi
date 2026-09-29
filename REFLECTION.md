###### \# Project Reflection



This project helped me understand how a Business Intelligence solution can be developed incrementally using version control. Power BI was used to transform the BrewMetrics sales data into a star schema with Fact\_Sales and the Dim\_Date, Dim\_City, Dim\_Product, and Dim\_StoreFormat dimension tables. DAX measures were then added individually for month-over-month sales growth, running total sales, product sales ranking, and Cold Brew sales.



I attempted to use Power BI Copilot while creating the DAX measures, but Copilot required access to a compatible workspace that was not available in my current account. Therefore, the DAX measures were created manually and tested using the actual sales data. This required understanding functions such as CALCULATE, DATEADD, FILTER, ALL, MAX, and RANKX rather than directly accepting generated code.



The commit history changed my approach compared with a normal single-file lab. Instead of building everything at once, I developed the project in stages: initial setup, star schema, individual measures, and the final dashboard. Each stage was committed separately, making it easier to track changes and understand how the solution developed.



Overall, the project improved my understanding of Power BI data modeling, DAX, dashboard design, and Git-based version control.

