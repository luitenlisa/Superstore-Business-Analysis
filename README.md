# Superstore-Business-Analysis 
Business case study for an unnamed superstore chain in the United States that sells direct to consumers, corporations, and home offices. 

## Executive Summary:
Problem:
<br/> This unnamed United States superstore chain needs to improve their profit margin. There is a significant amount of loss (18.7% of orders) that is inhibiting growth. It is imperative that this be identified and solved. There may also be excessive discounts being given in certain regions, which needs to be investigated, along with reduced sales/profit in certain regions (Central and Southern). 

Summary:
<br/>
- Profit declines sharply with discounts >20% in all regions and especially in the Consumer segment.
- Central and East regions have low sales and high loss rates with discounts.
- Tailored pricing strategies are recommended by region and segment.
- Increased marketing effors for Central to stimulate more purchasing.
- Implementation of a prediction model to flag orders that may cause a loss for a double inspection. 





## Table of Contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Tools](#tools)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Predictive Analysis](#predictive-analysis)
- [Recommendations](#recommendations)
- [Limitations](#limitations)

### Project Overview
In this project, I compiled some theoretical business questions to improve profitability for this superstore. The following questions were used as a guideline for this analysis:

Which factors contribute most to profit and loss on individual orders?

Are there customer or product segments where discounting is hurting more than helping?

Can we predict if an order is likely to be unprofitable?

How should marketing or pricing strategies differ by region?


### Data Sources
https://www.kaggle.com/datasets/vivek468/superstore-dataset-final

### Tools 
Python 
Jupyter Notebook

### Data Cleaning and Preparation
1. Data was loaded into Jupyter Notebook for analysis.
2. Data was explored and checked for inconsistencies (duplicates, typos, etc).
3. Data was formatted as necessary for various statistical analyses. Detailed in the attached Jupyter notebook: 
   

### Exploratory Data Analysis
This data set had 9994 records, with 21 variables observed. 

Starting with some broad exploration to understand the trends in sales and profits across the data. 


<img width="638" alt="Screenshot 2025-05-27 at 2 00 00 PM" src="https://github.com/user-attachments/assets/cbdfc338-4b09-4c95-a50d-151b2c846e8c" />
<br/> With a slight dip in 2015, there is an overall upward trend in sales.

<br/><img width="595" alt="Screenshot 2025-05-27 at 2 01 22 PM" src="https://github.com/user-attachments/assets/948f56cc-3651-49b8-9085-a724754435e2" />
<img width="593" alt="Screenshot 2025-05-27 at 2 01 48 PM" src="https://github.com/user-attachments/assets/8d6d12eb-a6dc-4a8f-85a2-7dbe964abb66" />

<br/> Sales and profit both peak in March, on average, over time. 

<br/><img width="546" alt="Screenshot 2025-05-27 at 2 03 08 PM" src="https://github.com/user-attachments/assets/31669bbc-a758-4a3d-9800-923c112745cf" />
<br/> Of the purchasers, consumers directly make up the majority of sales at 50.6% ($1.16M).
<br/>
<br/> From here, I started to look at the profitability and makeup of these orders to understand which products were bringing in the most money. 
<img width="618" alt="Screenshot 2025-05-27 at 2 09 07 PM" src="https://github.com/user-attachments/assets/9bbf1f26-e6cc-4976-8399-1fd8afb9c1da" />
<br/> Seeing that some products were causing a loss, I decided to see how many orders were leading to a loss compard to profit:
<br/> <img width="401" alt="Screenshot 2025-05-27 at 2 11 22 PM" src="https://github.com/user-attachments/assets/d38427e9-48a5-4ef0-866d-b097d80181d4" />
<br/> 18.7% of orders were resulting in loss, which is a significant amount of loss. 


<img width="599" alt="Screenshot 2025-05-27 at 2 13 11 PM" src="https://github.com/user-attachments/assets/c74787ff-f95f-4a38-8268-8045c80e6f50" />
<br/> Indicated in this chart, we can see that there are a large amount of discounts given to binders, machines, tables, and bookcases. However, bookcases and tables are the two products associated with the most loss in profit. It is worth investigating why there are so many discounts being applied to these items when they are not leading to any profit gain.  

<br/><br/>
### Predictive Analysis
Based on this exploration, it was imperative to identify any factors associated with loss and attempt to predict orders that were not profitable. In order to best predict this, both Logistic Regression and Naive Bayes were implemented in order to create a classification prediction system. 
<br/> Naive Bayes: 
<br/> <img width="438" alt="Screenshot 2025-05-27 at 2 23 05 PM" src="https://github.com/user-attachments/assets/e8a2eb04-bf99-4a74-aa92-07306b9cc7a5" />
<br/> This model yielded a 91% accuracy, but only a 60% recall. This means that Naive Bayes could correctly predict actual profitable and non-profitable purchases 90% of the time. However, when it came to recall, it was only at 60%. This means that out of all the orders that actually resulted in a loss, the model was able to correctly identify 60% of them as high-risk before they were fulfilled.


### Recommendations



### Limitations
 

### References


