# CryptoClustering
This project aims to cluster cryptocurrencies based on their price change percentages over different time periods. It utilizes K-Means clustering and Principal Component Analysis (PCA) to explore patterns in the data.

## Data Loading

- The data is loaded from the `crypto_market_data.csv` file, and the index is set to `coin_id`.
- The columns used include various price change percentages over different time periods, such as 24 hours, 7 days, 30 days, etc.
- The data is normalized using the `StandardScaler` from the scikit-learn library.

## K-Means Clustering

- Cryptocurrencies are clustered using K-Means to group them based on their price change patterns.
- The optimal number of clusters (k) is determined using the Elbow method. The elbow plot visually identifies the ideal value of k, which is 4 for this dataset.
- Clustering is performed on both the original scaled data and the PCA-reduced data.

## Principal Component Analysis (PCA)

- Objective: Reduce the dimensionality of the data while retaining most of the variance.
- PCA reduces the data into 3 principal components, which explain approximately 89.50% of the variance.
- The weights of each feature on the principal components are analyzed to understand which features contribute the most to each component.

## Visualization

- Scatter plots are generated to visualize clusters based on both the original data and the PCA-transformed data.
- The PCA-based scatter plot shows how cryptocurrencies are grouped in a lower-dimensional space.

## Project Workflow

### Data Loading and Preprocessing:

- Load `crypto_market_data.csv` and normalize the features using `StandardScaler`.

### Clustering using K-Means:

- Use the Elbow method to find the optimal number of clusters (k), which is 4.
- Predict clusters using the K-Means model and assign cryptocurrencies to clusters.

### Dimensionality Reduction with PCA:

- Apply PCA to reduce the dataset to 3 principal components.
- Predict clusters using PCA data and visualize the results using scatter plots.

### Feature Importance:

- Calculate the contributions of each original feature to the principal components to determine their importance in the PCA model.

## Results

- Best k-value: 4 (consistent across original and PCA-transformed data).
- Total Explained Variance by PCA: 89.5%.
- Cluster Visualization: Visualizations show distinct clusters for cryptocurrencies based on price change percentages.

## Usage

To run the analysis:

- Make sure the required dependencies are installed:
- Run the script to generate the clustering analysis and visualizations.



## References

- Classwork is referred a lot for this project.


