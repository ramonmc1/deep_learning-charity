# deep_learning-charity Report

1. Overview:
    The purpose of this project is to create an algorithm to predict whether or not
    applicants for funding will be successful. We created a binary classifier that is capable of 
    predicting whether applicants will be successful if funded by Alphabet Soup using neural 
    networks. A dataset with over 34,000 organizations was used to create the predictive model.

2. Results: 

  * Data Preprocessing
    * The train and test feature was the "Is Successful" (Yes/No) infromation from the dataset
    * Several variables were used as features to create the model. These are listed below:
         - APPLICATION_TYPE        
         - AFFILIATION             
         - CLASSIFICATION          
         - USE_CASE                
         - ORGANIZATION            
         - STATUS                  
         - INCOME_AMT              
         - SPECIAL_CONSIDERATIONS  
         - ASK_AMT    
    * The following variable(s) did not add value to the predictive features of the model and were removed:
         - EIN
         - NAME
         
  * Compiling, Training, and Evaluating the Model
    - Several combinations were used to achieve the highest accuracy and minimize the loss. Although a 75 percent was not achieved, the best combination of layers, neurons and activation functions are listed below.
    * neurons:50 for all layers
    * layers: 8 hidden layers and 1 output layer
    * activation functions: ReLU for activation, Sigmoid for output layer
    *100 Epochs
    * Model perfromance: The model achieved a 73 percent accuracy with 0.54 loss.
        * Steps taken to increase model performance:increased the number of neurons (10-50 per layer), number of hidden layers(3-8)and tried different ReLu, LeakyReLU and Tanh activation functions. Also, outliers in 'Ask_Amount' were removed (above 1e9).
    
3. Summary: 

Overall, the model has an 73 percent accuracy. Multiple changes to number of neurons, layers, epochs and removal of ouliers did not significantly increase the model accuracy. Another method such as logical regression or RandonForest could have been used to predict how succesful an applicant for funding would be. A comparison of these models would also be beneficial. 
