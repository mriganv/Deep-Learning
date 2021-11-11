# Deep-Learning

## Overview:

The purpose of this project analysis is to use the Tensorflow deep learning framework, written in Python to predict the success of applicants funded by Alphabet soup foundation. 

## Results:

### Data Preprocessing

The column IS_SUCCESSFUL will be the target variable as it has the binary data referring to whether the money was used effectively. 
APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT columns are the features for the model.
Encoding of the categorical variables, spliting into training and testing datasets and standardization have been applied to the features.
It’s best to drop most of the non-numeric features like EIN and NAME columns from the dataframe. As these variables are neither targets nor features.

### Compile, Train, and Evaluate the Model

 * How many neurons, layers, and activation functions did you select for your neural network model, and why?
    * Were you able to achieve the target model performance?
    * What steps did you take to try and increase model performance?

Selected Relu activation for hidden layers and Sigmoid for the output layer. And selected 2 hidden layers with 77 and 50 neurons in each layer respectively. This gave us 7,151 total trainable parameters for the model. 
Input:
![Screenshot 2021-11-10 215902](https://user-images.githubusercontent.com/81407869/141245864-601a54f3-4f40-4d99-8d90-68120c34d286.jpg)

#### Result:

![Screenshot 2021-11-10 215822](https://user-images.githubusercontent.com/81407869/141245904-5ba8dde9-ce23-4207-a57c-bf0b0623b7ac.jpg)
