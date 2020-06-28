# Cryptocurrencies
## Overview
Accountability Financial is considering offering a new Cryptocurrency portfolio and has requested help in identifying and grouping current Cryptocurrencies on the trading market. Due to the lack of known output for the data being processed, an unsupervised machine learning clustering algorithm was used to group currencies. 
In order to ensure optimal results were achieved, the data was first preprocessed using the following steps:

- Remove all cryptocurrencies that are not trading.
- Remove all cryptocurrencies that do not have an algorithm defined.
- Remove the redundant IsTrading dimension.
- Remove all cryptocurrencies with at least one null value.
- Remove all cryptocurrencies without coins mined.
- Store the names of all cryptocurrencies on a DataFrame named coins_name, using the crypto_df.index as the index.
- Remove the redundant CoinName dimension.
- Create boolean variables for all of the text features, and store the resulting data on a DataFrame named X.
- Scale the data using the StandardScaler from sklearn.

With the preprocessing complete, the dimensionality of the dataset was reduced to three dimensions using mathematical principles of linear transformations, eigenvalues, and eigenvectors, with the principal component analysis (PCA) algorithm. It was determined that the data should be grouped into four clusters by plotting the k-values (number of centroids or clusters) and corresponding inertia, onto a 2d plot and identifying the elbow curve. The KMeans model was then fit with the cluster value of four and plotted on 2d and 3d plots. The detailed technical analysis can be found in the notebook titled Cryptocurrencies_UML.ipynb.

## Resources
Data source: crypto_data.csv

Software: Python 3.7.6, Scikit-Learn 0.23.0, hvPlot 0.6.0, Plotly 4.8.1

Development Environment: Jupyter Lab 1.2.6
