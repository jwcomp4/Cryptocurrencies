# Cryptocurrencies

## Overview of the Analysis

- This analysis uses unsupervised machine learning to classify and group cryptocurrencies to better understand the trading market and aid Advisory Services Team at Accountability Accountant as they investigate entering the cryptocurrency market.

- To accompish this analysis, the following processed was executed:
	- The data is first preprocessed to fit machine learning models.
	- Use pandas `get_dummies()` to encode text features.
	- Scale the data using `StandardScaler`
	- Use Principal Component Analysis (PCA) 
	- Cluster the cryptocurrency data using K-Means
	- Visualize the clustered data using a 3-D (`plotly.express`) scatter plot and a 2-D scatter plot and sortable table using `hvplot` 

## Results

### Preprocessing the Data

- To preprocess the data, I used Pandas to read in the data, filter the dataframe, drop null values, and drop unncessary columns. 
- This preprocessing resulted in the following dataframe:

![preprocess_data]()

- From there, I used `get_dummies()` to encode the text data and then scaled the data to prepare for Principal Component Analysis

### Principal Component Analysis (PCA)

- PCA is a statistical technique that speeds up machine learning algorithms by reducing the amount of input dimensions.

- Applying PCA to this dataset reduced the dimensions down to three and resulted in this dataframe that could be then used to find the K value:

![pca_dataframe]()

### Clustering

- To cluster the data, I used a for loop and to plot a range of k values onto an Elbow Curve. 

- This process resulted in a K value of 4:

![elbow_curve]()

- After determining the appropriate K value, I could then run the K-Means model, and create a dataframe that includes cryptocurrency data, the princple components, and the classes resulting from the K-Means model:

![clustered_df]()

### Visualizing

- This work then prepared the data for visualizing the clusters in the following ways.

- 3-D scatter plot using `plotly.express`

![plotly_scatter]()

- A sortable table using `hvplot`:

![hvplot_table]()

- A scatter plot using `hvplot`

![hvplot_scatter]()

## Summary

- This analysis helpfully clusters the vast possibilities of tradeable cryptocurrencies, which enables first-time investors begin to have a better sense of the model. 
- Future analysis with appropriate data could include performance and return on investment.


