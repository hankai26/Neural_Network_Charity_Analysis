# Neural_Network_Charity_Analysis

# Overview
Using machine learning and neural networks, we use the features in the provided dataset to help create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. A CSV is used as data source containing more than 34,000 organizations that have received funding from Alphabet Soup over the years.

Here we conducted these studies as followings.
    - Deliverable 1: Preprocessing Data for a Neural Network Model;
    - Deliverable 2: Compile, Train, and Evaluate the Model;
    - Deliverable 3: Optimize the Model.


# Results
In this analysis, the knowledge of Pandas and the Scikit-Learn’s StandardScaler() are applied to preprocess the dataset in order to compile, train, and evaluate the neural network model. Then we use TensorFlow to design a deep learning model, by assigning the number of input features and nodes for each layer using Tensorflow Keras. Then the binary classification model is set up that can predict if an Alphabet Soup–funded organization will be successful based on the features in the dataset. The model is followed by compiling and traning the binary classification model. The model’s loss and accuracy are finally calculated to evaluate the model.

Further, the model is optimized in order to achieve a better predictive accuracy by using all of the following:
    - Adjusting the input data to ensure that there are no variables or outliers that are causing confusion in the model, such as:
        - Dropping more or fewer columns.
        - Creating more bins for rare occurrences in columns.
        - Increasing or decreasing the number of values for each bin.
    - Adding more neurons to a hidden layer.
    - Adding more hidden layers.
    - Using different activation functions for the hidden layers.
    - Adding and reducing the number of epochs to the training regimen.

1. Data Preprocessing
    - Multiple non-benefit columns are removed and not used as target and feathers:
        - EIN
        - NAME
        - SPECIAL_CONSIDERATIONS
    Different trials are tested to determine the final amount of feathers to train the model.
    
    - The column "IS_SUCCESSFUL" is used as the target for the model.

    - All other columns in the dataset except both non-benefit columns and target are considered to be the features.


2. Compiling, Training, and Evaluating the Model
    - Different neurons, layers, and activation functions are selected for neural network model in multiple trials.

    **Original Model**


    **Model Optimization: 1**



    **Model Optimization: 2**



    **Model Optimization: 3**


    **Model Optimization: 4**



    - The summary table for model evaluations are prepared. It indicates that the highest model accuracy is 
    


    - What steps did you take to try and increase model performance?



# Summary: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation