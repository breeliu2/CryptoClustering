# CryptoClustering

In this task, you will apply your Python expertise and unsupervised learning to forecast whether cryptocurrencies are influenced by price fluctuations within a 24-hour or 7-day period.

# Data Preparation:

To normalize the data from the CSV file, utilize the StandardScaler() module available in scikit-learn.

Construct a new DataFrame containing the scaled data and designate the "coin_id" index from the original DataFrame as the index for this new DataFrame.

The initial five rows of the scaled DataFrame should display as follows:
![image](https://github.com/breeliu2/CryptoClustering/assets/124847109/f94c839b-19df-4c1b-943d-3b6470703985)

# Determining the Optimal Value for k Using the Original Scaled DataFrame:

To find the best value for k using the elbow method, follow these steps:

Formulate a list containing k values ranging from 1 to 11.
Initialize an empty list to store the inertia values.
Employ a for loop to calculate the inertia for each k value.
Build a dictionary with the data required to plot the elbow curve.
Visualize the inertia values computed for the different k values through a line chart to identify the optimal value for k.
Answer the following question in the Notebook: What value for k yields the best results?

# Clustering Cryptocurrencies with K-means Using the Original Scaled Data:

To cluster the cryptocurrencies with the optimal value for k on the original scaled data, follow these steps:

Initialize the K-means model with the best value for k.
Fit the K-means model using the original scaled DataFrame.
Predict the clusters to group the cryptocurrencies using the original scaled DataFrame.
Create a duplicate of the original data and append a new column with the predicted clusters.
Generate a scatter plot using hvPlot as follows:
Set the x-axis as "PC1" and the y-axis as "PC2".
Color the graph points based on the labels obtained from K-means.
Include the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

# Optimizing Clusters with Principal Component Analysis:

To optimize the clusters using the original scaled DataFrame, conduct a Principal Component Analysis (PCA) to reduce the features to three principal components.

Retrieve the explained variance to assess the amount of information attributed to each principal component. Address the following question in your notebook: What is the total explained variance of the three principal components?

Create a fresh DataFrame with the PCA data and designate the "coin_id" index from the original DataFrame as the index for this new DataFrame.

The initial five rows of the PCA DataFrame should display as follows:
![image](https://github.com/breeliu2/CryptoClustering/assets/124847109/72e61e8b-a01e-409a-8020-9d402f798af5)

# Determining the Best Value for k Using the PCA Data:

To find the optimal value for k using the elbow method on the PCA data, follow these steps:

Formulate a list containing k-values ranging from 1 to 11.
Initialize an empty list to store the inertia values.
Employ a for loop to calculate the inertia for each possible value of k.
Build a dictionary with the data required to plot the Elbow curve.
Visualize the inertia values computed for the different k-values through a line chart to identify the best value for k visually.
In your notebook, address the following questions:

What is the best value for k when using the PCA data?
Does this value differ from the best k-value found using the original data?

# Clustering Cryptocurrencies with K-means Using the PCA Data:

To cluster the cryptocurrencies for the optimal value of k on the PCA data, perform the following steps:

Initialize the K-means model with the best value for k.
Fit the K-means model using the PCA data.
Predict the clusters to group the cryptocurrencies using the PCA data.
Create a copy of the DataFrame with the PCA data and append a new column to store the predicted clusters.
Generate a scatter plot using hvPlot as follows:
Set the x-axis as "price_change_percentage_24h" and the y-axis as "price_change_percentage_7d".
Color the graph points based on the labels obtained from K-means.
Include the "coin_id" column in the hover_cols parameter to identify the cryptocurrency represented by each data point.

Answer the following question:
What is the impact of using fewer features to cluster the data using K-Means?


