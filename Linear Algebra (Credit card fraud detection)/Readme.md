
#Exploratory Data Analysis on Kaggle DataSet
  
## Kaggle Data Set - Credit Card Fraud
### The datasets contains transactions made by credit cards in September 2013 by european cardholders. 
## Dataset Information:
    * Number of Instances: 284,807
    * Number of Attributes: 31 (including the class attribute)
    * Attribute Information:
    * Features V1, V2, ... V28 are the principal components obtained with PCA.    
    * The only features which have not been transformed with PCA are 'Time' and 'Amount'.
    * Feature 'Time' contains the seconds elapsed between each transaction and the first 
      transaction in the   dataset.
### Class (class attribute):
    * Feature 'Class' is the response variable and it takes value 1 in case of fraud and 0 
      otherwise. 
      1 = Fraud Transaction
      0 = Normal Transaction
### All the remaining details regarding the data set can be found in the below link.
### [CreditCardFraud](https://www.kaggle.com/dalpozz/creditcardfraud/data)

### Task 1:
1) Performed EDA on the dataset which is imabalanced.

### Task 2:  
1) Found Similarity of Transactions using Cosine Similarity.
2) Formula used :similarity(i,j) = dot product (vi, vj) / length(vi) * length(vj)
3) Took a sample from the data set which contains no less than 100 transactions, and for every transaction in the sample found  top 10 transactions 
     in the dataset which have the lowest similarity(i,j).
     
4) Sample Result for one of the transaction :
    
    For the transaction id = 134354, and Class = 0.
    
    *Similar transactions* are :
    
   Class = 0, Similarity = 0.999372, transactionId = 21934
   
   Class = 0, Similarity = 0.999723, transactionId = 219257
   
   Class = 0, Similarity = 0.999944, transactionId = 49906
   
   Class = 0, Similarity = 0.999961, transactionId = 35730
   
   Class = 1, Similarity = 0.999970, transactionId = 43428
   
   Class = 0, Similarity = 0.999982, transactionId = 38442
   
   Class = 0, Similarity = 0.999986, transactionId = 105030
   
   Class = 0, Similarity = 0.999996, transactionId = 80419
   
   Class = 0, Similarity = 0.999996, transactionId = 36749
   
   Class = 0, Similarity = 0.999998, transactionId = 187045     


 **EDA+and+Similarity+of+Transactions+on+CreditCardFraudDetection.pdf** contains all the code, plots and results.
 
 **EDA and Similarity of Transactions on CreditCardFraudDetection.ipynb** contains python code.
 
 ## How to run the code:
  **use Ipython(Jupyter)** notebook to run the code.



