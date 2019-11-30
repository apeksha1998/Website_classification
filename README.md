# Phishing_website_detection
It is a project of detecting phishing websites using Machine learning with Python

Phishing websites are those websites that mimic the legitimate websites and deceive online users in order to steal their sensitive information. Phishing website identification can be defined in machine learning context as a typical classification problem. 

## Steps Followed:
#### 1) Data Exploration:
   Using data.info()
   Data is clean and no Null values.

#### 2) Feature Importance
  The feature importance of each feature of your dataset by using the feature importance property of the model.
  Feature importance gives you a score for each feature of your data, the higher the score more important or relevant is the     feature towards your output variable.
  Feature importance is an inbuilt class that comes with Tree Based Classifiers, we will be using Extra Tree Classifier for       extracting the top 10 features for the dataset.
 
#### 3) Correlation Matrix with Heatmap
  Correlation states how the features are related to each other.
  Correlation can be positive (increase in one value of feature increases the value of the target variable) or negative (       increase in one value of feature decreases the value of the target variable)
  Heatmap makes it easy to identify which features are most related to the target variable, we will plot heatmap of             correlated   features using the seaborn library.
  
#### 4) Splitting the data into Train and Test
  77% of data is considered for training and 33% for testing. 
  
### Training the Model
   This is a classification task and the aim is to classify the websites to either
   "legitimate" or "phishy" based on the predictor variables.
#### Models used:
   ##### Random Forest Classifier
   ##### Decision Tree Classifier
   ##### Support Vector Machine
   ##### Gaussian Naive Bayes Classifier 
  
### Results:

#### 1) Decision Tree Classifier

   Decision Tree classifier gave an accuracy of 0.9593
   
#### 2) Gaussian Naive Bayes Classifier
                  

              precision    recall  f1-score   support
              0       0.95      0.95      0.95       456
              1       0.93      0.93      0.93       355
              
            accuracy                            0.94       811
            macro avg       0.94      0.94      0.94       811
         weighted avg       0.94      0.94      0.94       811

      

##### Accuracy on training set is 0.9142857142857143
##### Accuracy on testing set is 0.9395807644882861
      
#### 3) Random Forest Classifier
   precision    recall  f1-score   support

           
                  precision  recall  f1-score    support
           0       0.97      0.97      0.97       456
           1       0.97      0.96      0.96       355
         
           
           accuracy                            0.97       811
           macro avg       0.97      0.97      0.97       811
           weighted avg    0.97      0.97      0.97       811
    
##### Accuracy is 0.969173859432799

    
#### 4) Support Vector Machine Classifier
   

                precision    recall  f1-score   support
           0       0.95      0.96      0.96       456
           1       0.95      0.94      0.95       355
           
           accuracy                            0.95       811
           macro avg       0.95      0.95      0.95       811
           weighted avg    0.95      0.95      0.95       811

   
##### Accuracy on training set is 0.9556231003039514 
##### Accuracy on testing set is  0.9531442663378545

### Using PRINCIPLE COMPONENT ANALYSIS(PCA) 
##### After applying PCA, results obtained on testing data sets are :

#### Accuracies : 

###### Support Vector Classifier after applying PCA = 0.9642
###### Random Forest Classifier after applying PCA = 0.9667

### Conclusion
While classifying websites, it’s important to correctly identify the phishing websites. 
Identifying a phishing website correctly is considered as the true positive scenario and
identifying a legitimate website correctly is considered as the true negative scenario. There is
no harm caused to the user by misclassifying a legitimate website (false positive), but the
consequences of misclassifying a phishing website (false negative) is very disastrous. Hence
our models are evaluated based on the True Positive Rate (Recall).
Since Random Forest Classifier gives best accuracy and even high precision rate of 97% with accuracy of 96.9173%.Random Forest Classifier can be considered as best to train our model.
