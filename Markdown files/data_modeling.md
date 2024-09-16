# Data Modeling

[Go back to ETL](ETL.md)

Creating a Power BI `Semantic Model` consists in:

- Creating the relationships between the tables
- Configuring tables and columns properties
- Creating custom columns, tables or measures using M or DAX to analyze data

## Advantages

- Optimizing performance and data quality
- Improving Data Management and facilitating data aggregation using hierarchies and relationships
- Facilitating insights derivation and complex analysis (e.g. predictive analysis)


## Good Practices

- Adopt a star or snowflake schema
- Leverage dataflows if available
- Abuse one-to-many relationships
- Many-to-many is evil
- Hide useless fields from final users
- Do not model your data before cleaning it

>**DO NOT Flatten your tables :**
>- This'll slow down performance
>- and you won't be able to leverage advanced Power BI capabilities (e.g. time intelligence, DAX functions)


# Main Details

## Building the Star Schema

The initial data sources could not be used as-is :
- No keys to create relationships (Look up table > account statements > invoices)
- Messy invoices data structure

Before :

<img src="/Images/semantic_model_before.png" width="900">


After a few [transformations](transformation.md), here is the `Semantic Model`, ready to be used for Analysis : 

<img src="/Images/semantic_model_after.png" width="900">

## DAX Measures

### Good Practices

- **Gather your measures in dedicated tables** to improve readability and maintenance
- **Create a dedicated time table** in DAX and use it as a Date table to leverage time intelligence functions
- **hide all explicit fields that you've replaced** by explicit measures

> **Always build explicit measures** rather than just using implicit ones (explicit fields) to leverage their flexibility.

### ⚒️ Applied functions
- `ALL` : delete all filter context
- `AVERAGEX` : compute budget surplus 30 days moving average
- `CALCULATE` : modify filter context
- `CALENDARAUTO` : in combination with MIN, MAX and YEAR to create a custom Date table
- `CONCATENATEX` : dynamically update dashboard title for All or selected months
- `DIVIDE` : 💁🏽‍♂️
- `FORMAT` : format date columns
- `IF` : conditionnally format reference and callout values
- `ISFILTERED` : in combination with IF and VALUES to dynamically update dashboard title for my different accounts
- `LEFT` : extract first characters
- `MAX/MIN` : retrieve max/min dates from Date table
- `SAMEPERIODLASTYEAR` : calculate previous year/month cash outflow
- `SUM`: 💁🏽‍♂️
- `VALUES`: create a table of selected values
- `YEAR`(`QUARTER`, `MONTH`, `WEEKDAY`, `DAY`) : 💁🏽‍♂️ 


# Next Step

[Go to Dashboard Designing](dashboard_design.md)
