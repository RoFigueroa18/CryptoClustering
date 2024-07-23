# CryptoClustering

Module 19 - Challengue

Cryptocurrency Clustering Analysis
This repository contains an in-depth analysis and clustering of cryptocurrencies using K-Means clustering and Principal Component Analysis (PCA). The primary objective is to identify the impact of 24-hour and 7-day price changes on the clustering of cryptocurrencies.

Libraries Used
pandas
hvplot.pandas
scikit-learn (StandardScaler, KMeans, PCA)

Analysis Steps:

1. Import Required Libraries
We imported essential libraries for data manipulation, visualization, and machine learning.

2. Load and Preprocess Data
Loaded cryptocurrency market data from a CSV file.
Displayed sample data and generated summary statistics.
Plotted initial data to visualize the DataFrame contents.

4. Prepare the Data
Normalized the data using StandardScaler from scikit-learn.
Created a DataFrame with the scaled data.
Set the coin_id column as the index.

5. Find the Best Value for k Using the Original Data
Implemented the elbow method algorithm to find the optimal value for k, testing values from 1 to 11.
Plotted a line chart of inertia values to visually identify the best value for k.
Determined that the optimal value for k is 4.

6. Cluster the Cryptocurrencies with K-Means Using the Original Data
Initialized the K-Means model with four clusters.
Fitted the K-Means model using the original data.
Predicted clusters and reviewed the resulting cluster values.
Created a copy of the original data and added a new column with predicted clusters.
Generated a scatter plot using hvPlot to visualize the clusters.

7. Optimize the Clusters with Principal Component Analysis (PCA)
Created a PCA model instance with n_components=3.
Reduced features to three principal components using the PCA model.
Reviewed the first five rows of the DataFrame with PCA data.
Retrieved the explained variance to determine the information attributed to each principal component.
Determined that the total explained variance of the three principal components is approximately 0.892.
Created a new DataFrame with the PCA data.

8. Find the Best Value for k Using the PCA Data
Applied the elbow method algorithm on the PCA data to find the best value for k.
Plotted a line chart of inertia values to visually identify the optimal value for k.
Found that the best value for k remains 4, consistent with the original data.

9. Cluster the Cryptocurrencies with K-Means Using the PCA Data
Initialized the K-Means model with four clusters using the best value for k.
Fitted the K-Means model using the PCA data.
Predicted clusters and reviewed the resulting cluster values.
Created a copy of the DataFrame with the PCA data and added a new column for predicted clusters.
Generated a scatter plot using hvPlot to visualize the clusters with PCA data.

10. Visualize and Compare the Results
Created composite plots to compare the elbow curves and cryptocurrency clusters from both the original and PCA data.
Analyzed the impact of using fewer features for clustering, concluding that PCA leads to clearer and more distinct clusters.
Files in the Repository
crypto_market_data.csv: CSV file containing the cryptocurrency market data.
Crypto_Clustering_starter_code.ipynb: Jupyter Notebook with the complete analysis and clustering steps.
README.md: This file, describing the analysis, steps taken, libraries used, and contents of the repository.
In this project, ChatGPT assisted with code functionality and optimization, as well as several key tasks in clustering analysis, including explaining the process of optimizing clusters with PCA and understanding the explained variance.

Reference
OpenAi. (n.d.). ChatGPT by OpenAi from https://openai.com/chatgpt
