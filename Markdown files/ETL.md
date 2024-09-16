# ETL

[Go back to README.md](./README.md)

Once you know who your end users will be, what is the goal of your dashboard and what will be the KPIs, you must actually build it.

The ETL (Extract, Transform, Load) process consists of three consecutive steps, which can be simplified by using ELT _(I will add the link to the repo when I finish my ELT project)_:

1. Connect to the data sources and **E**xtract the data
2. Prepare and **T**ransform it
3. **L**oad it in the target tool (usually a Data Warehouse or a Data Mart).

In this project I took advantage of Power Query, the ETL engine within Power BI.

ETL usually is **the most time-consuming step** of building a dashboard and it clearly was for this one.

**Do not underestimate the time it will take.**


- [Go to Extraction]("/extraction.md")
- [Go to Transformation]("/transformation.md")
- [Go to Loading]("/loading.md")