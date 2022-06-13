# Cryptocurrency Clusters

## Background

* One of the prominent investment bank, is interested in offering a new cryptocurrency investment portfolio for its customers. The company, however, is lost in the vast universe of cryptocurrencies. in this project, we were assigned to create a report that includes what cryptocurrencies are on the trading market and determine whether they can be grouped to create a classification system for this new investment.

### Data Preparation

* The dataset was obtained from [CryptoCompare](https://min-api.cryptocompare.com/data/all/coinlist).

* Data pre-processing was performed to fit the machine learning models.

* Unsupervised machine learning algorithm was used, since there is no known classification system. Several clustering algorithms were explored to determine whether the cryptocurrencies can be grouped together with other similar cryptocurrencies.

### Dimensionality Reduction

* Performed dimensionality reduction with PCA. Rather than specifying the number of principal components when the PCA model was instantiated , 90% of the **explained variance** was preserved for this project. 

* Further reduced the dataset dimensions with t-SNE and visually inspected the results. 

### Cluster Analysis with k-Means

* An elbow plot was created to identify the best number of clusters. A for-loop was used to determine the inertia for each `k` between 1 through 10. 

## Findings

* The number of features went down from 98 to 74, which is expected because using PCA(n_components=0.9) creates a model that will preserve approximately 90% of the explained variance.

![tsne_plot](https://user-images.githubusercontent.com/95401250/173304280-652269ee-9c02-4080-9d2c-5c8dc7b4aad3.png)

* From the scatter plot it looks like there could be 3-4 clusters and some random points which do not fit into any of the clusters.

![kmeans_elbowplot](https://user-images.githubusercontent.com/95401250/173304258-c34c6484-e729-4245-bd45-267d87de82e5.png)

The results of the generated curve signify that there is no distinct elbow ie. the curve does not flatten. No elbow does not mean that there are no clusters in the data; No elbow means that the algorithm used cannot separate the clusters; The further options are to tune the algorithm or use a different algorithm to cluster the cryptocurrency data or perform more data pre-processing.
