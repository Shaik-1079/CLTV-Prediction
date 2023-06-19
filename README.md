# CLTV-Prediction
## Problem Statement :


## Approach
   ### First Step: Perform EDA on the Training Data
      We notice that claim_amount is RIGHT SKEWD so we can apply Log transformation to normalize it 
      Ordinal and One hot encoding can be used for some columns  
   ### Second Step: Perform the necessary data transformations
      (pd.get_dummies) for One Hot encoding
      (.map()) for Ordinal encoding
      (numpy.log2()) for log transformation 
   ### Third Step: Split the data in train and val split using test train split 
   ### Fourth Step: 
