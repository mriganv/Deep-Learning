# Deep-Learning

## Overview:

The purpose of this project analysis is to use the Tensorflow deep learning framework, written in Python to predict the success of applicants funded by Alphabet soup foundation. 

## Results:

### Data Preprocessing

The column IS_SUCCESSFUL will be the target variable as it has the binary data referring to whether the money was used effectively. 
The following columns APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT are the features for our model.
Encoding of the categorical variables, spliting into training and testing datasets and standardization have been applied to the features.
It’s best to drop most of the non-numeric features like EIN and NAME columns from the dataframe. As these variables are neither targets nor features.




