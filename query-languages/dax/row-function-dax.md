---
title: "ROW Function (DAX) | Microsoft Docs"
ms.service: powerbi 

ms.date: 11/07/2018
ms.reviewer: owend
ms.topic: reference
author: minewiskan
ms.author: owend
manager: kfile
---
# ROW Function (DAX)
Returns a table with a single row containing values that result from the expressions given to each column.  
  
## Syntax  
  
```dax
ROW(<name>, <expression>[[,<name>, <expression>]…])  
```
  
#### Parameters  

|Term|Definition|  
|--------|--------------|  
|  name|  The name given to the column, enclosed in double quotes. |  
|  expression| Any DAX expression that returns a single scalar value to populate. *name*.  |

## Return value  
A single row table  
  
## Remarks  
Arguments must always come in pairs of *name* and *expression*.  
  
## Example  
The following example returns a single row table with the total sales for internet and resellers channels.  
  
```dax
ROW("Internet Total Sales (USD)", SUM(InternetSales_USD[SalesAmount_USD]),  
         "Resellers Total Sales (USD)", SUM(ResellerSales_USD[SalesAmount_USD]))  
```

The code is split in two lines for readability purposes  
  
