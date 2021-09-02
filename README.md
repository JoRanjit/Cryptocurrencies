# :dollar: Cryptocurrencies

## In this prject we are creating a report that includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for a Cryptocurrency investment portfolio.

### :white_check_mark: Deliverable 1: Preprocessing the Data for PCA.

#### First step is to create a dataframe with all tradable cryptocurrencies from the downloaded 'Cryptocompare/crypto_data.csv' file.
The cleaned-up dataframe looks like this:
![crypto_df]( https://github.com/JoRanjit/Cryptocurrencies/blob/main/Images/crypto_df1.PNG)

#### Next we used get_dummies functions to create variables for <i> Algorithm and ProofType </i> Features.
![get_dummies]( https://github.com/JoRanjit/Cryptocurrencies/blob/main/Images/get_dummies.PNG)

#### Then we used StandardScaler fit_transform() function to standardize the features from the X DataFrame.
![stdscaler]( https://github.com/JoRanjit/Cryptocurrencies/blob/main/Images/fit_transform.PNG)

### :white_check_mark: Deliverable 2: Reducing Data Dimensions Using PCA.

#### We used PCA algorithm to reduce the dimensions of X DataFrame to 3 principal components, and created the pcs_df DataFrame.
![pcs_df]( https://github.com/JoRanjit/Cryptocurrencies/blob/main/Images/pca_df.PNG)

### :white_check_mark: Deliverable 3: Clustering Cryptocurrencies Using K-means.

#### Using this pcs_df we created an elbow curve using hvplot to find the best-value for K.
![elbow]( https://github.com/JoRanjit/Cryptocurrencies/blob/main/Images/elbow_curve.png)

#### We used KMeans algorithm to make predictions of the K clusters for the cryptocurrencies’ data.
![predict]( https://github.com/JoRanjit/Cryptocurrencies/blob/main/Images/predictions.PNG)

#### Finally we created clustered_df by concatenating the <i> crypto_df and pcs_df</i> DataFrames on the same columns and added <i> CoinName and Class </i> columns to the clustered_df as below.

![clustered_df]( https://github.com/JoRanjit/Cryptocurrencies/blob/main/Images/crypto_df.PNG)

### :white_check_mark: Deliverable 4: Visualizing Cryptocurrencies Results.

#### Here we create a 3D scatter plot using the Plotly Express scatter_3d function to plot the three clusters from the clustered_df DataFrame.

![scatter-3d]( https://github.com/JoRanjit/Cryptocurrencies/blob/main/Images/scatter-3D.png)

#### Next created a table with tradable cryptocurrencies using the hvplot.table() function.

![hvplot-table]( https://github.com/JoRanjit/Cryptocurrencies/blob/main/Images/hvplot_table.PNG)

<h3> :fleur_de_lis: There are 532 tradable cryptocurrencies. </h3>

![total]( https://github.com/JoRanjit/Cryptocurrencies/blob/main/Images/total_number.PNG)

#### Finally we created an hvplot scatter plot with x="TotalCoinsMined", y="TotalCoinSupply", and by="Class" which shows the CoinName when you hover over the the data point.

![hvplot-scatter]( https://github.com/JoRanjit/Cryptocurrencies/blob/main/Images/hvplot_scatter.png)

 <h2> :heavy_check_mark: In this way - we were able to calssify 532 tradable cryptocurrencies to 4 Classes, and then further classify them based on their supply and avialbility in the trade market. Customers also have the ability to slice and dice the data using a 2D or a 3D chart. </h2>










