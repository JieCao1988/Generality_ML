# Generality_ML
This work aims to evaluate the generality of machine learning models for ROP prediction.

For data splitting, we choose designated training+validation and hold unseen testing datasets. 

In the well scale, we assume that the bit is at a certain point of depth. The data of drilled portion is assigned to the training and validation (with radom split into 70 and 30%, respectively) and a small undrilled portion ahead of the bit. 

In field scale, we train and validate a model using a number of wells, assuming as drilled wells, and test it on a new well, which is assumed as undrilled well. Furthermore, we use data from a number of drilled well and the drilled portion of the well under investigation for training and validation, and testing on a further portion of the investigated well ahead of the current bit position. Here, a continuous learning structure is proposed as the data dynamically accumulating and model continuously updating

(TBD) Lastly, we propose to train models based on different formations and validate the model generality.

For ML models, we choose a number of most commonly used ML models, including Random forest, AdaBoosting, KNN, for investigations. The automatic hyperparameter tuning is called when the R2 for training is lower than 0.99. 
