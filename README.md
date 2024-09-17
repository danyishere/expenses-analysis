# expenses-analysis
**Expenses and Budget analysis (ETL and dashboard in power BI)**

# Table of Contents

- [🎯 Goal](README.md#goal)
- [⚒️ Showcased Skills](README.md#showcased-skills)
- [🔌 Getting Started](README.md#getting-started)
- [📑 Documentation](README.md#documentation)


# Goal

## Budget

The main focus here is to understand, based on my account statements:
- how much I spend in each category
- how much I save and invest
- determine whether my budget allows me to clear a budget surplus or if I should increase/shift it towards another category
- identify the flaws in my budget (i.e. negative amount of cashflow, irregular saving patterns and amounts)

Overview :

<img src="/Images/pict_dashboard.png" width="900">

Deep dive :

<img src="/Images/pict_dashboard_deepdive.png" width="900">

## Consumption Habits

Grocery shopping is a massive area of expenditure, right ?

Knowing so, wouldn't it be interesting to be able to understand my (me and my family) consumption habits in even more details than just my account statements ?

Well, my local supermarket allows me to do just that by mailing me my invoices.

# ⚒️ Showcased Skills

## ETL
  - Extraction:
     - multi-sources extraction with Power Query
  - Transformation: 
    - M custom functions (conditional row filtering, text extraction, custom fuzzy-matching)
    - Python Regular Expressions
    - Non linear transformations
    - Robust programming (Try structures, Parameterization)
  - Loading:
    - Performance driven loading
## Data Modeling
- Relational model:
  - table, attributes, primary and foreign keys
  - Star schema
- DAX :
  - Advanced modeling
  - Time-Intelligence
## Data Visualization
- Color and Design
- Goal-oriented visuals
- User Experience

## Data Analysis
- Identifying KPIs and patterns
- Interpreting data and extracting insights
- Proposing solutions



# Getting Started

1. If you don't have it, **install Power BI Desktop**. You can download it from [the official Microsoft download page](https://www.microsoft.com/fr-fr/download/details.aspx?id=58494).
2. **Download the files** in the "Files" folder :
  - **"2022_altered.xls"** _(2022 account statement)_: this is a fake, altered version, since I obviously can't give you the real ones. If you have an account at BNP or Hello Bank, feel free to use your own account statements
  - **"Facture_altered.pdf"** _(invoice)_: this is a fake, altered version, since I obviously can't give you the real ones. If you do your groceries at E.LECLERC, feel free to use your own invoices
  - **"Dashboard_frame.pptx"** _(canvas background)_: I believe PowerPoint is easier and faster to use than Figma, even though Figma is really good. But the hassle isn't worth it IMO, unless you need a really fancy design.
  - **"Lookup.xls"** _(lookup table)_: this is the lookup table that categorizes your transactions. This is a light version of mine but feel free to use it as a starting point to create yours.
  - **"Budget_analysis.pbit"**: the real deal.
3. **Create these folders** wherever you like (but in the same folder):
  - Banque/Relevés
  - E.LECLERC/Factures
3. **Open the .pbit file**. You will be asked to modify the path parameters to root and to your documents (the folder you created the "Banque" and "E.LECLERC" folders in):
  - **Modify "root_path"** to your root (e.g. "C:\Users\yourbeautifulname\\")
  - **Modify "docs_path"** to your folder relative to root (e.g. "OneDrive\Documents\\")

Full path should now look like "C:\Users\yourbeautifulname\OneDrive\Documents\Banque...".

4. The .pbix file has been created. You're all set to explore. Enjoy 😁!

# Documentation

To have a better understanding of this analysis, I have documented its different steps :

- [ETL process](Markdown%20files/ETL.md#introduction)
- [Data Modeling](Markdown%20files/data_modeling.md#introduction)
- [Dashboard Design](Markdown%20files/dashboard_design.md#introduction)
- [Results and Synthesis](Markdown%20files/synthesis.md#synthesis)
