# CLTV-Prediction
## Problem Statement :


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
   ### Fifth Step: Hyper Parameter Tuning
      Hyper parameter tuning can be done in two ways one of which is hard way by understanding the data and checking multiple parameters values for providing a good performance on the data 
