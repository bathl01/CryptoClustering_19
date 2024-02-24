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
  * clustered Cryptocurrencies with K-means Using the PCA Data
  * plotted the cluster graph using hvPlot by setting the x-axis as 'PCA1' and the y-axis as 'PCA2'.
## Visualize and Compare the Results
  * created combined Elbow Chart and combined cluster charts
  ### After visually analyzing the cluster analysis results, what is the impact of using fewer features to cluster the data using K-Means? The PCA Inertia is slightly lower than for the origional data.  However the changes did not affect the best value for 'k' which was 4 for both elbow curves.  The scatter plots both had out liers although in differemnt quadrents.  the PCA computations tightened up the pattern, but may have lead to over simplification and loss of information.

## Acknowledgements:
 * ChatGPT - getting rid of warningh message: "UserWarning: KMeans is known to have a memory leak on Windows with MKL, when there are less chunks than available threads. You can avoid it by setting the environment variable OMP_NUM_THREADS=1."  which required adding import os and os.environ['OMP_NUM_THREADS'] = '1', reinstalling "pip install hvplot", and using MiniBatchKMeans from from sklearn.cluster.
 * Stack Overflow - how to change the colors on the scatter plots so the groupings could be determined for the combined plot
