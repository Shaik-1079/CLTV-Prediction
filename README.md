# CLTV-Prediction
## Problem Statement :
   VahanBima is one of the leading insurance companies in India. It provides motor vehicle insurances at best prices 
   with 24/7 claim settlement. It offers different types of policies for both personal and commercial vehicles. It 
   has established its brand across different regions in India.

   Around 90% of the businesses today use personalized services. The company wants to launch different personalized 
   experience programs for customers of VahanBima. The personalized experience can be dedicated resources for 
   claim settlement, different kinds of services at doorstep, etc. Inorder to do so, they would like to 
   segment the customers into different tiers based on their customer lifetime value (CLTV).

   Inorder to do it, they would like to predict the customer lifetime value based on the activity and interaction of 
   the customer with the platform. So, as a part of this challenge, your task at hand is to build a high performance 
   and interpretable machine learning model to predict the CLTV based on the user and policy data.

## Approach
   ### First Step: Perform EDA on the Training Data
      No Null values in data ^_^
      We notice that claim_amount is RIGHT SKEWD so we can apply Log transformation to normalize it 
      Ordinal and One hot encoding can be used for some columns  
   ### Second Step: Perform the necessary data transformations
      (pd.get_dummies) for One Hot encoding
      (.map()) for Ordinal encoding
      (numpy.log2()) for log transformation 
   ### Third Step: Split the data in train and val split using test train split 
      from sklearn.model_selection import train_test_split
   ### Fourth Step: Model Training 
      import various models to train your data in my case I have used gradient boost regressor and cat boost regressor
      
      from sklearn.ensemble import GradientBoostingRegressor
      import catboost as cb
      cb.CatBoostRegressor() 
   ### Fifth Step: Hyper-Parameter Tuning
      Hyperparameter tuning can be done in two ways one of which is hard way by understanding the data and checking multiple 
      parameters values for providing good performance on the data
      The other way is using algorithms like  Random search CV and Grid search CV to auto-tune the hyperparameters
      I implemented a grid search CV to look for the  best parameters suitable for data
   ### Sixth Step: Make Predictions
   ### Seventh Step: Evaluate your model
      Eval metric to be used is R2 
