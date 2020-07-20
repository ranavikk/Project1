# credit_card_fraud_detection
PROJECT DESCRIPTION:

It is important that credit card companies are able to detect the fraudulent credit card transactions  so that the customers will not get charged for items that they did not purchased.I have done this project by detecting the anomaly using ISOLATION FOREST algorithms and LOCAL OUTLIER FACTOR ALGORITHM  for my proposed model for detecting frauds in credit card system using python.

DATASET:
 I have  analysed the  dataset which is taken from  Kaggle.
 link: https://www.kaggle.com/mlg-ulb/creditcardfraud
 The datasetis in CSV format(creditcard.csv), it contains Credit card transactions which are made by customers during September 2013 in Europe containing  284,807 transactions. Looking upon the behaviour of the transactions Credit card transactions are characterized into two categories fraudulent and non-fraudulent.Original features and more background information are not provided in the dataset because of confidentiality issues. Only numerical input variables are provided which are the results of Principal Component Analysis (PCA) Transformation. Features V1, V2 ... V28 are the  principal  components  obtained  with  PCA,  the  only features  which  have  not  been  transformed  with  PCA  are 'Time'  and  'Amount'.  Feature  'Time'  contains  the  seconds elapsed between each transaction and the first transaction in the dataset. The feature 'Amount' is the transaction Amount, this feature can be used for example-dependant cost-sensitive learning. Feature 'Class' is the response variable and it takes value 1 in case of fraud and 0 otherwise. 

ISOLATION FOREST METHOD:
Isolation forest is a tree-base model that is developed to detect outliers . This algorithm is based upon the fact that anomalies  are the  data points  which are  few and different. These  properties  result  in  susceptible  mechanism  to anomalies  which  is  known  as  Isolation.  This  method  is basically  different  from  all  other  existing  methods  and  is highly useful. To detect the anomalies rather than the  basic distance  and  density  measures  it  introduces  the  use  of isolation as an efficient and more effectively. This algorithm has  small  memory  requirement  and  low  linear  time complexity. It builds a good performing model with a small number  of  trees  using  small  sub-samples  of  fixed  size, regardless of the size of a data set.

LOCAL OUTLIER ALGORITHM:
The LOF algorithm is an unsupervised outlier detection method which computes the local density deviation of a given data point with respect to its neighbors. It considers as outlier samples that have a substantially lower density than their neighbors.
The number of neighbors considered, (parameter n_neighbors) is typically chosen 1) greater than the minimum number of objects a cluster has to contain, so that other objects can be local outliers relative to this cluster, and 2) smaller than the maximum number of close by objects that can potentially be local outliers. In practice, such informations are generally not available, and taking n_neighbors=20 appears to work well in general.

 METHODOLOGY:
 In order to classify the transactions as fraud or non-fraud i used some other standards of correctness which are as:
 ï‚· Precision 
 ï‚· Recall 
 ï‚· F1-score
 ï‚· Support 
 These all standard of correctness are depend upon the Actual and  Predict  class, so i draw a 2Ã—2 confusion matrix .
 
 RESULT:
 Isolation Forest: 73
Accuracy Score :
0.9974368877497279
Classification Report :
              precision    recall  f1-score   support

           0       1.00      1.00      1.00     28432
           1       0.26      0.27      0.26        49

   micro avg       1.00      1.00      1.00     28481
   macro avg       0.63      0.63      0.63     28481
weighted avg       1.00      1.00      1.00     28481

Local Outlier Factor: 97
Accuracy Score :
0.9965942207085425
Classification Report :
              precision    recall  f1-score   support

           0       1.00      1.00      1.00     2843
           1       0.02      0.02      0.02        49

   micro avg       1.00      1.00      1.00     28481
   macro avg       0.51      0.51      0.51     28481
weighted avg       1.00      1.00      1.00     28481

By comparing the results of Local Outlier Factor and Isolation Forest algorithms,i have found that the Local Outlier Factor is best for detecting the frauds in credit card transactions with the accuracy of  97% while the isolation forest algorithm gave the accuracy of 73% only.
  
