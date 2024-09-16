# Introduction

Once you know who your end users will be, what is the goal of your dashboard and what will be the KPIs, you must actually build it.

The ETL consists of three consecutive steps, which can be simplified by using ELT (I will add the link to the repo when I finish my ELT project):

1. Connect to the data sources and **E**xtract the data
2. Prepare and **T**ransform it
3. **L**oad it in the target tool (usually a Data Warehouse or a Data Mart).

In this project I took advantage of Power Query, the ETL engine within Power BI.

ETL usually is **the most time-consuming step** of building a dashboard and it clearly was for this one.

**Do not underestimate the time it will take.**


# Table of Contents

1. [Extraction](https://github.com/danyishere/expenses-analysis?tab=readme-ov-file#getting-started](https://github.com/danyishere/expenses-analysis/edit/main/Markdown%20files/ETL.md#extraction))
2. [Transformation and the challenges faced]()
3. [Loading]()


# Extraction

## Getting the invoices

The invoices are sent to my personal email from E.LECLERC so I created a worfklow in Power Automate to automatically download the attached pdf file whenever I receive an email from nepasrepondre@l-information.com and store it in E.LECLERC/Factures in OneDrive.

## Getting the account statements

I tried to leverage the BNP API but did not manage to. I believe individual customers are not allowed to use it, for security reasons.

For now, this is a manual process of extracting my account statements as .xlsx files from the official BNP or HelloBank websites.

The statements are then stored in Banque/Relevés in OneDrive.

## Look Up

I manually add rows to my lookup table whenever I encounter unknown transaction labels.

This is the only way I've found to have a detailed view of my spendings (category, subcategory, subsub, detail...).

**Next step :**

So far, it works, but this is a tedious process which I must automate. As the lookup table grows, I may send it to a database to query it using SQL and build an user interface to easily alter it.

## Actually Extracting

The data is extracted using :
- the Web connector (with my Microsoft 365 credentials)
- the Folder connector to automatically extract the new invoices and statements as they are being added
