**FOOD SALES PREDICTION**

by Senait Abate




**Business problem:**

The goal of this project is to predict food sales for a retailer to understand properties of products and outlets that can  increase sales.

**Data:**

The data for this project was obtained from Anayltics Vidyha. The information obtained here consists of food items that were sold at various grocery stores and supermarkets from approximately 1985 to 2009. A range of food items and household products that were sold at each store was collected. The total sales of an item or product of a particular store was then inputed as item outlet sales.

Source: https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/#DiscussTab

**Methods:**

After the data was cleaned and reviewed for trends, it was preprocessed and a linear regression model and regression tree were performed and the ability of these models to predict future food sales was analyzed. The target vector for these models is "Item Outlet Sales," sales of a product in the particular store

**Results:**

In reviewing the total sales, there is a left-skewed distribution. This suggests that in creating a sales prediction model, the model will perform better when predicting the sales of items that cost less. Any outliers in this dataset will be from more expensive items and this would cause significant error in a predictive model. The positive distribution of total sales is further observed when reviewing the median and mean price in dolllars. The minimum value of item outlet sales is 33.29 and the maximum value is 13,086.96. The median price for item outlet sales is 1,794.33. The mean price is 2181.28. The mean is greater than the median price which suggests that more expensive items are driving the mean higher, affecting the distribution curve.

![image](https://user-images.githubusercontent.com/105686944/181138462-1345cb57-75ac-46f7-a0e8-476f8d4150ef.png)

Tier 3 supermarkets had the largest sales of all store types. The boxplots show that supermarkets in general sell much more than grocery stores.

![image](https://user-images.githubusercontent.com/105686944/181138508-f9233388-a45c-4ac6-adab-71315d3614d6.png)

Based on location type, Tier 1 stores performed the lowest in item sales versus Tier 2 and Tier 3 that are more competitive. Furthermore, there is a downward trend of sales for stores established 2004 and after. Further research needs to be done to examine what other factors may contribute to this decrease. 

![image](https://user-images.githubusercontent.com/105686944/181138580-fa9205aa-0f94-4daa-9c68-94a5e7b15cf2.png)


**Model:**

A linear regression and regression tree model was performed. The linear regression model is not ideal for this dataset as it contained very large errors. The RMSE for this model in dollars is 985.81 for the training set and 12563944732208.65 for the testing set. RMSE, root mean squared error is the square root of the mean. As it's a squared error, it assigns a higher weight to larger errors. The fact that the RMSE for this model is disproportionately high implies that there are larger value errors. In the initial regression tree model, the RMSE for this model in dollars is 2799.82 for the training set and 2673.58 for the testing set. The R2 values are 1.0 for the training set and 0.22 for the testing set. In other words, 22% variation can be explained by the model's inputs or features. 

However this low variance is also not ideal as it shows a low correlation between the actual values and the predictions made by the model. After tuning the regression tree model for the best fit, it's R2 value is 0.596, or about 60% variation at a max depth of 5. This model is still not the most indicative but it's features can explain more than half of the observed variation.

**Recommendations:**

Data visualizations: As there is a downward trajectory in sales for newer stores, established since 2004, more research should be done to examine if this is due to outside factors not realized within this dataset. For example, there is a social tendency to rely on longer established stores rather than new ones. 

Regression Models: Based on the model evaluations of the linear regression and regression tree models, I would recommend the regression tree model. The RMSE score is much higher on the test set of the linear regression model than it is on the regression tree model. The RMSE implies that there are larger value errors in the linear model. R2 of the testing set in the regression tree model is about .6. This shows that approximately more than half of the observed variation can be explained by the model's inputs.

**Limitations & Next Steps:**

The results for this project is greatly limited due to the small dataset that was used. A larger dataset would provide more accurate insight into sales predictions as it would decrease the amount of variable errors that can occur when dealing with a smaller sample size.

**For further information:**

For any additional questions, please contact **abate.senait@gmail.com**

