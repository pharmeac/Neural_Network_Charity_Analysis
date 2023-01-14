# Neural_Network_Charity_Analysis

## Overview 
The purpose of this analysis was to create a model to help the foundation predict where to make investments, using data from more than 34,000 organizations that have received funding from Alphabet Soup over the years. 

## Results 
### Data Preprocessing
 - Target variable(s) for the model: The IS_SUCCESSFUL data was used as the target variable in this model
 - Feature variable(s) for the model: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, SPECIAL_CONSIDERATIONS.
 - Variable(s) removed (not targets nor features): EIN, NAME, ASK_AMT

### Compiling, Training, and Evaluating the Model
 - For the first attempt at optimizing the model I kept the neurons, layers, and activation functions the same, so that I could try to narrow in on what facters impacted the accuracy.
   - First hidden layer
      - 80 neurons
      - ReLu activation
   - Second hidden layer
      - 30 neurons
      - ReLu activation
 - Target model performance:
   - Accuracy 68.5%, loss 2.16
   - After callback optimization (after 5 epochs): Accuracy 72.3%, loss 0.56
 - On the second attempt to optimize the model, I added nodes to the first hidden layer (total 140 nodes)
   - Accuracy 64.7%, loss 3.2
   - After callback optimization (after 5 epochs): Accuracy 72.3%, loss 0.56
 - On the third attempt to optimize the model, I added another hidden layer (10 nodes) and change the activation functions of the hidden layers (tanh)
   - Accuracy 70.5%, 0.61
   - After callback optimization (after 5 epochs): Accuracy 72.4%, loss 0.55
 
 ![image](https://user-images.githubusercontent.com/109913335/212482085-51a1d800-40e0-4c08-ac3a-d36c20c2ea5a.png)


## Summary
I was not able to achieve the target model performance of 75% accuracy. We ended up with a model that achieved 72.4% accuracy. A different model, that bins the ASK_AMT instead of removing it may improve the model. Additionally, a ratio of income to ask amount may also improve the model.


