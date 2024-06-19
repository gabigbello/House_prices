# House_pricesRL,
 Prediction of house prices based on the Ames Housing dataset

Description: Database 'Ames Housing dataset' with 79 initial variables describing (almost) every aspect of residential homes in Ames, Iowa.
Goal: Prediction of final price of each home on  test.csv

Language used: python - jupyter notebook

Files:
code.py - code for prediction
train.csv - train dataset
test.csv - prediction dataset for final price
data_description - description of each variable

Workflow stages:
1. Understanding the problem and the dataset itself.
2. Studying the dataset, cleaning columns and rows of null values. Analyzing to understand better each column and how the data is distributed, to
finally get to choose how to replace these null values (median, most common value or random choice).
3. Analyzing data, identifying patterns and exploring it. In this step we also need to understand what columns to keep in our initial dataset.
4. Creating our "training" and "test" groups, after cleaning both train and test datasets and keeping the same columns on both.
5. Model and predict using a lot of models to compare our results among them and chose which one to use for our final predict.
6. Save final submission file (Results can be seen on: https://www.kaggle.com/gabrielagbello)

Concepts used:
- K-Means clustering is an algorithm that partitions a dataset into a specified number of clusters. Each cluster is defined by its centroid (the mean of the points in the cluster), and each data point is assigned to the cluster with the closest centroid.
    #Goal: Identify the number of clusters where the SSE starts to diminish at a slower rate, forming an "elbow" in the plot.
    #Interpretation: The point where the elbow occurs is considered the optimal number of clusters, balancing compactness and efficiency.
- The Sum of Squared Errors (SSE), also known as "inertia" in the context of K-Means, is a measure of how compact the clusters are. It is calculated as the sum of the squared distances between each data point and the centroid of the cluster to which it belongs. Lower SSE values indicate more compact and well-defined clusters.

