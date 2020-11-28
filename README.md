# Neural Network Charity Analysis

## Overview

The purpose of this project is to use deep learning neural netowrk to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. For the purpose of this project, we will use a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. This dataset contains a number of columns that capture metadata about each organization.

## Results

- **Data Preprocessing**  
For the initial model, data preprocessing included removing variables that were irrelevent for the model such as the identifier, grouping/binning variables that had skewed distribution.  
**Target:** The "IS SUCCESSFUL" column is considered the target for this model  
**Features:** APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT columns are considered as features for the model  
**Neither Targets nor Features:** EIN and NAME columns are considered neither targets nor features, and are removed from the input data
- **Compiling, Training, and Evaluating the Model**  
**Layers:** There are 2 hidden layers, one input layer and an output layer for the intial model  
**Neurons:** There are 80 neurons in the first hidden layer and 30 neurons in the second hidden layer  
**Activation Functions:** The hidden layers use "RELU" activation function and the output layer uses "Sigmoid" activation function  
- **Optimizing**  
**Data Preprocessing:** The "INCOME_AMT" column has a lot of zero's. This column was dropped from the dataset. In the "ASK_AMT" column, most of the values were $5000. The data in this column were grouped into standarad (=5000) and high (>5000) values. The original column was then dropped from the dataset.  
**Model:** Initially, the number of neurons and the hidden layers were increased in the model, ti increase the accuracy. However this caused the model to overfit and resulted in lower accuracy. The hidden layer was then reduced to 1 and the neurons were reduced. This increased the model accuracy to 71.4%  

## Summary

The original accuracy of the deep learning model was 53.3% as shown below
![original](https://github.com/ssathyanath/Neural_Network_Charity_Analysis/blob/main/Images/Original_Accuracy.PNG)

After optimizing the accuracy improved to 71.4% as shown below
![optimized](https://github.com/ssathyanath/Neural_Network_Charity_Analysis/blob/main/Images/After_Optimizing.PNG)

Using deep learning model with more neurons and layer caused the model to overfit. Using a basic neural network with one hidden layer and less neuron caused the model to perform better. This suggest, that a simpler model like Support Vector Machine would be better for this project.