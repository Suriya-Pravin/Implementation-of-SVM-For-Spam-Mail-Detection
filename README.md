# Ex-11:Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Import the necessary python packages using import statements.

2.Read the given csv file using read_csv() method and print the number of contents to be displayed using df.head().

3.Split the dataset using train_test_split.

4.Calculate Y_Pred and accuracy.

5.Print all the outputs.

6.End the Program.

## Program:
```py
Program to implement the SVM For Spam Mail Detection..
Developed by: Suriya Pravin M
RegisterNumber: 212223230223

import chardet
file='spam.csv'
with open (file,'rb') as rawdata:
    result = chardet.detect(rawdata.read(100000))
result

import pandas as pd
data=pd.read_csv("spam.csv",encoding='windows-1252')

data.head()

data.info()

data.isnull().sum()

x=data["v1"].values
y=data["v2"].values

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)

from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()

x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)

from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred

from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
```
## Output:
## Encoding:
![image](https://github.com/user-attachments/assets/94a2e2ae-97b2-4b4f-ad57-9c7d6ed96b2c)


## Head():
![image](https://github.com/user-attachments/assets/27ef174b-6f5b-4a5d-a048-ea0ca7e91d4e)



## Info():
![aa](https://github.com/user-attachments/assets/b11afcfa-fc0c-45d5-a5c3-19471c14f630)




## isnull().sum():
![aas](https://github.com/user-attachments/assets/6fa1f523-23b2-4a3f-821c-7d7ba41855ef)




## Prediction of y:
![image](https://github.com/user-attachments/assets/f24d4be6-4ed5-4ea1-8e71-b50aa6ee2d59)



## Accuracy:
![image](https://github.com/user-attachments/assets/58efd971-088b-454d-b0a4-289182f6a1c1)



## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
