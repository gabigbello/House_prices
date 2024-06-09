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
1. Understanding the problem.
2. Study of the dataset, cleaning columns and rows.
3. Analyze data, identify patterns and explore it.
4. Creating our "training" and "test" groups.
5. Model and predict.
6. Save final submission file.

Treatments to get the database sharper - proposals:
MSZoning - Only letting the first letter of the values (this way we will make RH, RL, RP and RM into one (Residential))
LotShape - Transform data to keep only the first letter (R for Regular and I for Irregular)
Neighborhood - Only keep first word and organize to be a clean data
Create column (Overall) with the sum of OverallQual and OverallCond
1stFlrSF and 2ndFlrSF - Put it into groups of data
GrLivArea - Put it into groups of data
Sum BsmtFullBath + BsmtHalfBath + FullBath + HalfBath
WoodDeckSF - group
OpenPorchSF - group
EnclosedPorch - group
PoolArea - group
MiscVal - group
SaleType - organize
SaleCondition - organize

Initial test by taking out some columns, since we have too much columns in our predict model. 
Columns to take out:
1. Lot Frontage - Lot Area can already be used with this parameter
2. Alley - Street can already be used for this parameter
3. LandContour - LotShape already helps us with this info
4. LotConfig
5. Land Slope
6. Condition 2 - Only keep Condition 1 initially
7. House Style
8. YearRemodAdd
9. RoofStyle
10. Exterior2nd
11. MasVnrArea
12. ExterCond
13. BsmtQual
14. BsmtExposure
15. BsmtFinSF1
16. BsmtFinType1
17. BsmtFinType2
18. BsmtFinSF2
19. BsmtUnfSF
20. HeatingQC
21. Electrical
22. Functional
23. FireplaceQu
24. GarageYrBlt
25. GarageFinish
26. GarageCars
27. GarageCond
28. 3SsnPorch
29. ScreenPorch
30. MiscFeature
31. MoSold
32. YrSold

Concepts used:
K-Means Clustering
K-Means clustering is an algorithm that partitions a dataset into a specified number of clusters. Each cluster is defined by its centroid (the mean of the points in the cluster), and each data point is assigned to the cluster with the closest centroid.

SSE (Sum of Squared Errors)
The Sum of Squared Errors (SSE), also known as "inertia" in the context of K-Means, is a measure of how compact the clusters are. It is calculated as the sum of the squared distances between each data point and the centroid of the cluster to which it belongs. Lower SSE values indicate more compact and well-defined clusters.

#Goal: Identify the number of clusters where the SSE starts to diminish at a slower rate, forming an "elbow" in the plot.
#Interpretation: The point where the elbow occurs is considered the optimal number of clusters, balancing compactness and efficiency.