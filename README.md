# Deep Learning Challenge
Module 21 Challenge Submission by Kali Notaras

## Overview
This analysis was performed on the behalf of the nonprofit foundation Alphabet Soup, with the aim of creating a neural network model capable of selecting business applicants who will succeed if provided funding from Alphabet Soup. The model predicts the success of each applicant by taking a range of features that capture metadata about each organisation. Alphabet Soup would like this model to predict success with above 75% accuracy. 

-----------------------------------
## Results
The model utilises the variable 'IS_SUCCESSFUL' as the target value. All other variables are considered features for the model, except for the identification variables 'EIN' and 'NAME' which were removed from the imported dataset. 

With optimisation, the best accuracy score I achieved was 72.64% with both Optimisation 1 and Optimisation 3. Compared to the starter code provided, this optimisation made the following adjustments to the hyperparameters of the model:
 - Added 1 hidden layer to the neural network, for a total of 3 layers.
 - Increased the number of neurons per hidden layer, from 80/30 to 100/70/50.
 - Increasing the number of neurons and hidden layers increased the total trainable parameters from 5981 to 15071.
 - Increased the number of epochs to 150

I tried decreasing the number of categorical values in the 'APPLICATION_TYPE' variable by increasing the threshold from 500 to 1000 in Optimisation 2, but this did not cause an increase in the model's accuracy. I added 1 hidden layer to the neural network to try to increase the chance of capturing the complexity of the data and increased the number of neurons per layer to increase the accuracy of the weight coefficients. I increased the number of epochs to allow the model more training iterations with the additional hidden layer. 

In Optimisation 3, I made the additional adjustment of changing the activation function from 'ReLU' to 'Tanh'. This didn't have any impact on the accuracy of the model, so it must be a different hyperparameter that is limiting the accuracy of the model. 

-----------------------------------
## Summary
Overall, the model was not able to be optimised to significantly improve its accuracy, and it did not achieve the target model performance of 75%. A Logistic Regression model could be used to try achieve a higher predictive power/accuracy, as Logistic Regression models can intake multiple independent variables and use this data for predicting binary outcomes like our 'IS_SUCCESSFUL' outcome. It would use the same target and features as used in this neural model. 

Further optimisation techniques could look to alter the training/testing dataset split, to give the model more training data to learn from. We could also investigate the use of PCA to reduce the number of features in the dataset.

-----------------------------------
## References
IRS. Tax Exempt Organization Search Bulk Data Downloads. https://www.irs.gov/
