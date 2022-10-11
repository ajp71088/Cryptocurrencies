# Cryptocurrencies

### Overview
In Python, the challenge was to use Principal Component Analysis & K-means clustering to create an analysis of the cryptocurrency market.

#### Deliverable 1 - Preprocessing the Data for PCA
Kept cryptocurrencies that are being traded and have a working algorithm with the following code:

![image](https://user-images.githubusercontent.com/107162310/195135506-57e8d22a-e1e4-4b20-af95-88429bb52ed4.png)

Performed further data preprocessing, including removing null values and dropping unnecessary columns:

![image](https://user-images.githubusercontent.com/107162310/195135804-e6891724-a12a-49d0-ab76-82f0cffb3a6d.png)

Created a new DataFrame to hold the coin names, and then dropped that column from the crypto_df:

![image](https://user-images.githubusercontent.com/107162310/195136018-84fcbab1-a34a-4eef-bbd5-ad878522150c.png)

Finally, used the get_dummies method to create variables for the columns with text-based data so that they can be used in the modeling, and then used StandardScaler to standardize the features:

![image](https://user-images.githubusercontent.com/107162310/195136301-26320681-a8f5-4416-aebd-251077563232.png)

#### Deliverable 2 - Reducing Data Dimensions Using PCA
Reduced the dimensions of the X DataFrame to three principal components and then placed those into a new DataFrame with the following code:

![image](https://user-images.githubusercontent.com/107162310/195137279-07950f70-a42e-4562-8fcc-a80faf2587ca.png)

#### Deliverable 3 - Clustering Cryptocurrencies Using K-means
Using the K-means algorithm, the following code creates an elbow curve with hvPlot to find the best value for K from the pcs_df created in Deliverable 2:

![image](https://user-images.githubusercontent.com/107162310/195137706-946ad677-25b3-4066-bec7-fd2be9c406d4.png)

Ran the K-means algorithm with the number of components set to 4 as the elbow curve identified:

![image](https://user-images.githubusercontent.com/107162310/195138072-8ebb83d0-85b6-47c7-979d-fdda34b7ab5c.png)

Created a new DataFrame by concatenating the crypto_df and pcs_df, adding the CoinName column, and a Class column which holds the predictions from the K-means algorithm:

![image](https://user-images.githubusercontent.com/107162310/195138464-fa5d4a49-d1b7-48ca-9694-7f7725385f30.png)

#### Deliverable 4 - Visualizing Cryptocurrencies Results
Created a 3D scatter plot using Plotly Express with the following code:

![image](https://user-images.githubusercontent.com/107162310/195138930-1954e8ed-4be1-448d-aee3-dff6a5108c13.png)

Created a table with the tradable cryptocurrencies:

![image](https://user-images.githubusercontent.com/107162310/195139206-b2da223e-47cb-4df1-b246-c06dae104c99.png)

Used the MinMaxScaler to scale the TotalCoinSupply and TotalCoinsMined columns, and then placed that scaled data into a new DataFrame:

![image](https://user-images.githubusercontent.com/107162310/195139457-6da3d1ca-2985-4bd4-ac6c-b9ce47cc688b.png)

Lastly, created an hvplot scatter plot with that new DataFrame:

![image](https://user-images.githubusercontent.com/107162310/195139579-bb0253b5-5a8b-4807-8c05-6aaba6673c8f.png)
