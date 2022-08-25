# Red Wine Quality Predictions
<center>
<img src="images/wineimage.png" width="700">                                       
</center>                                

# Objective
## Build a machine learning model to predict the quality of wines based on rating.

**Author**: 
Darlene Phan

### Business problem:

A global wine supplier is looking for a way to rate wines before determining if they should be acquired for their inventory.

### Data
- Source: 
    - https://www.kaggle.com/datasets/fedesoriano/spanish-wine-quality-dataset
#### Data Dictionary:
| Col Name           | Description                                                                                       |
| ------------------ | ------------------------------------------------------------------------------------------------- |
| winery             | Winery Name                                                                                       |
| wine               | Name of Wine                                                                                      |
| year               | Year in which the grapes were harvested                                                           |
| rating             | Average rating given to the wine by the users from 1-5                                            |
| num_reviews        | Number of users that reviewed the wine                                                            |
| country            | Country of origin (Spain)                                                                         |
| region             | Region of the wine                                                                                |
| price              | Price in Euros                                                                                    |
| type               | Wine variety                                                                                      |
| body               | Body score, defined as the richness and weight of the wine in your mouth from 1-5                 |
| acidity            | Acidity score, defined as wine's "pucker" or tartness; it's what makes a wine refreshing and your tongue salivate and want another sip. from 1-5                                 |


#### **Target:**
- Rating    
#### **Features:**
   - Winery
   - Wine
   - Year
   - Num Reviews
   - Region
   - Price
   - Type
   - Body
   - Acidity

## Methods
- Data was only imputed for visualizations.
- Both univariate and multivariate visualizations were used to determine outliers, distribution and patterns.
- Pipelines and column transformers were used to preprocess both the numerical and categorical data for the respective machine learning models.
- Machine Learning Models/Technique used:
    - Linear Regression
    - Principal Component Analysis (PCA)
    - Decision Trees (Regression Trees)
    - Ridge Regression
    - GridSearchCV
    - Feature Engineering
    
## Results

### Data Exploration Visualizations
<img src="images/outlet_type_hist.png">




> This histogram displays the of Sales Distribution by Outlet type. It allows us to visually compare the sales of the outlet types to the overall sales. 


<img src="images/item_sales_product_type.png">



> This bar chart clearly displays the lowest to highest sale items grouped by product type. This allows us to understand what makes up the majority of our sales and places a magnifying glass on the areas that do not perform as well. 


## Model

### Hypertuning Regression Tree
<img src="images/regression_tree.png">



> The final model is a regression tree. Tree based models have a tendency to overfit(high variance) to the training data. This will result in underfitting(high bias) on the testing data. Therefore, in order to create a model that will better predict on new data, we would have to tune the model. Essentially finding the sweet spot that has both a low variance and a low bias. 

> This visual is after automating the depth ranges of the regression tree model in order to find the most optimal depth. It exhibits that depth five will give us the best R^2 test result. We will be modifying the next regression model based on this result. 

## Evaluation:
<img src="images/metrics.png">

-   Once both Linear Regression and Regression Tree models were run, the metrics used to determine their accuracy and realtionship were Root Squared Mean Error (RMSE) and R-Squared (R^2)

-   Based on the regression metrics of both models, it's clear that once we addressed the overfitting issue on the Decision Tree training data, the model performed better by roughtly 45%.

-   The implementation of both these models suggest that with some tuning, the Regression Tree performed slightly better than the linear regression model. The R^2 on the Regression Tree suggests that 59% of the target can be realted back to our features data.

-   In conclusion, out of the two machine learning models created, the Regression Tree would be the more ideal choice in this scenario.

## Recommendations:

As a veteran of the Hospitality and Food Service industry, based on my experience, I would recommend an additional analysis on the business. In order to do this, it woul require more detailed data from the individual store to understand those key points. 

Since the R^2 score of both models sit below 59%, it tells us that less than 59% of the target predictions(sales) can be explained by our features matrix. 

## Limitations & Next Steps

-   Based on the dataset given, there are massive limitations to determine growth within the business. 
- These would be my next steps in terms of more data collection:
    -   Monthly or quarterly sales data
    -   Customer purchasing data (Customer averages)
    -   Locations of stores. City or suburb? Are they highly densely populated areas?
    -   Peek Hours of operations
    
-   Questions to consider when determining data collection:
    -   Who are my potential customers?
    -   Who are my competitors?       
    -   What are my lowest performing items? Why?
    -   What are my customers asking for?

In summary, there is a lot more we could explore here. A thing to note, just because two of the stores (Out 19 and Out 10) had lower sales, doesn't necessarily mean they performed poorly. If there was more data, it could potentially show that these stores are performing well. 

Maybe these two locations are not in highly populated areas but perform higher than the competition. They have less customers, smaller store and have higher customer sales average. 


### For further information


For any additional questions, please contact **thelemoncookie.data@gmail.com**
