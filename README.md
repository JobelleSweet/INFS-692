# INFS-692
This is our final project in STT 371: Advanced Statistical Computing. 
##### Objective
The objective of this project is to develop different models to predict failure (endpoint) of the radiomics signature based from MRI, PET and CT scans. 
##### Packages
These are the packages needed in this project: 'readr', 'dplyr', 'ggplot2', 'stringr', 'recipes', 'rsample', 'xgboost', 'gbm', 'rpart', 'rpart.plot', 'ROCR', 'pROC', 'gridExtra', 'tidyverse', 'cluster', 'factoextra', 'caret', 'keras', 'tfruns', 'tensorflow', 'tfestimators', and 'mclust'.
##### Data
Radiomics dataset is used in this project. It has 431 variables with 197 observations.
##### Preprocess the data
First, I checked and removed the missing values. Next, I checked for the normality of the data by using shapiro.test and if it is not normal, then I normalized the data by using scale() function. Lastly, I get the correlation of the whole data except the categorical variables such as Institution and Failure.binary. In addition, I split the data into training (80%) and testing (20%)
##### Model1
In Model1, I created 3 models in ensemble classification model. I used the xgboost, gbm and rpart to model the training and testing dataset. After that I printed the AUC values during training, the top 20 important features during training and the AUC values during testing.
##### Model2
In Model2, I created a neutral network-based classification model by creating a 5 hidden layes with 256, 128, 128, 64and 64 neurons, respectively with activition functions of sigmoid. And then created an output layer with 2 neurons respectively with activition functions of Softmax. Every layer is followed by a 30% dropout to avoid overfitting. Then, create a backpropagation compiler approach and model compiler approach. After that,I trained the model with epoch=10, batch size=128, and validation split=0.15. Lastly, I evaluated the trained model using testing dtaset and get the model prediction using testing dataset.
##### Model3
In Model3 I created 3 unsupervised learning models, namely, kmeans, hierarchical and model-based and compare the results of the 3 models.
