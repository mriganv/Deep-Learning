# Deep-Learning

## Overview:

The purpose of this project analysis is to use the Tensorflow deep learning framework, written in Python to predict the success of applicants funded by Alphabet soup foundation. 

## Results:

### Data Preprocessing

* The column IS_SUCCESSFUL will be the target variable as it has the binary data referring to whether the money was used effectively. 
* APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT columns are the features for the model.
* Encoding of the categorical variables, spliting into training and testing datasets and standardization have been applied to the features.
* It’s best to drop most of the non-numeric features like EIN and NAME columns from the dataframe. As these variables are neither targets nor features.

### Compile, Train, and Evaluate the Model
Our data is having fewer dimensions or features, so assuming that 1 to 2 hidden layers would work. So tried the below input to see if it gives us an expected accuracy. Also keeping in mind that increasing hidden layers would also increase the complexity of the model and choosing hidden layers such as 8, 9, or in two digits may sometimes lead to overfitting. Based on the research that I made to determine the correct number of neurons to use in the hidden layers, these are some of the points that I got. 

There are many rule-of-thumb methods for determining the correct number of neurons to use in the hidden layers, such as the following:

* The number of hidden neurons should be between the size of the input layer and the size of the output layer.
* The number of hidden neurons should be 2/3 the size of the input layer, plus the size of the output layer.
* The number of hidden neurons should be less than twice the size of the input layer.

From above I have 9 input layer  and one output layer. 2/3(9)+1 = 7, Twice the size of the input layer is 18. So tried feeding some of the combination of between 0 and 18 as the hidden neurons. 

Input:
Selected Relu activation for hidden layers and Sigmoid for the output layer. Selected 2 hidden layers with 15 and 5 neurons for each layer respectively. With 100 epochs in the training model, this gave us 746 total trainable parameters for the model. With 100 epochs for the training model, I got the below result.

![Screenshot 2021-11-11 142043](https://user-images.githubusercontent.com/81407869/141377379-1f996031-e885-491e-9f09-971f12a01389.jpg)

### Result:

Got a 73% accuracy on the above selection.

![Screenshot 2021-11-11 142102](https://user-images.githubusercontent.com/81407869/141377419-c0d72001-1ca8-41fb-9037-bd64ff316f85.jpg)


#### To achieve a better target model performance, tried to add more bins for one more column in the dataset. 
#### Tried three attempts to achieve the target of 75% or above target predictive accuracy.

Neural networks have two main hyperparameters that control the architecture or topology of the network: the number of layers and the number of nodes in each hidden layer.
Trying some random configurations of layers and nodes per layer.

### Attempt #1
Input:
Selected Relu activation for hidden layers and Sigmoid for the output layer. Selected 3 hidden layers with 7, 4 and 2 neurons for each layer respectively. This gave 395 total trainable parameters for the model. With 100 epochs for the training model, results are below. With decreasing number of neurons in each layer, 


![Screenshot 2021-11-11 142234](https://user-images.githubusercontent.com/81407869/141377567-48376c02-a247-40ce-adcd-b0a5d23088ce.jpg)

### Result of Attempt #1:

![Screenshot 2021-11-11 142250](https://user-images.githubusercontent.com/81407869/141377546-f38019bd-17b6-430d-a4c2-3c9105588aca.jpg)


### Attempt #2
Input:
Selected Tanh activation for hidden layers and Sigmoid for the output layer. Selected 2 hidden layers with 8 and 4 neurons for each layer respectively. This gave 441 total trainable parameters for the model. With 100 epochs for the training model, results are below. 


![Screenshot 2021-11-11 142443](https://user-images.githubusercontent.com/81407869/141377845-eb3e76bc-27f6-43e4-acfc-f7d4a434196d.jpg)


### Result of Attempt #2:

![Screenshot 2021-11-11 142459](https://user-images.githubusercontent.com/81407869/141377821-cf4987c6-3e22-42e6-8de5-3f8d8555d639.jpg)

### Attempt #3
Input:
Selected Tanh activation for hidden layers and Sigmoid for the output layer. Selected 3 hidden layers with 7, 5 and 3 neurons for each layer respectively. This gave 412 total trainable parameters for the model. With 50 epochs for the training model, results are below.

![Screenshot 2021-11-11 142727](https://user-images.githubusercontent.com/81407869/141378011-7ba7c7cc-5b19-4923-afd7-13a85186dd1f.jpg)


### Result of Attempt #3:

![Screenshot 2021-11-11 142720](https://user-images.githubusercontent.com/81407869/141378017-79f033f0-6344-4beb-bc6d-098fdfa59a2f.jpg)

### Summary

The model ended up with the accuracy score of 72% again after optimization. It didn't change much. The initial neural network had the accuracy score of 73%.  We can further optimize our neural network by adding more features or simply adding more data to the dataset to increase accuracy. Since our accuracy score was not particularly up to the standard with neural networks, we could have used the Random Forest classifiers. This is because random forest is a robust and accurate model due to their sufficient number of estimators and tree depth. Also the random forest models have a faster performance than neural networks. As our intented output in this particular assignment is  binary classification(whether the funding was successful or not) we can also try Logistic regression model , as its intended for binary(two-class)classification problems. 








    
