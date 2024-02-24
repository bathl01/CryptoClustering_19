# Crypto Clustering
### Module 19 Challenge
In this challenge, there is use of Python and unsupervised learning to predict if cryptocurrencies are affected by 24-hour or 7-day price changes. The .CSV data analyzed can be found in the resoources folder.

## Data Preparation:
  *  Load the data into a Pandas DataFrame
  *  Generate summary statistics and plot the data to see what is in the data
  *  normalize the data using 'StandardScaler()' module and put in in a Data frame with coin Id as the index
## Find the Best Value for k Using the Original Data:
  *  using k values 1 through 11 compute the inertia values
  *  create a data frame with the data and plot the elbow curve
  ### We found that based on the elbow curve, the best value for 'K' is 4 with the original scaled data.
## Cluster Cryptocurrencies with K-means Using the Original Data
  * clustered Cryptocurrencies with K-means Using the Original Scaled Data
  * plotted the cluster graph using hvPlot by setting the x-axis as 'price_change_percentage_24h' and the y-axis as 'price_change_percentage_7d'.
## Optimize Clusters with Principal Component Analysis (PCA)
  * the PCA Model was used to reduce the original scaled dataFrame, to 3 principal components.
  * the data was put into a data frame
  ### Total Explained Variance = the sum of the 3 Explained Variance Ratios 0.34871677, 0.31363391, 0.22627118 = 0.8886218549859446
## Find the Best Value for k Using the PCA Data
  *  using k values 1 through 11 compute the inertia values
  *  create a data frame with the PCA data and plot the elbow curve
  ### We found that based on the elbow curve, the best value for 'K' is 4 with the PCA data.  This is the same 'k' value as found using the original data
## Cluster Cryptocurrencies with K-means Using the PCA Data  

Does it differ from the best k value found using the original data?
Cluster Cryptocurrencies with K-means Using the PCA Data
Use the following steps to cluster the cryptocurrencies for the best value for k on the PCA data:

### Initialize the K-means model with the best value for k.
Fit the K-means model using the PCA data.
Predict the clusters to group the cryptocurrencies using the PCA data.
Create a copy of the DataFrame with the PCA data and add a new column to store the predicted clusters.
Create a scatter plot using hvPlot as follows:
Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".
Color the graph points with the labels found using K-means.
Add the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.
### Answer the following question:
What is the impact of using fewer features to cluster the data using K-Means?
