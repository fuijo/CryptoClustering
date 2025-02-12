# CryptoClustering
Crypto Clustering Project

![image](https://github.com/user-attachments/assets/1f4ee477-703c-4050-bb8c-feb2fa0462a6)


1. Data Preprocessing and Normalization

The dataset from crypto_market_data.csv was successfully loaded into a Pandas DataFrame. Summary statistics and data visualization were conducted to understand the data distribution. Standardization was applied using the StandardScaler() module from scikit-learn to normalize the feature values. A new DataFrame with the scaled data was created while retaining the coin_id as the index.

![image](https://github.com/user-attachments/assets/12670239-753b-415b-8631-3c86d6ba24e5)


2. Finding the Optimal k for Clustering

Using the elbow method on the scaled DataFrame:

A range of k-values (1 to 11) was tested.

Inertia values were computed and plotted.

The optimal k was determined based on the elbow point in the plot.

The best value for k was found to be 4, as indicated by the inflection point in the elbow curve.

![image](https://github.com/user-attachments/assets/397fd099-985b-4bdb-9739-616b6fcb6db6)


3. K-Means Clustering on Scaled Data

The K-Means model was initialized with k=4.

The model was trained using the scaled DataFrame.

Cryptocurrencies were grouped into four clusters.

![image](https://github.com/user-attachments/assets/57ee58d9-2bd1-4840-ab27-a845d0bd8d3e)


A scatter plot was generated using hvPlot, with:

price_change_percentage_24h on the x-axis.

price_change_percentage_7d on the y-axis.

Data points color-coded based on cluster labels.

The coin_id included in the hover information for identification.

![image](https://github.com/user-attachments/assets/b1bd0251-4458-4607-ad9a-e5abf5d42bea)

![image](https://github.com/user-attachments/assets/5416d183-48c2-4969-975d-23cf31a05d82)


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

![image](https://github.com/user-attachments/assets/28ef9481-10ff-4f53-8e4a-043bb2ee1262)


7. Impact of Using PCA for Clustering

Reducing features via PCA helped simplify the dataset while retaining most of the variance.

The clustering results remained largely consistent with the original scaled DataFrame.

PCA improved computational efficiency by reducing dimensions, making the clustering process faster.

However, interpretability of the principal components was lower compared to the original feature set.

![image](https://github.com/user-attachments/assets/780696b1-35d9-44fd-9606-c97044dcc0f4)


Conclusion

The project successfully demonstrated the use of K-Means clustering to group cryptocurrencies based on price changes. PCA proved effective in optimizing clustering performance while maintaining meaningful cluster differentiation. The consistency of k-values between the original and PCA-transformed data suggests the robustness of the clustering approach. Future improvements could involve testing alternative clustering methods such as DBSCAN or hierarchical clustering for comparison.

