# CryptoClustering
Crypto Clustering Project

1. Data Preprocessing and Normalization

The dataset from crypto_market_data.csv was successfully loaded into a Pandas DataFrame. Summary statistics and data visualization were conducted to understand the data distribution. Standardization was applied using the StandardScaler() module from scikit-learn to normalize the feature values. A new DataFrame with the scaled data was created while retaining the coin_id as the index.

2. Finding the Optimal k for Clustering

Using the elbow method on the scaled DataFrame:

A range of k-values (1 to 11) was tested.

Inertia values were computed and plotted.

The optimal k was determined based on the elbow point in the plot.

The best value for k was found to be 4, as indicated by the inflection point in the elbow curve.

3. K-Means Clustering on Scaled Data

The K-Means model was initialized with k=4.

The model was trained using the scaled DataFrame.

Cryptocurrencies were grouped into four clusters.

A scatter plot was generated using hvPlot, with:

price_change_percentage_24h on the x-axis.

price_change_percentage_7d on the y-axis.

Data points color-coded based on cluster labels.

The coin_id included in the hover information for identification.

4. Principal Component Analysis (PCA)

The dataset was transformed using PCA to reduce dimensionality to three principal components.

The explained variance was computed, revealing that the first three principal components accounted for 90% of the variance in the dataset.

A new PCA-transformed DataFrame was created with coin_id as the index.

5. Finding Optimal k Using PCA Data

The elbow method was applied to the PCA DataFrame.

The optimal k-value was found to be 4, which was consistent with the original scaled DataFrame.

6. K-Means Clustering on PCA Data

The K-Means model was re-trained using the PCA-transformed DataFrame with k=4.

Cryptocurrencies were grouped into four clusters based on PCA features.

A scatter plot was created using hvPlot, with:

PC1 on the x-axis.

PC2 on the y-axis.

Data points color-coded based on cluster labels.

The coin_id included in the hover information.

7. Impact of Using PCA for Clustering

Reducing features via PCA helped simplify the dataset while retaining most of the variance.

The clustering results remained largely consistent with the original scaled DataFrame.

PCA improved computational efficiency by reducing dimensions, making the clustering process faster.

However, interpretability of the principal components was lower compared to the original feature set.

Conclusion

The project successfully demonstrated the use of K-Means clustering to group cryptocurrencies based on price changes. PCA proved effective in optimizing clustering performance while maintaining meaningful cluster differentiation. The consistency of k-values between the original and PCA-transformed data suggests the robustness of the clustering approach. Future improvements could involve testing alternative clustering methods such as DBSCAN or hierarchical clustering for comparison.

