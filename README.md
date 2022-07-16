# Generality_ML
This works aims to evaluate the generality of machine learning models for ROP prediction.

In general, the proposed models are mostly with high accuracy with given dataset, while may not be applicable to other wells outside the dataset. This means that the generality of the model is not well validated, resulting in less persuasive and not useful models.
The cross evaluation is implemented in well scale and in field scale to validate the generality of ML models for ROP prediction.

For data splitting, we choose designated training+validation and unseen testing datasets. 
In the well scale, we assume that the bit is at a certain point of depth. The data of drilled portion is assigned to the training and validation (with radom split into 70 and 30%, respectively) and a small undrilled portion ahead of the bit. 
In field scale, we train and validate a model using a number of wells, assuming as drilled wells, and test it on a new well, which is assumed as undrilled well. Furthermore, we use data from a number of drilled well and the drilled portion of the well under investigation for training and validation, and testing on a further portion of the investigated well ahead of the current bit position. Here, a continuous learning structure is proposed as the data dynamically accumulating and model continuously updating
Lastly, we propose to train models based on different formations and validate the model generality.

For models, we choose a number of most commonly used ML models, including Random forest, AdaBoosting, KNN, for investigations.
