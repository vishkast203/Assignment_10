# Assignment_10
Assignment-10 Unsupervised Learning, clustering &amp; scaling with PCA's
Executive Summary: 
The purpose of this project was to investigate other methods to evaluating assembling investment portfolios based on Crypto Currencies versus relying on traditional methods such as returns and volatility. Based on the daatset evaluated,  we need to continue further analyssis with different datasets as the data set used for this projet did not yield significantly differing results.  However the analytical tools did show that the methodologys employed lend itself for quick segregation of large financial data to find data clusters of interest to narrow the analysts focus anad potentially save time to making investment decisions.

Analytical Tools utiized:
The software used was Python version 3.8 along with Jupyter NoteBooks. The Libraries & dependencies     imported were:  
 import pandas as pd
 import hvplot.pandas
 from path import Path
 from sklearn.cluster import KMeans
 from sklearn.decomposition import PCA
 from sklearn.preprocessing import StandardScaler
Data Analytical Steps:
First the csv file provided was loaded for review as a dataframe. The data was then checked for consistency using the HEad & Tail functions. The desctribe function was used to primarily verify the data counts and the general statistical summary of the data. The dataset was finally reviewed using a line plot of the various crypto currencies.
Next the Standard Scaler(plus fit.transform function) & SciKitLearn was used to create a scaled data set & a new dataframe was created using the coin_id colums as the index. 

A best value for k was chosen as follows: 
1. Created a list with the number of k-values with a range of 1 - 11. A empty inertia List was created for storing inertia data using a For Loop which was then fitted t the scaled dataframe. The First Elbow chart was created to pick the best value for k. (=4)
Ths was followed by predicting the clusters group using the original data set & the array outputs were checked along with the generated Dataframes. A new column labelled CryptoClusters was created that showed the scaled data. This was then plotted using a scatter plot. 
The second phase of the analysis was to use the Principal Component Analysis (PCA) method. Teh data clusters were reduced to 3 principle components &  the variance was determined. We observed that the first principal component contains 33.7% of the variance, and the second principal component contains 31.35% of the variance. Both components together thus contain approximately 65% of the original information. The third principal contains approximately 23.41% to bring the total explained variance to approx. 88.41%.
Further a new DF was created &  the three columns of PCA values generated were checked. The best k value was re-determined & found to still be k= 4 based off the resulting Elbow Plots  & Scatter /Cluster plots. The Composite plots were compared to show hardly any change in the cluster formation of the datasets. Hence no efficiencies were gained by using the PCA methiodology for this dataset.
In summary it is recommended that additonal datasets be screened using ths methodology to determine if the PCA analysis lends value to reduction in analytical time as the usefulness of this tool cannot n=be determined using just one dataset.  