# CryptoClustering

This repository examines the unsupervised learning methods, K-means and PCA to analyze crypto currency data to better predict 24 hour and 7 day price fluxuations.

You can find all the code in (Crypto_Clustering.ipynb)[Crypto_Clustering.ipynb]

This notebook begins by reading in the data into a pandas dataframe. From here, we examine the data by graphing it into a line plot, illustrating the need for scaling. 

StandardScaler is used to fit_transform the data into a standard scale, from which a new dataframe is created. 

In order to decide the optimal cluster values, a line (elbow) graph is created with n_clusters ranging from 1-11 clusters. Where the inertia levels out is approximately 4 clusters, and this is selected as the optimum cluster value.

The KMeans algorithm is then used with the cluster value of 4 to make predictions of clustering, and the resulting datapoints are scatter-plotted within the notebook.

A Principal Component Analysis (PCA) is then run on the dataset with an n_components value of 3. The variance ratio is acquired as 89.5%, and the resultant values are used as a separate dataframe.

Like in section 1, an elbow graph is created to identify the optimum clusting for the data which, like in the initial example is identified as 4 clusters. 

A scatter plot is created using the PCA1 and PCA2 outputs, and the results are examined alonside the initial KMeans clustering. It becomes apparent from examining the two graphs side-by-side that PCA clustering makes it easier to identify outliers by more closely and distinctly clustering the data points. 