# Marketing Campaign
 ### :paperclip: This repository contains all the files inherent in a marketing campaign analysis project. One file contains the dataset used for the analysis, another     file the R-language code, and finally, a file with the final report written by yours truly.

### Goal 🎯
The purpose of of this paper is to identify the success of a marketing campaign in terms of actual users acquired, that is, those who actually signed up for the  contract proposal. They are also present personal delucidations and considerations aimed at improving the final results. In light of the intended objective,
it is believed that the implementation of a model of logistic regression is appropriate to obtain the desired information.

### Dataset 📊
The dataset consists of 41,188 records and 19 features that are very varied and informative, categorical and continuous, with little correlation between them.
only some of them were taken into account for the analysis.

### Preliminary Exploratory Analysis :mag:
In preliminary exploratory analysis, we checked for null values and plotted several graphs with the ggplot2 library. Finally, we created a correlation analysis between variables and eliminated those that were highly correlated with each other.

### Logistic Regression :chart_with_upwards_trend:
To identify the most significant variables to be used in the logistic regression model, we proceeded with a stepwise selection on the basis of the lowest AIC value. The results of this selection make it possible to eliminate insignificant variables, so that the model is created with only the highly qualifying variables.
Next, the analysis involves creating the training set consisting of approximately 28,000 records and using the latter to train a logistic regression model, using both the link 'logit' and the 'probit' link as hyper-parameters, with roughly similar results, with some variation regarding the significance of the individual coefficients.

The confusion-matrix on the test-set shows that the model is able to predict well the cases of failure, while some difficulty occurs when trying to predict successful cases. The model predicts well 11,000 cases out of about 12,000, the accuracy is 89%, but at the same time the specificity is 19%, which means that the model does not predict well the success cases, that is, the cases in which the customer subscribes to the offered contract. In contrast, the sensitivity calculation shows how the 
model achieves a 98% prediction of failure cases.
These results are obtained with a theshold of 0.56. what happens if you reduce or increase theshold? 
Reducing theshold to 0.2 slightly reduces accuracy to 85% but at the same time, increases specificity significantly to 56%. If the goal was to correctly predict those who have actually signed the contract, it is recommended to set a low threshold, more towards to zero.
Analyzing the results obtained, we assume that a theshold lower than 0.5, can improve significantly the ability of our model to predict the users who actually signed the contract.

For more information regarding the interpretation of the results, please read the final report.
