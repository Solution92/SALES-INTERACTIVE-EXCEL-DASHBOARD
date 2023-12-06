# SALES-INTERACTIVE-EXCEL-DASHBOARD

## Table of Content
- [Business Objective](#business-objective)
- [Data Source](#data-source)
- [Tools Used](#tools-used)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Data Analysis](#data-analysis)
- [The Dashboard](#the-dashboard)
- [Result and Findings](#result-and-findings)
- [Recommendation](#recommendation)
- [Limitations](#limitations)
- [Reference](#reference)


### Business Objective

To explore the Dataset and create an interactive dashboard to explain key Performance Indicators (KPI) such as Total Revenue and total Quantity and identify Yearly Accrued Revenue for the years involved, to identify the product or item that yielded the highest Revenue, Region that generated the highest Revenue.

Also, we want to know the salesperson who generated the highest Revenue in 2018 and 2019, the Top 10 Customers with the Highest Revenue, and the Customer with the Highest Quantity Purchase.

I will be doing Exploratory Data Analysis (EDA) for this dataset intending to increase revenue. It involves the initial analysis of the data to discover patterns and insights which typically include.

The main objective of every Operational business is primarily focused on increasing revenue alongside customer satisfaction. However, to achieve this, different data are collected daily because these data are needed for stakeholders' decision-making. Businesses don’t just make decisions without proper data analysis.

### Data Source

Quantum Analytics, during my internship training with them.

### Tools Used

Microsoft Excel - Data Cleaning, Transformation, analysis, and Creating Reports (Pivot Table).

### Data Cleaning and Preparation

Identifying and handling missing values, outliers, and errors in the dataset. Understanding the data was my first project.

![Screenshot_140](https://github.com/Solution92/SALES-INTERACTIVE-EXCEL-DASHBOARD/assets/144762124/f8a4ab2a-486d-4697-9665-045310c36efd)
The original file

The Dataset has 17 Columns with about 2,000 rows. Few of the Columns are Order ID, Date, Customer ID, Customer Name, Sales Person, Region, etc

![Screenshot_142](https://github.com/Solution92/SALES-INTERACTIVE-EXCEL-DASHBOARD/assets/144762124/89787f49-da50-4221-9fc6-e99ede8c54a0)
After the first transformation

The “Order ID” Column was pre-formatted as text instead of numbers. So, I had to clean it using the “CLEAN” function in a different Column. I created a different Column for “Year” and “Month” using the “TEXT” function.

Moreso, because I needed to analyze sales by different quarters I created another Column for “Quarter” using a “TEXT” function nested with “OR” and “IF” functions.

### Exploratory Data Analysis (EDA)

Here are a few KPIs and Insights created for this analysis:
- Sum of revenue
- Sum of Quantity
- Sum of Total revenue
- Revenue by item
- Revenue by Region
- Revenue by Year
- Revenue by Yearly Quarter
- Revenue by Sales Person
- Top 10 Customers by Revenue
- Customer by Quantity Purchased


### Data Analysis

I created another Column for “Quarter” using a “TEXT” function nested with “OR” and “IF” functions. Thus:

Quarter = IF(OR(TEXT([@Date], “mmm”)=”Jan”, TEXT([@Date], “mmm”)=”Feb”, TEXT([@Date], “mmm”)=”Mar”), “Q1”,

IF(OR(TEXT([@Date], “mmm”)=”Apr”, TEXT([@Date], “mmm”)=”May”, TEXT([@Date], “mmm”)=”Jun”), “Q2”,

IF(OR(TEXT([@Date], “mmm”)=”Jul”, TEXT([@Date], “mmm”)=”Aug”, TEXT([@Date], “mmm”)=”Sep”), “Q3”,

IF(OR(TEXT([@Date], “mmm”)=”Oct”, TEXT([@Date], “mmm”)=”Nov”, TEXT([@Date], “mmm”)=”Dec”),”Q4"))))

### The Dashboard

![Screenshot_141](https://github.com/Solution92/SALES-INTERACTIVE-EXCEL-DASHBOARD/assets/144762124/0941bbfc-eadf-4c5b-be81-d295f7ec8eca)

With different connecting slicers like “Quarter”, “Region”, and “Sakes’Person”, I was able to interact with the Visuals for a better result.

### Result and Findings

- Revenue Contribution by Sales Person, as seen on the Chart, Anna Weber and Laura Larsen Contributed almost equal Revenue followed by Ben Wallace. The Top 10 Customers, Company D, S, and M were the highest in revenue respectively while Company H, Q, and B, were the least contributors.
- On the other hand, the highest customer by Quantity Purchased happened to be Company D followed by B, which was among the lowest in Revenue Contribution.
- Texas contributed $532,135, to become the highest in the Region while Arizona is the least with $495,353. Moreover, the Business accrued more Revenue in 2019 with $1,158,151.
- Moreso, the first quarter recorded the highest Revenue with a value of $606,564 while the fourth quarter had $317,078. Item 1 happened to be the highest revenue contributor.

### Recommendation

My recommendation, however, 
- Based on the findings from the analysis, it is recommended to further investigate and understand the factors contributing to the similar revenue performance of salespersons Anna Weber and Laura Larsen. Identifying and leveraging the strategies employed by these individuals could potentially enhance overall sales performance. 
- Secondly, there should be a focus on optimizing the revenue from high-quantity customers like Company D, exploring opportunities to upsell or cross-sell to increase their contribution. 
- To boost revenue in lower-performing regions like Arizona, targeted marketing and sales initiatives may be implemented.
- Reward Sales Person with high Contributions with sales percentage and top customers should be given some insensitive to encourage their continuous Purchase.
- Finally, considering the success of Item 1 in revenue generation, a detailed analysis of its popularity and potential variations or bundles could lead to further revenue growth. 

### Limitations

- The dataset's relatively short time frame may restrict the ability to capture long-term trends or project future performance accurately. 

### Reference

Related datasets can be found on public websites like Kaggle













