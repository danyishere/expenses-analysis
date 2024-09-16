# Transformation

This clearly was the hardest and the most interesting part, besides deriving insights from the data.

# Heads Up

Before diving into what's been done, I would like to remind you a few things:

## Good practices

In descending order based on importance (according to me) :

- **Leverage M rather than DAX** as much as you can (new columns, switch cases, data types, ...) to improve performance (M is usually faster because it is processed before loading)
- **Disable auto-detection** of column types and headers

```
File > Options and settings > Options > Data Load > Type detection
```

- ⚠️ **Be careful when changing types**, this is the most common souce of error:
    - Try to change types once as the last step for all columns
    - Immediately affect a data type while creating new columns to avoid errors when you change its name
    - Error proof your change types step by using a Try structure
- **Rename all your steps** and use **only letters, numbers and underscores (no spaces)** to avoid the weird looking #"Column Name" step in the Advanced Editor
- **Leverage functions** for redundant operations
- **Leverage parameters for file paths** (or for anything else) to build robust queries
- **Group your queries** by creating distinct groups for parameters, helper queries, functions, to improve maintenance and readability
- **Add comments**
- **Add a description** to all your query groups, tables, columns and measures if necessary to allow other developpers and users to understand what you've done
<br/>
<br>

# Main transformations

## Functions

### "Transform file"

This function is the template transformation for all account statements in the "Banque/Relevés" folde

⚒️ **Applied skill sets** :
- Functions
- Filename proofing with Source{0}

### "Transform file (2)"

This function is the template transformation for all invoices from E.LECLERC. Those are semi-structured .pdf files that necessitate a lot of transformation to become clean and usable.

⚒️ **Applied skill sets** :
- Functions
- Filename proofing with Source{0}
- Non linear transformations in M
- Custom functions (conditional row filtering, custom text extraction) in M
- Testing and conditions in M (Try structure, if else structure)

### "func_filter_rows"

This function automatically filters the invoice total amount and is leveraged by the "Transformed file (2)" function

## Queries

### "Statements"

This query