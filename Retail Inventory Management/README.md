### Inventory Management
![image](https://user-images.githubusercontent.com/13950516/162671469-439c2144-cb8a-41e2-ad26-a91c361cb248.png)

### <img src="https://user-images.githubusercontent.com/13950516/162672483-4d953e53-2d6b-49d6-81ba-e7daa4a54351.png" width="40" height="40" />  &nbsp; Problem Statement:


-  **Context**: A retail firm has many products in their inventory, and very few of them tend to sell (only about 10% sell each year) and many of the products only have a single sale in the course of a year

-  **Objective**: The sales and growth team of the retail firm wants to determine which products from their inventory should they retain to sell and the ones to discard

-  **Data**: The data given contains both historical sales data AND active inventory

-  **Goal**: We have a to building a binary classifier which gives us a list of product ID which need to retained in the inventory or list of products that need to be removed



### <img src="https://user-images.githubusercontent.com/13950516/162672846-869bf047-63a7-489f-9b33-4f4a3beab1b2.png" width="40" height="40" /> &nbsp; Dataset
The dataset contains a detailed set of products in an inventory and the main problem statement here is to determine the products that should continue to sell, and which products to remove from the inventory. The file contains the observations of both historical sales and active inventory data. The end solution here is to create a model that will predict which products to keep and which to remove from the inventory – we’ll perform EDA on this data to understand the data better.

We will analyze the dataset and take a closer look at its content. The aim here is to find details like the number of columns and other metadata which will help us to gauge size and other properties such as the range of values in the columns of the dataset.

### <img src="https://user-images.githubusercontent.com/13950516/162673345-5ea37d71-b9e4-47b7-aa6e-c43921d7b2d0.png" width="40" height="40" />&nbsp; Approach

- #### We will be using the historical dataset for the analysis and training the model
  - The dataset contains 198,917 rows and 14 columns with 12 numerical and 2 categorical columns. There are 122,921 actively sold products in the dataset, which is where we’ll focus our analysis.
- #### Univariate distribution plots
  - This section shows a frequency histogram for the selected variable along with the density and normal curves for the data

  - The box plot shows the basic statistics of the data like median, 25th and 75th quantiles and the outliers.

- #### Categorical Variable

  - Shows the frequency distribution of the difference factors

  - The data associated with each attribute includes a long list of values (both numeric and not), and having these values as a long series is not particularly useful yet – they don’t provide any standalone insight. In order to convert the raw data into information we can actually use, we need to summarize and then examine the variable’s distribution.

  - The univariate distribution plots are graphs where we plot the histograms along with the estimated probability density function over the data. It’s one of the simplest techniques where we consider a single variable and observe its spread and statical properties. The univariate analysis for numerical and categorical attributes are different.
 
  - For categorical columns we plot histograms, we use the value_count() and plot.bar() functions to draw a bar plot, which is commonly used for representing categorical data using rectangular bars with value counts of the categorical values. 
