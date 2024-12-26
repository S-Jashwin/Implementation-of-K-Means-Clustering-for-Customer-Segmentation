# Implementation-of-K-Means-Clustering-for-Customer-Segmentation

## AIM:
To write a program to implement the K Means Clustering for Customer Segmentation.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv("Mall_Customers.csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.cluster import KMeans
wcss = []
for i in range(1,11):
  kmeans = KMeans (n_clusters = i, init ="k-means++")
  kmeans.fit(data.iloc[:,3:])
  wcss.append(kmeans.inertia_)
plt.plot(range(1,11),wcss)
plt.xlabel("no of cluster")
plt.ylabel("wcss")
plt.title("Elbow Metthod")
km=KMeans(n_clusters=5)
km.fit(data.iloc[:,3:])
y_pred = km.predict(data.iloc[:,3:])
y_pred
data["cluster"]=y_pred
df0=data[data["cluster"]==0]
df1=data[data["cluster"]==1]
df2=data[data["cluster"]==2]
df3=data[data["cluster"]==3]
df4=data[data["cluster"]==4]
plt.scatter(df0["Annual Income (k$)"],df0["Spending Score (1-100)"],c="red",label="cluster0")
plt.scatter(df1["Annual Income (k$)"],df1["Spending Score (1-100)"],c="pink",label="cluster1")
plt.scatter(df2["Annual Income (k$)"],df2["Spending Score (1-100)"],c="green",label="cluster2")
plt.scatter(df3["Annual Income (k$)"],df3["Spending Score (1-100)"],c="blue",label="cluster3")
plt.scatter(df4["Annual Income (k$)"],df4["Spending Score (1-100)"],c="black",label="cluster4")
plt.legend()
plt.title("Customer Segments")

/*
Program to implement the K Means Clustering for Customer Segmentation.
Developed by: JASHWIN.S
RegisterNumber: 24000675
*/

## Output:
![image](https://github.com/user-attachments/assets/0bc1ae07-a1a5-4085-8709-595eeb5afd5e)
![image](https://github.com/user-attachments/assets/282885c8-a29a-4b04-a420-a4282d4e63b8)
![image](https://github.com/user-attachments/assets/182c5958-d2c3-4b07-9d93-a84397b0ed1d)
![image](https://github.com/user-attachments/assets/4c1fefaf-f1fb-42bb-80eb-b6b43341ac31)
![image](https://github.com/user-attachments/assets/6392c639-62ba-49f3-8d6b-e3d257ac6947)
![image](https://github.com/user-attachments/assets/dff24b57-fd29-4bc0-be04-d69df38b4a18)
![image](https://github.com/user-attachments/assets/a728f09e-4728-4ab1-b902-bef241b73aca)









## Result:
Thus the program to implement the K Means Clustering for Customer Segmentation is written and verified using python programming.
