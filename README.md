# Crypto_clustering
Module 19 Challenge

## Overview

In this project, I used Python and unsupervised learning techniques to predict the impact of 24-hour or 7-day price changes on cryptocurrencies. The journey involved loading and preprocessing the data, finding the optimal number of clusters (k), and clustering cryptocurrencies using both the original scaled data and reduced PCA data.

## Step-by-Step Progress

### Step 1: Data Preparation
To begin, I loaded the cryptocurrency market data from crypto_market_data.csv into a DataFrame. I gained insights into the data by obtaining summary statistics and creating visualizations. Using the StandardScaler() module from scikit-learn, I normalized the data and crafted a new DataFrame with the scaled data. Crucially, I set the "coin_id" as the index for the new DataFrame.

### Step 2: Finding the Best Value for k (Original Scaled Data)

To identify the optimal number of clusters (k), I applied the elbow method. This involved creating a list of k values from 1 to 11 and computing the inertia for each possible value of k. I then visualized the results using a line chart to pinpoint the elbow and determine the best k value.

### Step 3: Clustering Cryptocurrencies with K-means (Original Scaled Data)

Armed with the optimal k value, I initialized the K-means model, fitted it using the original scaled DataFrame, and predicted the clusters. I augmented the original data by adding a new column with the predicted clusters. To visually assess the clusters, I plotted a scatter plot using hvPlot.

### Step 4: Optimizing Clusters with Principal Component Analysis (PCA)

In this step, I performed Principal Component Analysis (PCA) on the original scaled DataFrame, reducing the features to three principal components. By retrieving the explained variance, I gauged the information content of each component. Subsequently, I created a new DataFrame with the PCA data and set "coin_id" as the index.

### Step 5: Finding the Best Value for k (PCA Data)

I continued the quest for the optimal k value, this time employing the elbow method on the PCA data. Similar to the previous step, I created a list of k values, computed the inertia, and visualized the results. The best k value was then identified and compared with the one obtained from the original data.

### Step 6: Clustering Cryptocurrencies with K-means (PCA Data)

Equipped with the optimal k value from PCA, I initialized a new K-means model, fitted it using the PCA data, and predicted the clusters. The PCA data DataFrame was extended by adding a new column to store the predicted clusters. To visualize the clusters, I created a scatter plot using hvPlot, this time focusing on the "price_change_percentage_24h" and "price_change_percentage_7d" axes.

### Step 7: Analysis

Finally, I addressed key questions:

I determined the total explained variance of the three principal components from the PCA analysis. I reflected on the impact of using fewer features for clustering data using K-Means. Conclusion The CryptoClustering project unfolded as a meticulous exploration of cryptocurrency data, employing K-means clustering and Principal Component Analysis. For a comprehensive walkthrough, refer to the Crypto_Clustering.ipynb notebook.
