# Neural_Network_Charity_Analysis

### Overview of the analysis
Using neural networks, this analysis has been performed to help the Alphabet Soup foundation predict where to make investments.
#
A binary classifier is created with the features in the provided dataset to help predict whether applicants will be successful if funded by Alphabet Soup.
#
A CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years is used. Within this dataset are a number of columns that capture metadata about each organization including:
* EIN and NAME—Identification columns
* APPLICATION_TYPE—Alphabet Soup application type
* AFFILIATION—Affiliated sector of industry
* CLASSIFICATION—Government organization classification
* USE_CASE—Use case for funding
* ORGANIZATION—Organization type
* STATUS—Active status
* INCOME_AMT—Income classification
* SPECIAL_CONSIDERATIONS—Special consideration for application
* ASK_AMT—Funding amount requested
* IS_SUCCESSFUL—Was the money used effectively
#
### Deliverable 1
#
#### Data Preprocessing
* What variable(s) are considered the target(s) for your model?
The target is the column  IS_SUCCESSFUL
* What variable(s) are considered to be the features for your model?
APPLICATION_TYPE             
AFFILIATION                  
CLASSIFICATION               
USE_CASE                     
ORGANIZATION                 
STATUS                       
INCOME_AMT                   
SPECIAL_CONSIDERATIONS       
ASK_AMT                   
#
* What variable(s) are neither targets nor features, and should be removed from the input data?
EIN and NAME in round 1, EIN in round 2
#
### Deliverable 2
#
#### Compiling, Training, and Evaluating the Model
* How many neurons, layers, and activation functions did you select for your neural network model, and why?
#
##### First Round - used deep learning example from lessons
* Layer 1 - 80 activation relu
* Layer 2 - 30 activation relu
* Output Layer - 1 activtation sigmoid
#
![r1](https://github.com/jcsargis00/Neural_Network_Charity_Analysis/blob/main/Resources/round1.PNG)
#
##### Second Round to improve accuracy - changed # neurons, added layer, changed activation, looked at name feature, where applicant had applied for a loan more than 5 times
Layer 1 - 100 activation relu
Layer 2 - 30 activation Sigmoid
Layer 3 - 10 activation Sigmoid
Output Layer 1 activation Sigmoid
#
![r2](https://github.com/jcsargis00/Neural_Network_Charity_Analysis/blob/main/Resources/round2.PNG)
* Were you able to achieve the target model performance?
#
Yes
* What steps did you take to try and increase model performance?
#
I tried all of the suggestions.  I found success by adding a third layer, adding more neurons, binning name in addition to application, and changing the activations for the 2nd and 3rd layer to sigmoid.  I also increased the number of epochs from 50 to 150.
#
#### Summary of the results 
The model was optimized by modifying each of the following:
- Adjusting the input data to ensure that there are no variables or outliers that are causing confusion in the model, such as:
* Dropping more or fewer columns.
* Creating more bins for rare occurrences in columns.
* Increasing or decreasing the number of values for each bin.
* Adding more neurons to a hidden layer.
* Adding more hidden layers.
* Using different activation functions for the hidden layers.
* Adding or reducing the number of epochs to the training regimen.
The model returned a better result after changing the activation function to sigmoid for the hidden layer.
#
#### Recommendation for how a different model could solve this classification problem, and explain your recommendation.
Random Forest Deep Learning algorithm is well suited for this problem and returned a similar accuracy result while being much easier and faster to set up and run. Deep Learning had 78.88% accuracy while Random Forest had 77.76% accuracy.
![nnets](https://github.com/jcsargis00/Neural_Network_Charity_Analysis/blob/main/Resources/models.PNG)