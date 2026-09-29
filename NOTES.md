\# Copilot and DAX Notes



\## Measure 1: Month-over-Month Sales Growth



\### Copilot Attempt



I attempted to use Power BI Copilot to generate a DAX measure for month-over-month sales growth. Power BI requested a workspace that supports Copilot, but no compatible workspace was available in my current account. Therefore, Copilot did not generate a usable DAX suggestion.



\### DAX Used



```DAX

MoM Sales Growth % =

VAR CurrentSales = \[Total Sales]

VAR PreviousMonthSales =

&#x20;   CALCULATE(

&#x20;       \[Total Sales],

&#x20;       DATEADD(Dim\_Date\[date], -1, MONTH)

&#x20;   )

RETURN

&#x20;   DIVIDE(

&#x20;       CurrentSales - PreviousMonthSales,

&#x20;       PreviousMonthSales

&#x20;   )

```



\### Rework / Correction



Since Copilot could not generate a suggestion because of the workspace requirement, I created the measure manually. I used the existing Total Sales measure and DATEADD with the Dim\_Date date column to compare the current month with the previous month.



The measure was formatted as a percentage and tested using Month Name, Total Sales, and MoM Sales Growth %. The results showed 9.45% growth in May, -16.18% in June, and -13.01% in July.



\## Measure 2: Running Total Sales



\### Copilot Attempt



Power BI Copilot was not available because my current account did not have access to a compatible Copilot workspace. Therefore, no Copilot-generated DAX suggestion was available for this measure.



\### DAX Used



```DAX

Running Total Sales =

CALCULATE(

&#x20;   \[Total Sales],

&#x20;   FILTER(

&#x20;       ALL(Dim\_Date\[date]),

&#x20;       Dim\_Date\[date] <= MAX(Dim\_Date\[date])

&#x20;   )

)

```



\### Rework / Correction



I created the running total manually using CALCULATE, FILTER, ALL, and MAX. The measure removes the current date filter and includes all dates up to the current date, allowing sales to accumulate over time.



The measure was tested using Month Name, Total Sales, and Running Total Sales. The running total increased from April through July, and the final running total matched Total Sales.



\## Measure 3: Product Sales Rank



\### Copilot Attempt



Power BI Copilot was not available because my current account did not have access to a compatible Copilot workspace. Therefore, no Copilot-generated DAX suggestion was available for this measure.



\### DAX Used



```DAX

Product Sales Rank =

RANKX(

&#x20;   ALL(Dim\_Product\[item]),

&#x20;   \[Total Sales],

&#x20;   ,

&#x20;   DESC,

&#x20;   DENSE

)

```



\### Rework / Correction



I created the ranking measure manually using RANKX. The ALL function removes the current product filter so that each product can be compared with all other products. The ranking is based on Total Sales in descending order, with DENSE ranking used for tied values.



The measure was tested using the product item, Total Sales, and Product Sales Rank fields.



\## Measure 4: Cold Brew Sales



\### Copilot Attempt



Power BI Copilot was not available because my current account did not have access to a compatible Copilot workspace. Therefore, no Copilot-generated DAX suggestion was available for this measure.



\### DAX Used



```DAX

Cold Brew Sales =

CALCULATE(

&#x20;   \[Total Sales],

&#x20;   Dim\_Product\[item] = "Cold Brew"

)



Rework / Correction



I created this measure manually to specifically analyze Cold Brew sales. The CALCULATE function applies a filter to the item column so that Total Sales is calculated only for Cold Brew. This measure will be used in the dashboard to identify the monthly sales pattern of Cold Brew.

