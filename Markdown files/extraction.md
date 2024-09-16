# Extraction

[Go back to ETL](ETL.md)

## Getting the invoices 

The invoices are sent to my personal email from E.LECLERC so I created a worfklow in Power Automate to automatically download the attached pdf file whenever I receive an email from nepasrepondre@l-information.com and store it in E.LECLERC/Factures in OneDrive.

## Getting the account statements

I tried to leverage the BNP API but did not manage to 🤕. I believe individual customers are not allowed to use it, for security reasons.

For now, this is a manual process of extracting my account statements as .xlsx files from the official BNP or HelloBank websites.

The statements are then stored in Banque/Relevés in OneDrive.

## Look Up

I manually add rows to my lookup table whenever I encounter unknown transaction labels.

This is the only way I've found to have a detailed view of my spendings (category, subcategory, subsub, detail...).

🚧 **Next steps :**

So far, it works, but this is a tedious process which I must automate. As the lookup table grows, I may :
- send it to a database to query it using SQL 
- build an user interface to easily alter it

## Actually Extracting

The data is extracted using :
- the Web connector (with my Microsoft 365 credentials)
- the Folder connector to automatically extract the new invoices and statements as they are being added

# Next Step

[Go to Transformation](transformation.md)