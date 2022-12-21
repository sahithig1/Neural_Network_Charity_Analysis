# Neural_Network_Charity_Analysis

## Overview of the Analysis 
Using Machine Learning and Neural Networks for this project, I used the features in the dataset to create a binary classifier that will help to predict if the applicants that will be funded by a Charitable organization called Alphabet Soup will be successful. For this analysis we had a dataset containing various measures on 34,000 organizations that have been funded by Alphabet Soup. This project compromised of the following 3 steps: 
- Preprocessing the data for the neural network 
- Compile, Train and Evaluate the Model 
- Optimizing the model

## Results 

### Data Preprocessing 
- Variable that was considered as the target for my model: IS_SUCCESSFUL Column
- Variables that were considered features for my model: Every Column except for IS_SUCCESSFUL which is our target and the ones we will drop
- Variable that were neither targets or features for the dataset: Columns that I dropeed are EIN, NAME because they will have little to no impact om our outcome

### Compiling, Training and Evaluating the Model

The number of neurons, layers, and activation functions I selected for my neural network model:
- For my neural network model I had 2 hidden layers. My first layer had 80 neurons, the second has 30 there is also an output layer. The first and second hidden layer have the "relu" activation function and the activation function for the output layer is "sigmoid."

<img width="645" alt="1st Summary" src="https://user-images.githubusercontent.com/55648656/208982495-644a84c6-222a-48dd-86de-8814be155238.png">


Was the model able to achieve the target model performance?
- The model was not able to reach the target 75%. The accuracy for my model was 69%.

<img width="660" alt="1st accuracy" src="https://user-images.githubusercontent.com/55648656/208982527-891e83c3-ec18-4466-ad3a-3edc31a27b14.png">


The steps taken to try and increase model performance

- Attempt 1: Removed additional feature, that is the 'USE_CASE' column. Rest of the model components stayed the same, however model accuracy went down to 63%. 

<img width="646" alt="Attempt 1 change" src="https://user-images.githubusercontent.com/55648656/208982557-11736093-d7fd-48e1-b985-baf6602fe258.png">

<img width="657" alt="Attempt 1 accuracy" src="https://user-images.githubusercontent.com/55648656/208982615-08e78834-4c95-4ca7-a340-5fbca48318dc.png">


-  Attempt 2: Adding Additional neurons to hidden layers and additional hidden layers are added. The accuracy went down again, this time it was 53%.

<img width="649" alt="Attempt 2 change" src="https://user-images.githubusercontent.com/55648656/208982680-9ae9ae86-b0a2-4af0-9270-0f5d7e4ff50b.png">

<img width="659" alt="Attempt 2 accuracy" src="https://user-images.githubusercontent.com/55648656/208982709-24c8e906-cd30-4a34-8c55-248d76f4bc27.png">

- Attempt 3: Changing activation function of output layer from "sigmoid" to "tanh." The accuracy of the model went down even more to 50%.

<img width="653" alt="Attempt 3 change" src="https://user-images.githubusercontent.com/55648656/208982896-2f5b1d7c-28ee-480c-b259-e6b6d1ebb384.png">

<img width="644" alt="Attempt 3 accuracy" src="https://user-images.githubusercontent.com/55648656/208982921-1b22add0-7db0-4422-9003-e998ae4978fd.png">


## Summary 

The model ended up with the accuracy score of 45% after optimization. The initial neural network had a accuracy score of 73%. This loss in accuracy can be explained from the fact that the model overfitted. Furthermore, we could further also optimize our neural network by removing more features or simply adding more data to the dataset to increase accuracy.

Since our accuracy score was not particularly up to the standard with neural networks, we could have used the Random Forest classifiers. This is because random forest is a robust and accurate model due to their sufficient number of estimators and tree depth. Also the random forest models have a faster performance than neural networks and could have avoided the data from being overfitted. 
