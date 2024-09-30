# American Express Exit Prediction Using Artificial Neural Network (ANN)
This project aims to predict whether a customer will leave the services of American Express by utilizing an Artificial Neural Network (ANN). 
The model is developed using TensorFlow and Keras and trained on customer data to classify the likelihood of customer churn.

## Installation
To run this project, you need to have Python installed, along with the following required libraries:

1. numpy for numerical computations
2. pandas for handling data structures
3. tensorflow for building and training the ANN model
4. scikit-learn for data preprocessing and metrics

## Dataset
The data is loaded from an Excel file that contains customer-related information. The target variable represents whether a customer is predicted to leave the service. 
The dataset includes various features such as customer demographics, account balances, and more.

## Data Preprocessing
1. Dividing the data
The dataset is divided into features (X) and the target variable (y), where X represents all input features and y represents the output labels (whether the customer exits).

2. Label Encoding
Some categorical variables need to be label-encoded. For example, a column (such as gender or customer type) is converted into numerical labels using LabelEncoder from scikit-learn.

3. One-Hot Encoding
The categorical features are transformed using One-Hot Encoding to handle non-numerical columns. The ColumnTransformer and OneHotEncoder classes from scikit-learn are used to achieve this.

4. Feature Scaling
Standardization is applied to the numerical features using StandardScaler to ensure that all variables contribute equally to the model training.
This is necessary for the convergence of gradient-based learning algorithms like neural networks.

5. Train-Test Split
The data is split into training and testing sets, with 80% used for training and 20% for testing

## Building the ANN
The ANN is built using TensorFlow's Keras API. It includes two hidden layers and one output layer.

1. ANN Initialization
A Sequential model is initialized to add layers sequentially.

2. Input Layer
The input layer accepts 11 features based on the dataset.

3. Hidden Layers
Two dense layers are added, each with 5 units and a ReLU activation function.

4. Output Layer
The output layer is a dense layer with 1 unit and a sigmoid activation function, which is used for binary classification (customer exit prediction).

## Compiling and Training the Model
The model is compiled with the Adam optimizer and binary cross-entropy loss function. The accuracy metric is used to evaluate the model's performance during training.

## Making Predictions
After training, predictions are made on the test set. The predicted probabilities are converted to binary outcomes (1 for "exit", 0 for "not exit") based on a threshold of 0.5.

## Model Evaluation
The model's performance is evaluated using the following metrics:

1. Confusion Matrix
A confusion matrix is generated to visualize the performance of the model in terms of correct and incorrect classifications.

2. Accuracy Score
The accuracy score is calculated to determine the overall accuracy of the model's predictions.

## Conclusion
This project demonstrates how to build an ANN model for predicting customer churn using structured data.
By preprocessing the data, creating an appropriate network architecture, and evaluating its performance, we can effectively predict customer exit behavior with a decent level of accuracy.
