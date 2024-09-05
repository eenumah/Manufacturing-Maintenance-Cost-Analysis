# Business Case
This analysis examines the maintenance costs of a manufacturing company, with the objective of identifying key drivers of these expenses and proposing strategies for cost optimization. By analyzing historical data, and operational practices, we aim to gain insights into cost trends, inefficiencies, and potential areas for improvement. The findings from this analysis will inform recommendations to enhance asset reliability, and achieve a more efficient and cost-effective maintenance strategy. This will support the company’s long-term operational and financial objectives.



**_Disclaimer_**: _All datasets and reports do not represent any company, institution or country, the data have been highly annonymized and meant to showcase my understanding and experience in manufacturing, as well as competence in data analytics.._


The process flow in arriving at the insights includes:
- Exploring the different variables, datatypes and relationships contained in the dataset.
- Performing some transformation of the data from the source as data had no clear cut way of building relationships via primary or foreing keys
- Connecting the folders (To facilitate automation of data refreshes) containing the datasets to Power BI
- Building relationship between the different tables and writing DAX to generate extra information about the data.
- Further exploring the data to better understand and identify trends, patterns and abnormalies
- Summarizing these information into visualizations and reports of findings with recommendations.
---



# Modelling

![](Modelling.png)  
---
Sample DAX 1         | Sample DAX 2  
:-------------------:|:-----------------:
![](DAX1.png)       | ![](DAX3.png) 

![](DAX2.png) 
---
# Visualization
The report comprises of 4 pages:
- Homepage
- Overview
- Usage
- Price trend



## Homepage
Contains buttons at the top right to allow for easy navigation between report pages.
![](Home_page.png)

## Overview
A summary of major cost drivers, Inventory vs Purchase orders ratio and maintenance cost per ton trend against volume.
![](Overview.png)

## Usage
An analysis of consumables; exact spares, their volume of usage, the frequency of usage and the amount incurred
![](Usage_1.png)

## Price Trend
Analysis of how the unit price of spares have changed over time, with some spares rising way beyond what can be explained by only inflation.
![](Price_trend_1.png)
---



# Analysis
This analysis was done with flour production in mind, hence data and analysis have been tailored accordingly. However, this can apply to most manufacturing companies, especially food and beverage.

### Data Issues
Several issues were identified while exploring the data at the source, which includes;
1. Poor requisition process. For example, an item costing $1500 is requisited and later reversed, on requisition the data shows a value of -$1500 but after beign reversed it shows +$0 instead of +$1500
2. Same issue as above with quantity of spare requisited.
3. Lots of transactions made with improper description or no description at all making it difficult to trace what exactly that expense was for.

![](Transaction.png)

The table above shows transactions without a description displayed as "NA" amounting to $215k in FY22-23 alone ranking among top 10 transactions in cost.


### Maintenance Cost per Ton
The industry standard maintenance cost per ton in flour milling can vary significantly depending on several factors, including the location, scale of the operation, age and condition of the equipment, and specific processes used in the milling operation. However, some general benchmarks can be provided. Approximate maintenance cost for smaller mills range between $1 to $3 per ton of milled flour, while medium to large mills may have maintenance costs ranging from $0.5 to $1.5 per ton, benefiting from economies of scale and more advanced technology. For a typical, well-maintained flour milling operation, maintenance costs are often budgeted at around 1% to 3% of the total operating costs, with a specific target of $0.5 to $2 per ton of product being a common industry figure.

![](maintenance_cost_per_ton.png)

The chart shows a maintenance cost between $1 to $5 in the first fiscal year, $2.4 to $4.5 in the second fiscal year, and $4.5 to $6.9 in FY22-23. This is way above the industry average for medium to large scale operations.
Influencing factors includes geaographic location with high cost of importing spares and economic conditions like high inflation rate, age of equipment and maintenance strategies.

Also, the general downtrend in prodiction volume due to possible economic conditions and inflation leading to lower purchasing power of people and hence lower sales demands did not affect maintenance cost as its expected that both ought to be directly proportional.


### Customer Orders
Orders starts coming in as early as 1am ranging from 18-48 orders per hour between 1am and 4am. However, the busiest hours of the day is usually between 7am-11:30am where orders can peek at 158 per hour. On average, about 1,070 orders are placed across Maven Roaters three retail outlets daily.

![](Busiest.png)



The charts below is a reflection of average monthly orders. The right chart shows orders including the current year 2019 (only recorded 3 months) while the left chart excluded 2019. With 2019 included, there is a spike in revenue between march and april which was due to the 67% increase in sales revenue between 2018 and 2019 februaries.

With 2019                          | Without 2019
:----------------------------------|:---------------------------:
![](Average_monhly_ordered.png)    |    ![](without_2019.png)



Customers with highest orders are predominantly females with 22%, although a larger portion of customer orders at 67% did not specify gender. 
**Note that Top 4 customers are females.**

![](Top_customer.png)



# Recommendations
- If the dip in february is due to weather conditions at the beginnning of the year, then stock levels can be controlled to avoid holding excess inventory.
- An increased sales and profits can be recorded if more female appealing products and adverts are made.
- Encouraging customers to reveal gender can help with decisions on adverts and tailor made products appealing to specific gender.

---

# This was really fun for me, thank you for getting to the end!
