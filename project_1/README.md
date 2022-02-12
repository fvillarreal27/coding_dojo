## **Project 1**

### **Food Sales Prediction**

This repository has the objective of processing data and implementing Machine Learning methods to predict the sale of food products that are sold in different stores.

### **Goals**

* Predict the sales of the establishments of the chain 'Coding Dojo XYZ'.
* Identify the main factors that explain the behavior and prediction of sales.

### **Considerations**

* Database that contains information regarding the sale of products in establishments of the 'Coding Dojo XYZ' chain.
  * 8,523 registers and 12 variables

* A data cleaning and mining process was carried out to address missing values, inconsistencies in the base, determine classifications, among others.

* The relationship between the variables was determined by descriptive statistics.

* Machine Learning models were estimated with the aim of being able to better predict sales, based on a set of explanatory variables and determining the estimate on a training and validation/test sample.
  * Test base size = 30%

### **Data Visualization**

**Distribution of sales by type of product**

<img src="https://drive.google.com/uc?export=view&id=1-N2Npng_tp-JqsVp7dPKehjPc2syjz_0" width="600">

There are a lot of observations regarding sales when considering fruits and vegetables or snacks. On the other hand, the type of product that registers the least amount of sales is seafood, although it is one of those that presents the highest levels in terms of median sales.

**Distribution of sales by establishment**

<p float="left">
  <img src="https://drive.google.com/uc?export=view&id=1PKx1OS3BWgRGGZSlqyuFZd9loFX1xx14" width="500" />
  <img src="https://drive.google.com/uc?export=view&id=1-2INvVs7fSz_AQIrkU7b-YmqYV61UdmJ" width="500" />
</p>

Grocery stores have, on average, a lower level of sales, in relation to supermarkets. In particular, it can be seen that the type 3 supermarket has, on average, a higher level of sales.

**Distribution of sales by location**

<p float="left">
  <img src="https://drive.google.com/uc?export=view&id=1vTXDEK3lLl_pEKJgsxJMidw-tQhWnusW" width="500" />
  <img src="https://drive.google.com/uc?export=view&id=1-MOEdQfzRxpkcpheXA2TYQO9EIn_SMKk" width="500" />
</p>

The graphs suggest that there is a greater accumulation of data to the left when considering establishments located in Tier 1.

**Correlation between variables**

<img src="https://drive.google.com/uc?export=view&id=1-EF70y8tEG_JH7ieiF3kQYXtPJZ_Hnxk" width="500" />

Sales correlates at 0.57 with the maximum retail price of the product. On the other hand, there is a weak, albeit negative, correlation with product visibility (-0.13).

### **Estimated models**

* **Linear regression**
  * With constant

* **Regression with KNN**
  * The optimal number of neighbors and the type of weight to be used were estimated.
  * Results: K = 6 and the inverse of the distance is used as weights

* **Decision Tree**
  * The optimum level of depth was estimated. Result: Depth = 5

* **Bagged Trees**
  * The optimal number of estimators was calculated. Result: Estimators = 170

* **Random Forest**
  * The optimal number of estimators was calculated. Result: Estimators = 200

### **Results**

The results regarding the coefficient of determination and the RMSE of each model are shown below:

<img src="https://drive.google.com/uc?export=view&id=134Eeuljl_a1BqpEi0QkrJYH4LOPPxV15" width="600" />

When considering the results of the coefficient of determination and the RMSE in both the training and test samples, it is recommended to use the **Random Forest** model.

The most important features (explanatory variables) in the Random Forest model are shown below:

<img src="https://drive.google.com/uc?export=view&id=1-Gb2jsiK-gU0RW2toMnb3-5gbcPm6bEc" width="500" />

* It can be seen that the maximum retail price of the product is the characteristic with the greatest weight, followed by the type of Outlet, particularly the Grocery Store, and the visibility of the product.
* In general terms, it can be seen that the type of outlet is important (grocery store or supermarkets), as well as the type of product.

**OLS Results**

In order to provide information regarding the relationships between the dependent variable and the characteristic/explanatory variables, the results of the linear regression coefficients using OLS are presented below.

<img src="https://drive.google.com/uc?export=view&id=1-Grs73nMnep9B25ADRxKAxsbZg4T_72I" width="500" />

### **Conclusions and recommendations**

Focus on the **type of establishment: Grocery stores vs Supermarkets**. Grocery stores are associated on average with a lower level of sales.

The results suggest that emphasis should be placed on **establishments located in Tier 2** when determining a higher level of sales. On the other hand, establishments located in Tier 1 have a lower level of sales on average.

Take into consideration the visibility of the products, as well as the establishment of competitive prices.

Seafood is the type of product that has the greatest positive relationship with sales.
