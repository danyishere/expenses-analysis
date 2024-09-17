# Dashboard Design

[Go back to Data Modeling](data_modeling.md)

This is the easiest part.

# The Method and its application 

- **Define your audience**: Data Analyst, technical background
- **Determine whether you should leverage accessibility features**: I'm a tech guy, pretty young (I guess), no vision impairment, no dyslexia --> NO
- **Clarify the objective of your dashboard**:
    - Identify spendings categories, need for budget increase/shift, potential flaws (i.e. irregular patterns, missing payments, negative cashflow, ...)
    - Reveal inflation
- **Choose colors**:

| Element | Color | Why ? |
| ---| --- | --- |
| Background | white and grey | low saturation (will not draw attention) |
| Text, Icons  | black and dark grey  | high contrast with background for visibility |
| Numbers | grey gradient, red and green | varying contrast (value importance in a distribution) , highly saturated colors (important values such as KPIs, rising and falling values) |

- **Choose visuals**:
    - Distribution: horizontal bar charts
    - Time serie : bar charts (or line chart)
    - Time comparison (single variable) : line chart
    - Static composition : treemap
    - Detail : classic grid


# Optimization

Once you've applied the general method, it's just a matter of playing with the options of each graph to optimize its readability and facilitate the understanding of the underlying data :
- optimize contrast
- highlight important values, outliers
- highlight contribution with Pareto lines
- add trend lines, moving averages
- add clear titles, legends
- display general data context (year, categories...) or filter context
- hide the mess or the useless
- 🗒️ Don't forget : the less the clearer
- Have fun with it ! 😀

# Next Step

[Go to Analysis and Results](analysis.md)
