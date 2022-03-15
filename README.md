# Neural_Network_Charity_Analysis
## Project Overview
Alphabet Soup’s business team has provided us with a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. In this project we use our knowledge of machine learning and neural networks along with the features in the provided dataset to assist in creating a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

## Resources
- Data Source: [charity_data.csv](https://github.com/Reed-Daniel/Neural_Network_Charity_Analysis/blob/main/charity_data.csv)
- Software: Python, VS Code

## Results
### Data Preprocessing
- The column `IS_SUCCESSFUL` is a target variable as it contains binary data refering to whether or not the charity donation was used effectively. 
- The columns `APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT` are the features for our model.
Encoding of the categorical variables, spliting into training and testing datasets and standardization have been applied to the features.
- The columns `EIN` and `NAME` are identification information and have been removed from the input data.

### Compiling, Training, and Evaluating the Model
- This deep-learning neural network model is made of two hidden layers with 80 and 30 neurons respectively.
- The input data has 43 features and 25,724 samples.
- The output layer is made of a unique neuron as it is a binary classification.
- To speed up the training process, the activation function `ReLU` was used for the hidden layers. As our output is a binary classification, a `Sigmoid` activation function was used on the output layer.
- For the compilation, the optimizer is `adam` and the loss function is `binary_crossentropy`.
- The accuracy of the model is under 75% which is sub-par performance in determing if the foundation's investment is effective.
- To increase the performance of the model, bucketing was applied to the feature `ASK_AMT` and the different values were organized by intervals.
- The number of neurons on one of the hidden layers were increased and then a model with three hidden layers was used.
- Different activation functions (`tanh`) were tested but none of these steps helped improve the model's performance.

### Summary
The neural network model we created did not reach the target accuracy score **(75%)**. Given the moderate/low performance of the model, it would not be suggested to be used in AlphabetSoup's research in regards to their charitable investments. A possible recommendation would be to use a supervised machine learning model such as the Random Forest Classifier to combine multiple decision trees to generate a classified output and evaluate its performance against our deep learning model.
