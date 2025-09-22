# Customer-Segmentation-with-K-means-Clustering
This project demonstrates the application of the K-Means clustering algorithm for customer segmentation based on their annual income and spending score.

Steps:

1. Importing Dependencies:

numpy, pandas, matplotlib.pyplot, seaborn, and KMeans from sklearn.cluster.

2. Data Collection and Analysis:

Load the customer data from the "Mall_Customers.csv" file into a pandas DataFrame.
Examine the first few rows of the DataFrame using head().
Check the shape of the DataFrame using shape.
Get information about the DataFrame, including data types and non-null values, using info().
Check for any missing values in the DataFrame using isnull().sum().

3. Selecting Features:

Select the relevant columns for clustering: 'Annual Income (k$)' and 'Spending Score (1-100)'. These will be the features used for clustering.
Determining the Optimal Number of Clusters (Elbow Method):


4. Calculate the Within-Cluster Sum of Squares (WCSS) for a range of cluster numbers (e.g., 1 to 10). WCSS is the sum of squared distances between each point and the centroid of its cluster.

5. Plot the WCSS values against the number of clusters. This is known as the "Elbow Graph".
Identify the "elbow point" on the graph, which is the point where the rate of decrease in WCSS significantly changes. This point represents the optimal number of clusters. In this project, the optimal number of clusters was determined to be 5.

6. Training the K-Means Clustering Model:

Initialize the KMeans model with the optimal number of clusters (k=5), using the 'k-means++' initialization method to avoid the random initialization trap, and a specified random_state for reproducibility.
Fit the model to the selected features (X) to perform the clustering.
Obtain the cluster labels for each data point using fit_predict().

7. Visualizing the Clusters:

Create a scatter plot to visualize the clusters.
Plot each cluster with a different color for clarity.
Plot the centroids of the clusters as larger, distinct markers (e.g., black).
Add a title and labels to the x and y axes to make the plot informative.
Display the plot using plt.show().
Conclusion:
The visualization shows the distinct customer segments based on their annual income and spending score. These segments can be used for targeted marketing strategies and business decisions.

