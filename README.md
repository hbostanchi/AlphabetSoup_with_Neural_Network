# AlphabetSoup_with_Neural_Network
## Project Overview
In this module, we explore and implement neural networks using the TensorFlow platform in Python. We discuss the background and history of computational neurons as well as current implementations of neural networks as they apply to deep learning. We discuss the major costs and benefits of different neural networks and compare these costs to traditional machine learning classification and regression models. Additionally, we practice implementing neural networks and deep neural networks across a number of different datasets, including image, natural language, and numerical datasets. Finally, we learn how to store and retrieve trained models for more robust uses.
## Objectives
-	Compare the differences between the traditional machine learning classification and regression models and the neural network models.
-	Describe the perceptron model and its components.
-	Implement neural network models using TensorFlow.
- Explain how different neural network structures change algorithm performance.
-	Preprocess and construct datasets for neural network models.
-	Compare the differences between neural network models and deep neural networks.
-	Implement deep neural network models using TensorFlow.
-	Save trained TensorFlow models for later use.
#### Challenge Overview
In this challenge, we use unsupervised learning to analyze data on the cryptocurrencies traded on the market. We present a report of what cryptocurrencies are on the trading market and how cryptocurrencies could be grouped toward creating a classification for developing a new investment product. The data we work with is not ideal, so we process it to fit the machine learning models. Since there is no known output for what we are looking for, we decided to use unsupervised learning. To group the cryptocurrencies, we decided on a clustering algorithm to help determine about investing in this product. We used data visualizations to share our findings.

## Objectives
-	Import, analyze, clean, and preprocess a “real-world” classification dataset.
-	Select, design, and train a binary classification model of your choosing.
-	Optimize model training and input data to achieve desired model performance.

## Challenge Summary
### Data Preprocessing
In this section, we had to load the information about cryptocurrencies from the provided CSV file and perform some data preprocessing tasks. The data was retrieved from CryptoCompare

We started by loading the data in a Pandas DataFrame named [“crypto_df”](https://github.com/hbostanchi/Cryptocurrencies/blob/master/challenge/Crypto_challenge.ipynb) and continued with the following data preprocessing tasks:

- Remove all cryptocurrencies that aren’t trading.
- Remove the IsTrading column.
- Remove all cryptocurrencies with at least one null value.
- Remove all cryptocurrencies without coins mined.
- Store the names of all cryptocurrencies on a DataFramed named coins_name, and use the crypto_df.index as the index for this new DataFrame.
- Remove the CoinName column.
- Create dummies variables for all of the text features, and store the resulting data on a DataFrame named X.
- Use the StandardScaler from sklearn to standardize all of the data from the X DataFrame.

### Reducing Data Dimensions Using PCA
We used the [PCA algorithm from sklearn](https://scikit-learn.org/stable/modules/generated/sklearn.decomposition.PCA.html) to reduce the dimensions of the X DataFrame down to three principal components.

Once we had reduced the data dimensions, we created a DataFrame named “pcs_df” that includes the following columns:

- PC 1
- PC 2
- PC 3
We used the crypto_df.index as the index for this new DataFrame.

Clustering Cryptocurrencies Using K-means
We used the [KMeans algorithm from sklearn](https://scikit-learn.org/stable/modules/generated/sklearn.cluster.KMeans.html) to cluster the cryptocurrencies using the PCA data.

Create an elbow curve to find the best value for K, and use the pcs_df DataFrame.
Once you define the best value for K, run the K-means algorithm to predict the K clusters for the cryptocurrencies’ data. Use the pcs_df to run the K-means algorithm.
Create a new DataFrame named “clustered_df,” that includes the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinSupply, PC 1, PC 2, PC 3, CoinName, and Class.
Visualizing Results
We created data visualizations to present the final results.

Create a 3D scatter plot using Plotly Express to plot the clusters using the clustered_df DataFrame. You should include the following parameters on the plot: hover_name="CoinName" and hover_data=["Algorithm"] to show this additional info on each data point.
Use hvplot.table to create a data table with all the current tradable cryptocurrencies. The table should have the following columns: CoinName, Algorithm, ProofType, TotalCoinSupply, TotalCoinsMined, and Class.
Create a scatter plot using hvplot.scatter to present the clustered data about cryptocurrencies having x="TotalCoinsMined" and y="TotalCoinSupply" to contrast the number of available coins versus the total number of mined coins. Use the hover_cols=["CoinName"] parameter to include the cryptocurrency name on each data point.

#### Create a new [README.txt](https://github.com/hbostanchi/Neural_Network/blob/master/README.md) file within the same folder as your AlphabetSoupChallenge.ipynb notebook. Include a 5–10 sentence writeup in your README that addresses the following questions:

+ How many neurons and layers did you select for your neural network model? Why?

Observing the data, I decided that the columns EIN and Name were neither features nor targets. 
Also came up with the target variable column "Is_Successful".
For my first model, I chose 8 neurons in the first hidden layer and 4 neurons in the second. This model only achieved about 58.6% accuracy after 100 epochs.
+ Were you able to achieve the target model performance? What steps did you take to try and increase model performance? 

To optimize, I tried the following to add one neurons  on hidden layer. This model with 8 neurons in the first layer, 5 neurons in the second layer and reached the accuracy 0f %75.5 after 100 epoches.

+ If you were to implement a different model to solve this classification problem, which would you choose? Why?

Random forest classifiers are what I choose to use for classification into a more robust and accurate model. 
Random forest models have been popular in machine learning algorithms for many years due to their robustness and scalability. 



