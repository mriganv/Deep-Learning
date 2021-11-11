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
Our data is having fewer dimensions or features, so assuming that 1 to 2 hidden layers would work. So tried the below input to see if it gives us an expected accuracy. Also keeping in mind that increasing hidden layers would also increase the complexity of the model and choosing hidden layers such as 8, 9, or in two digits may sometimes lead to overfitting.  

Input:
Selected Relu activation for hidden layers and Sigmoid for the output layer. Selected 2 hidden layers with 15 and 5 neurons for each layer respectively. With 100 epochs in the training model, this gave us 746 total trainable parameters for the model. With 100 epochs for the training model, I got the below result. 

### Result:

Got a 73% accuracy on the above selection.

![Screenshot 2021-11-10 215822](https://user-images.githubusercontent.com/81407869/141245904-5ba8dde9-ce23-4207-a57c-bf0b0623b7ac.jpg)

#### To achieve a better target model performance, tried to add more bins for one more column in the dataset. 
#### Tried three attempts to achieve the target of 75% or above target predictive accuracy.

Neural networks have two main hyperparameters that control the architecture or topology of the network: the number of layers and the number of nodes in each hidden layer.
Trying some random configurations of layers and nodes per layer.

### Attempt #1
Input:
Selected Relu activation for hidden layers and Sigmoid for the output layer. Selected 3 hidden layers with 100, 70, and 40 neurons for each layer respectively. This gave us 14,951 total trainable parameters for the model. With 100 epochs for the training model, results are below. With decreasing number of neurons in each layer, 

### Result:

![Screenshot 2021-11-10 224405](https://user-images.githubusercontent.com/81407869/141250678-2a43ef24-0dc0-48fb-84cf-bc6a191443e2.jpg)


### Attempt #2
Input:
Selected Tanh activation for hidden layers and Sigmoid for the output layer. Selected 2 hidden layers with 80 and 40 neurons for each layer respectively. This gave us 7,281 total trainable parameters for the model. With 100 epochs for the training model, results are below. 

### Result:

![Screenshot 2021-11-10 222755](https://user-images.githubusercontent.com/81407869/141248849-ae53ca5d-66cd-4003-af86-10a635609260.jpg)

### Attempt #3
Input:
Selected Tanh activation for hidden layers and Sigmoid for the output layer. Selected 3 hidden layers with 70, 40 and 10 neurons for each layer respectively. This gave us 6,761 total trainable parameters for the model. With 50 epochs for the training model, results are below.

### Result:

![Screenshot 2021-11-10 224615](https://user-images.githubusercontent.com/81407869/141250959-3752020a-aa7d-4aed-bce4-025a7e050770.jpg)


### Summary:








    
