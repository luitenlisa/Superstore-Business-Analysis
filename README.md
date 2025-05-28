# Superstore-Business-Analysis 


## Executive Summary:
This project analyzes order-level sales data from an unnamed Superstore chainto identify the drivers of unprofitable orders. The goal is to recommend pricing and promotional strategies tailored by region and customer segment to improve profitability.

<b>Problem:</b>
<br/> 
- Significant amount of loss (18.7% of orders) that is inhibiting growth.
- Excessive discounts being given in certain regions causing reduced profit
- Lagging profit margins in certain regions.

<b>Key Questions:</b>
- Which factors contribute most to profit and loss?

- Where is discounting hurting more than helping?

- How should marketing and pricing strategies vary by region and segment?


<b>Findings:</b>
<br/>
1. Central and Southern regions are overly sensitive to discounts.
- Profitability drops sharply in Central and East at moderate discount levels, indicating the need for alternative promotional strategies.

2. Excessive Discounts lead to higher loss rates.
- There is a sharp decline in profitability once discounts exceed 20%.
- Negative profit margins and high loss rates after 20%.

3. Logistic regression for predicting orders associated with loss.
- Using a balanced logistic regression (71% recall and 93% accuracy) we can reduce loss by $97,584.

<b>Recommendations:</b>
1. Cap discounts at 15-20%.
2. Shift away from percentage based discount promotions in the South and Central. Implement new marketing strategy to stimulate increased spending (loyalty program, bundle discounts, free shipping, etc).
3. Implement predictive modeling to flag high-risk orders pre-fulfillment to reduce chances of loss. 

<br><br>
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
- Python 
- Jupyter Notebook

### Data Cleaning and Preparation
1. Data was loaded into Jupyter Notebook for analysis.
2. Data was explored and checked for inconsistencies (duplicates, typos, etc).
3. Data was formatted as necessary for various statistical analyses. Detailed in the attached Jupyter notebook: 
   

### Exploratory Data Analysis
This data set had 9994 records, with 21 variables observed. 

Starting with some broad exploration to understand the trends in sales and profits across the data. 


<img width="638" alt="Screenshot 2025-05-27 at 2 00 00 PM" src="https://github.com/user-attachments/assets/cbdfc338-4b09-4c95-a50d-151b2c846e8c" />
<br/> With a slight dip in 2015, there is an overall upward trend in sales.

<br/> 
<img width="618" alt="Screenshot 2025-05-27 at 2 09 07 PM" src="https://github.com/user-attachments/assets/9bbf1f26-e6cc-4976-8399-1fd8afb9c1da" />
<br/> Seeing that some products were causing a loss, I decided to see how many orders were leading to a loss compard to profit:
<br/> <img width="401" alt="Screenshot 2025-05-27 at 2 11 22 PM" src="https://github.com/user-attachments/assets/d38427e9-48a5-4ef0-866d-b097d80181d4" />
<br/> 18.7% of orders were resulting in loss, which is a significant amount of loss. It was also determined, by analyzing correlation, that there was a negative correlation between discounts and profit and discounts and sales. 


<img width="599" alt="Screenshot 2025-05-27 at 2 13 11 PM" src="https://github.com/user-attachments/assets/c74787ff-f95f-4a38-8268-8045c80e6f50" />
<br/> Indicated in this chart, we can see that there are a large amount of discounts given to binders, machines, tables, and bookcases. However, bookcases and tables are the two products associated with the most loss in profit. It is worth investigating why there are so many discounts being applied to these items when they are not leading to any profit gain.  

</br></br><img width="1076" alt="Screenshot 2025-05-27 at 7 51 04 PM" src="https://github.com/user-attachments/assets/be7862bb-7858-4f2a-92f0-62af3f3f7fc1" />
<br>
<br/><br/>The South is sensitive to high discount rates and sees a sharp decline in profitability after 20%. While the West also sees a sharp decline, 



### Predictive Analysis
Several predictive classification models were run, which can be detailed in the attached Jupyter notebook. The best model was a balanced Logistic Regression. It was decided to use a balanced model since "loss" made up less than 19% of the total orders, but was our main focus. 

Using the balanced logistic regression model, we are able to reduce loss by <b>$97,583.58.</b> The model was able to accurately predict 93% of the time. It was able to correctly identify non-profitable orders out of all non-profitable orders 71% of the time. 



| Model                   | Recall (Loss) | Accuracy | Estimated Losses Prevented |
|-------------------------|---------------|----------|-----------------------------|
| Logistic Regression (balanced) | **71%**       | **93%**   | **$97,584**                 |
| Naive Bayes             | 60%           | 90%      | $81,442                      |



### Recommendations
The first recommendation would be to cap discounts at the 15-20% range. It is evident that giving discounts exceeding 20% has a strong negative impact on profit, especially in the South. The South and Central regions are lagging in terms of profit, compared to the other regions. Central, in particular, had lots of orders but little profit. Thus, the next recommendation would be to tailor marketing efforts in these areas. It would be beneficial to reduce percent discount marketing efforts and transition to a bundle discount to increase basket revenue or a sort of loyalty program. It may also be beneficial to do a free shipping promo. Finally, it is advisable to implement a predictive model to help flag orders that are high-risk for loss prior to their fulfillment. This would allow the company to double check for any issues before fulfilling. This may also provide more data in the future as to what exactly is causing these high losses. 


### Limitations
 There is not a lot of information outside from this data set. It would be more informative to understand why such large discounts are being given. It would also be beneficial to understand if this superstore operates primarily through web orders or in-person shopping, as this could help steer marketing efforts better. It is unclear how many locations are apart of this chain and there is also not a lot of information on the customer base, outside of their name and segment. 


### References
https://www.kaggle.com/datasets/vivek468/superstore-dataset-final

