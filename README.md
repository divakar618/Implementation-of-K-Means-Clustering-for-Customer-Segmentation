# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm


1.Import pandas and matplot libraries.


2.import Kmeans algorithm to solve customer segmentation.


3.Using the for loop cluster the given data


4.Predict the output and plot data graphs.


5.Display the outputs

## Program:
```
/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: DIVAKAR R 
RegisterNumber: 212222240026

import pandas as pd

import matplotlib.pyplot as plt

data=pd.read_csv("/content/Mall_Customers (1) (1).csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.cluster import KMeans
WCSS=[]

for i in range(1,11):
  kmeans=KMeans(n_clusters=i,init="k-means++")
  kmeans.fit(data.iloc[:,3:])
  WCSS.append(kmeans.inertia_)

  plt.plot(range(1,11), WCSS)
plt.xlabel("No. of clusters")
plt.ylabel("WCSS")
plt.title("Elbow Method")

km=KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])

y_pred=km.predict(data.iloc[:,3:])
y_pred

data["cluster"] = y_pred
df0 = data[data["cluster"]==0]

df1 = data[data["cluster"]==1]

df2 = data[data["cluster"]==2]

df3 = data[data["cluster"]==3]

df4 = data[data["cluster"]==4]

plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")

plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="black",label="cluster1")

plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="blue",label="cluster2")

plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="green",label="cluster3")

plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="magenta",label="cluster4")

plt.legend()
plt.title("Customer segments")
*/
```

## Output:


data.head() function



![ml-801](https://github.com/divakar618/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/121932143/ca4fd168-0ce4-4a8c-8b9b-eb9f1be64592)


data.info



![ml802](https://github.com/divakar618/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/121932143/3ef947a3-cb49-4e23-91ef-403d85a443ab)




data.isnull().sum() function




![ml803](https://github.com/divakar618/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/121932143/7bd0512e-fe00-415a-bea1-213c8f8e4271)



Elbow Method Graph



![ml804](https://github.com/divakar618/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/121932143/a911fb18-e659-40aa-9e77-5877fd187901)


KMeans clusters



![ml805](https://github.com/divakar618/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/121932143/c7768fe0-c43e-423e-92f6-74dc6d417b2b)




array()



![ml806](https://github.com/divakar618/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/121932143/0bbc3db6-5cbd-42fa-99ef-10bad47f3667)



Customers segments Graph



![ml807](https://github.com/divakar618/Implementation-of-K-Means-Clustering-for-Customer-Segmentation/assets/121932143/cd053997-2eaa-4564-8a20-200d6d06e771)






## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
