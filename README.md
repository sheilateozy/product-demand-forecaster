# Forecasting Nestlé's product demand
## Using Random Forests with Recursive Feature Elimination

I interned as a Data Scientist at Nestlé USA.
<br><br>This is the project that I worked on, which increased demand prediction accuracy by 9.4% from existing models, translating into cost savings of $3.4 million.
<li> SQL to query and manipulate big data on SAS.
<li> Designed, implemented, and back-tested optimal models using custom scoring metrics.
<li> Feature selection using Recursive Feature Elimination.
<li> Data visualisation dashboarding on Microsoft Power BI to depict business impact of new models.

# About
My work involved improving Nestlé's existing demand forecasting models through 3 aspects, as follows:

## 1. Feature selection tool: Recursive Feature Elimination
Nestlé collects an enormous amount of data, such as demand data, promotional data, holiday data, and competitor data. With this large amount of features available to be used for modelling, the team required a robust feature selection tool.

The first aspect of my project involved designing an end-to-end framework for feature selection (code and documentation). The goal was to (i) Increase model accuracy through technical feature selection methods instead of human intuition and domain expertise, and (ii) Increase model explainability to non-technical stakeholders within Nestlé.

I designed an approach that utilized Recursive Feature Elimination (RFE) through Permutation Feature Importance with Random Forests. This new approach improves on the current feature selection approach used by the team through the following aspects:

<center><img src="readme_images/feature_selection_tool.png" width="550"></center>

## 2. Feature selection at different levels
Next, I explored different levels in which to conduct feature selection. Feature selection can be conducted at 3 main levels:

<li><b>Business level:</b> The term “business” at Nestlé refers to a category of products that Nestlé sells, examples being the Baking business, the Beverage business, and so on. Under this method, one would conduct feature selection for an entire business of products, and use this same selected features to forecast demand for all products under that business.

<li><b>Product level:</b> Within any one business, there are hundreds of products. For example, two different products within Nestlé’s Baking business are pies and cakes. Conducting feature selection at the product level instead would mean selecting features to use for forecasting demand for each unique product, and using different features in modelling between different products within the same business.

<li><b>Product and store level:</b> Nestlé sells its products at thousands of stores around the world. Different products are sold at each store. Conducting feature selection at the product and store level entails using different features for each product-store pair.
<br>
<br>
<center><img src="readme_images/feature_selection_business.png" width="550"></center>
<center><img src="readme_images/feature_selection_product.png" width="550"></center>
<center><img src="readme_images/feature_selection_product-store.png" width="550"></center>

Among the 3 levels, I determine the optimal level at which feature selection should be conducted by back-testing across various time periods to find the level that results in the highest forecasting accuracy.

<h2>3. Benchmark suite of machine learning models:<br>Elastic Net, Random Forest, XGBoost, Deep Neural Network</h2>
The team had primarily been using traditional Statistics-based models such as ARIMA, ARIMAX, and other regression-based models for time-series demand forecasting. However, they were keen to branch out and adopt other machine learning-based models. Hence, I also worked on benchmarking models that had not yet been used by the team prior, using a custom scoring metric termed Demand Planning Accurcacy at Nestlé.

# Results: Making an impact at Nestlé
My work increased the accuracy of product demand forecasts by 9.4% on average across 6 categories of Nestlé products, with the exact breakdown as follows:

<center><img src="readme_images/accuracy_impact.png" width="550"></center>

This translates into cost savings of $3.4 million across the various categories:

<center><img src="readme_images/cost_savings.png" width="550"></center>

# Project Methodology
1. Feature engineering: Transform time-series problem into supervised learning problem
2. Encode categorical variables using Hash Encoding
3. Tune Random Forest using Random Search
4. Obtain unbiased permutation feature importances
5. Feature selection using Recursive Feature Elimination (RFE)
6. Train model on optimal subset of features
7. Repeat for various levels of forecasting to determine optimal level
8. Repeat for different models to determine optimal model

# Still curious?
Check out this project on my website <a href="_____">here</a> :)
  
