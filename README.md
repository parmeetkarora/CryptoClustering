# CryptoClustering
In this challenge, we will apply unsupervised learning techniques using Python to explore if cryptocurrencies are influenced by 24-hour or 7-day price changes. The goal is to cluster cryptocurrencies and analyze patterns based on these changes.

Steps Overview:
Repository Setup:

Create a new repository called CryptoClustering on GitHub.
Clone the repository and push changes as you proceed.
Load and Inspect the Data:

Import the crypto_market_data.csv file into a DataFrame.
Explore the data by generating summary statistics and plotting the data to understand its characteristics.
Data Preprocessing:

Use StandardScaler from scikit-learn to normalize the data.
Create a scaled DataFrame with the normalized data, setting the "coin_id" as the index.
Determine Optimal k Value (Elbow Method):

Use the elbow method to find the optimal number of clusters (k).
Iterate k values from 1 to 11, compute inertia for each, and plot the results to identify the best value for k.
Record the optimal k value based on the elbow curve.
Clustering with K-Means:

Initialize the K-Means model using the optimal k value.
Fit the model and predict clusters for the scaled DataFrame.
Create a scatter plot using hvPlot, displaying clusters with axes as "price_change_percentage_24h" and "price_change_percentage_7d", and color-coded clusters. The cryptocurrency names should appear in hover details.
PCA for Dimensionality Reduction:

Apply Principal Component Analysis (PCA) to reduce the data to three principal components.
Compute the explained variance for each component and assess how much information is captured.
Create a new DataFrame with the PCA data, keeping the "coin_id" as the index.
Determine Optimal k Value with PCA:

Repeat the elbow method on the PCA-reduced data to find the optimal k value.
Compare this k value with the one found from the original scaled data.
Clustering with K-Means using PCA Data:

Cluster the cryptocurrencies using the PCA-reduced data and the best k value from the elbow method.
Create a scatter plot using hvPlot, setting "PC1" and "PC2" as axes, with color-coded clusters.
Analysis:

Evaluate how clustering changes when fewer features (using PCA) are used.
Analyze the impact on the clusters and interpret how dimensionality reduction influences the model.