# Data Modeling

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
<br/>

<br>

# Main Details

## Building the Star Schema

The initial data sources could not be used as-is :
- No keys to create relationships (Look up table > account statements > invoices)
- Messy invoices data structure

Before :

After a few [transformations](transformation.md) 

