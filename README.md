# Neural_Network_Charity_Analysis

# Overview
Using machine learning and neural networks, we use the features in the provided dataset to help create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. A CSV is used as data source containing more than 34,000 organizations that have received funding from Alphabet Soup over the years.

Here we conducted these studies as followings.
    - Deliverable 1: Preprocessing Data for a Neural Network Model;
    - Deliverable 2: Compile, Train, and Evaluate the Model;
    - Deliverable 3: Optimize the Model.


# Results
In this analysis, the knowledge of Pandas and the Scikit-Learn’s StandardScaler() are applied to preprocess the dataset in order to compile, train, and evaluate the neural network model. Then we use TensorFlow to design a deep learning model, by assigning the number of input features and nodes for each layer using Tensorflow Keras. Then the binary classification model is set up that can predict if an Alphabet Soup–funded organization will be successful based on the features in the dataset. The model is followed by compiling and traning the binary classification model. The model’s loss and accuracy are finally calculated to evaluate the model.

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
![model_0](https://github.com/hankai26/Neural_Network_Charity_Analysis/blob/main/image/model_0.png)

    **Model Optimization: 1**
I tried to add one more hidden layers (3 in total) and different neurons as in the image to try to improve the model. The activation function for the last activation layer is also changed as "sigmoid".

![model_1](https://github.com/hankai26/Neural_Network_Charity_Analysis/blob/main/image/model_1.png)


    **Model Optimization: 2**

I increase the amount of hidden layers to 6 and more neurons, since the result in first optimization doesn't look better. The activation function is changed back to "relu" becasue it doesn't help much in last trial. Meanwhile, I increase the epochs to 200.

![model_2](https://github.com/hankai26/Neural_Network_Charity_Analysis/blob/main/image/model_2.png)


    **Model Optimization: 3**

Since the results from last two trials are not improved much. I set the number of hidden layers back to 3, but walk back to the original dataframe and further reduce more variables in selected columns. The activation function is also changed as in the following image.
![model_3](https://github.com/hankai26/Neural_Network_Charity_Analysis/blob/main/image/model_3.png)


    - The summary table for model evaluations are prepared. It indicates that the highest model loss and accuracy are 0.565936 and 0.725364, respectively.

![Sum_table](https://github.com/hankai26/Neural_Network_Charity_Analysis/blob/main/image/Sum_table.png)


    - The model is optimized in order to achieve a better predictive accuracy by using all of the following:
        a. Adjusting the input data to ensure that there are no variables or outliers that are causing confusion in the model, such as:
            - Dropping more or fewer columns.
            - Creating more bins for rare occurrences in columns.
            - Increasing or decreasing the number of values for each bin.
        b. Adding more neurons to a hidden layer.
        c. Adding more hidden layers.
        d. Using different activation functions for the hidden layers.
        e. Adding and reducing the number of epochs to the training regimen.

![Opt1](https://github.com/hankai26/Neural_Network_Charity_Analysis/blob/main/image/Opt1.png)

![Opt2](https://github.com/hankai26/Neural_Network_Charity_Analysis/blob/main/image/Opt2.png)

![Opt3](https://github.com/hankai26/Neural_Network_Charity_Analysis/blob/main/image/Opt3.png)


# Summary
The deep machine learning model cannot achieve a target predictive accuracy higher than 75% in multiple trials. The neural network model might not be the best one for this case. We can continue more trials using other models, like a logistic regression model, a classification algorithm that can analyze continuous and categorical variables. Considering the limit of features we have in our dataset, neural networks may be overcomplicated. Additionally, logistic regression models are easier to dissect and interpret than their neural network counterparts, which tends to put more traditional data scientists and non-data experts at ease.