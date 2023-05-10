# Alphabet Soup Charity Applicant Funding Model Report
By: Kiana Navarre

## Overview 
For this project, the nonprofit foundation Alphabet Soup is requesting a tool that can help select applicants for funding given the best chance of success in their ventures.  The CSV file recieved from the Alphabet Soup team contains more than 34,000 organizations that have previously recieved funding.  For each of these records the following data is included: 
    * Organizaiton Name
    * Alphabet Soup application type 
    * Affiliated sector of industry 
    * Government organization classification 
    * Use case for funding 
    * Active status 
    * Income classification 
    * Special considerations for application 
    * Funding amount requested 
    * Was the money used effectively 

The deliverable for this project is to create a neural network model with an accuacy percentage of greater that 75%. 

## Results
Data Preprocessing 
* Target Variable for Model: IS_SUCCESSFUL 
  * Variable defining if the funding was successful and the money was used effectively
* Feature Varables for Model: 
  * APPLICATION_TYPE
  * AFFILIATION
  * CLASSIFICATION
  * USE_CASE
  * ORGANIZATION
  * INCOME_AMT
  * SPECIAL_CONSIDERATIONS
* Removed Variables: EIN and NAME 
  * These variables were removed as they were neither target nor feature variables. 


Compiling, Training, and Evaluating the Model

Initial Model 
  * Layers: 
    * 2 hidden layers
    * 1 output layer
  * Neurons: 
    * Hidden Layer 1: 80
    * Hidden Layer 2: 30
    * Output Layer: 1 
  * Activation function(s): 
    * hidden layers: 'relu' 
    * output layer: 'sigmoid'
  * Epochs: 100

  ![alt text](https://github.com/knavarre/deep-learning-challenge/blob/main/images/initial_model.PNG?raw=true)
  * Model Loss: 0.5568
  * Model Accuracy: 0.7286

  ![alt text](https://github.com/knavarre/deep-learning-challenge/blob/main/images/initial_model_accuracy.PNG?raw=true)

Optimized Model
  * Layers: 
    * 3 hidden layers
    * 1 output layer
  * Neurons: 
    * Hidden Layer 1: 16
    * Hidden Layer 2: 16
    * Hidden Layer 3: 16
    * Output Layer: 1 
  * Activation function(s): 
    * hidden layers: 'relu' 
    * output layer: 'sigmoid'
  * Epochs: 50

  ![alt text](https://github.com/knavarre/deep-learning-challenge/blob/main/images/optimized_model.PNG?raw=true)
  * Model Loss: 0.5508
  * Model Accuracy: 0.7287

  ![alt text](https://github.com/knavarre/deep-learning-challenge/blob/main/images/optimized_model_accuracy.PNG?raw=true)

When attempting to optimize the model, the model continued to hover at an accuracy of ~72%.  The following steps were taken to attempt to increase the models accuracy percentage: 
  * Increase the number of hidden layers 
  * Decrease the number of neurons 
  * Decrease the number of epochs used to train the model

Following the model optimization, the deliverable of an accuracy percentage greater than 75% was not achieved, and there is a negligable increase in the accuracy percentage of the Optimized Model (72.87%) compared to the Initial Model (72.83%). 

## Summary
Both the initial and the optimized neural network models that were created had an accuracy percentage of ~72.8%.  Adjusting the number of hidden layers, adjusting the number of neurons, and decreasing the number of epochs used to train the model did not appear to significantly affect the accuracy of the model.  Thus the final deliverable was not achieved as the model accuracy continued to hover around 72%.   

Future considerations to increase the model's accuracy percentage may include excluding features or gathering additional data.  Ultimately gathering more data woud help the model more significantly, but in the case where this is not possible, it may be beneficial to narrow the scope of the model by decreasing the number of features considered. 