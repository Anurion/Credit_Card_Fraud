# Credit_Card_Fraud
Practice Machine Learning Skills

## Sources
The dataset was taken from the kaggle website https://www.kaggle.com/mlg-ulb/creditcardfraud.

## Preprocessing
The data can be called ideal, because all values are numeric, there are many parameters, the correlation matrix clearly shows which of them most affect our target. It was decided to remove columns whose correlation with the target column was less than 0.01, because they just created noise for our model.

## Building the model
As a basis, as in most of my work, XGBoost was taken. It immediately showed good results, and by adjusting the parameters it was possible to improve them a little more.

###Stacking
For a long time I wanted to implement this approach in machine learning, and now the time has come :) Classical models were taken as the basis: Logistic regression, Support vector machine, Decision tree and Nearest neighbors. I also tuned these models manually before writing them to the StackingClassifier to get the best result. My favorite XGBoost was taken as a meta-model, I configured its parameters already in the course of training stacked_model.

## Results
Overall, I'm satisfied with the result in Roc_Auc ~0.91 and F1_score ~0.89. Although, of course, I would like to better tune the parameters, for example, using Bayesian optimization.
In future works, I hope to be able to apply it.

Thanks for reading, I hope this was as helpful to you as it was to me!
