# Neural Network Charity Analysis
## (Module 19 Challenge)

#
## Overview
We are helping Beks to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.

#
## Results
<!-- EIN and NAME—Identification columns
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special consideration for application
ASK_AMT—Funding amount requested
IS_SUCCESSFUL—Was the money used effectively -->

### Data Processing
1. Variable(s) considered the target
    1. IS_SUCCESSFUL - This suggests if the investments were effective & successful.

1. Variable(s) considered to be the features
    1. AFFILIATION — Affiliated sector of industry
    1. CLASSIFICATION — Government organization classification
    1. USE_CASE — Use case for funding
    1. ORGANIZATION — Organization type
    1. STATUS — Active status
    1. INCOME_AMT — Income classification
    1. SPECIAL_CONSIDERATIONS — Special consideration for application
    1. ASK_AMT — Funding amount requested
1. Variable(s) we removed since these did not add value
    1. EIN and NAME — Identification columns

### Compiling, Training, and Evaluating the Model
1. How many neurons, layers, and activation functions did you select for your neural network model, and why?
    1. To start with we selected 2 layers with 80 and 30 neurons respectively.
    ![](https://github.com/neerajain9/Neural_Network_Charity_Analysis/blob/Data-Science/Resources/base%20model_neuron%20selction.png?raw=true)
    
        1. We kept the number of neurons in the first layer to be twice the size of trained input variables. We then selected second layer to be approx. 40% of the first layer to achieve reasonable performance.
        1. We chose 2 layers since we figured the data to be a bit complicated and reasonable in size.Adding an extra layer would justify the use of the entire dataset with more appropriate individual weighing of the components.
    1. We chose ReLU activation group due to its property of simplifying outputs. Plus ReLU is most widely used activation group.


1. Were you able to achieve the target model performance?
    1. We **could not achieve the target model performance**. We made many attempts but recorded only 3 for the challenge.
    ![](https://github.com/neerajain9/Neural_Network_Charity_Analysis/blob/Data-Science/Resources/optimization%201.png?raw=true)
    ![](https://github.com/neerajain9/Neural_Network_Charity_Analysis/blob/Data-Science/Resources/optimization%202.png?raw=true)
    ![](https://github.com/neerajain9/Neural_Network_Charity_Analysis/blob/Data-Science/Resources/optimization%203.png?raw=true)



1. What steps did you take to try and increase model performance?
    1. We tried to reduce the number of features that could possibly be producing noise.
    1. We changed the number of neurons to 3 times the number of trained input variables.
    ![](https://github.com/neerajain9/Neural_Network_Charity_Analysis/blob/Data-Science/Resources/optimized%20model_neuron%20selction.png?raw=true)

    1. Added an additional layer though we weren't a big follower of it in this case. We intended to achieve the desired accuracy using two layers.
    1. We played around altering the number  (between 50 and 200) of epochs.
    1. Also, we tried replacing "ReLU" with "tanh" acivation group for its sophistication reasons.
    1. we used checkpoints to reuse the trained model and added callback to save after every 5 epochs.

## Summary
We felt challenged in optimizing the ML model and weren't successful in achieving the desider accuracy.

Considering the size of the data, not that big though, it was a bit time consuming process. We thought of trimming the data to half its size to achieve the model accurancy and then apply the same on the full data set. Doing this might have created other unexpected issues like overfitting due to uneven data selection, and many more that we are not even aware of.

Our first model design is our best so far and our only **[recommendation](https://github.com/neerajain9/Neural_Network_Charity_Analysis/blob/Data-Science/Resources/optimization_Original.png)**.


![](https://github.com/neerajain9/Neural_Network_Charity_Analysis/blob/Data-Science/Resources/optimization_Original.png?raw=true)