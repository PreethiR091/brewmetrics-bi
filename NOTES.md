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

