# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
Import required libraries and read the customer dataset.
Select Annual Income and Spending Score columns as input data.
Apply K-Means clustering with 5 clusters to group customers.
Plot the clusters and centroids using a scatter graph.

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: 
RegisterNumber: 




```import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans

df = pd.read_csv("Mall_Customers.csv")

print(df.head())

X = df[['Annual Income (k$)', 'Spending Score (1-100)']]

model = KMeans(n_clusters=5, random_state=42)

df['Cluster'] = model.fit_predict(X)

print(df)

plt.scatter(
    X['Annual Income (k$)'],
    X['Spending Score (1-100)'],
    c=df['Cluster']
)

plt.scatter(
    model.cluster_centers_[:,0],
    model.cluster_centers_[:,1],
    color='red',
    marker='X',
    s=200
)

plt.xlabel("Annual Income")
plt.ylabel("Spending Score")
plt.title("Customer Segmentation using K-Means")

plt.show()
```
## Output:
<img width="1026" height="726" alt="Screenshot 2026-05-28 202047" src="https://github.com/user-attachments/assets/330e9c3e-c8f6-4963-9c04-96dd0a2a34d2" />
<img width="729" height="462" alt="Screenshot 2026-05-28 202059" src="https://github.com/user-attachments/assets/61a854cc-21ab-46ec-b785-a448ae5c7507" />


## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
