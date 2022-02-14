# Implementation of K-Means Clustering Algorithm
## Aim
To write a python program to implement K-Means Clustering Algorithm.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation

## Algorithm:

### Step1:
Import pandas.
<br>

### Step2:
Import matplotlib.pyplot.
<br>

### Step3:
Import sklearn.cluster from KMeans module.
<br>

### Step4:
Import seaborn
<br>

### Step5:
Import warnings
<br>
### Step6:
Display the predicted_class

## Program:
```
#Developed by: GAUTHAM M G
#Register number: 212221230027
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans
import seaborn as sns
import warnings
warnings.filterwarnings('ignore')
x1 = pd.read_csv('clustering.csv')
print(x1.head(2))
x2 = x1.loc[:,['ApplicantIncome','LoanAmount']]
print(x2.head(2))

x=x2.values
sns.scatterplot(x[:,0],x[:,1])
plt.xlabel('Income')
plt.ylabel('Loan')
plt.show()

kmean = KMeans(n_clusters=4)
kmean.fit(x)

print('Cluster Centers:',kmean.cluster_centers_)
print('Labels:',kmean.labels_)

predicted_class = kmean.predict([[9200,110]])
print('The cluster group for Applicant Income 9000 and Loanamount',predicted_class)



```
## Output:
![image](https://user-images.githubusercontent.com/94810884/153896358-a665c659-5d2c-459e-a62f-0b0a28949cd6.png)


<br>

## Result
Thus the K-means clustering algorithm is implemented and predicted the cluster class using python program.
