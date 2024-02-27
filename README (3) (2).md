# deep-learning-challenge

## Neural Network Model Report
1. **Overview of the analysis:** The following analysis examines a dataset of organizations that have received funding from a nonprofit, Alphabet Soup, and whether or not their particular venture had success. We are applying deep learning methods to help Alphabet Soup determine which of the organizations are most likely to be successful, predicting the outcome before Alphabet Soup grants the funding. 
   
3. **Results:** Using bulleted lists and images to support your answers, address the following questions:
- Data Preprocessing
  - What variable(s) are the target(s) for your model?
    - The target for this model is the column "IS_SUCCESSFUL", that identifies whether the money was used effectively and if the venture had success. 
  - What variable(s) are the features for your model?
    - The features are the variables which we are using to predict the target outcome. Included in this are all columns excluding the identification columns ("NAME" and "EIN"). "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "STATUS", "INCOME_AMT", "SPECIAL_CONSIDERATIONS", "ASK_AMT" are all applicable columns, though in the optimization phase I tried dropping "SPECIAL_CONSIDERATIONS". "USE_CASE", "SPECIAL_CONSIDERATIONS", and "ASK_AMT" refer to the grant application, while the other variables center on the organization making the request. 
  - What variable(s) should be removed from the input data because they are neither targets nor features?
    -The Variables that are to be removed include the identification columns, "EIN" and "NAME".
- Compiling, Training, and Evaluating the Model
  - How many neurons, layers, and activation functions did you select for your neural network model, and why?
    - I used 5 neurons, because its between the output layer (1) and input dimension (number of columns in the X_train dataset). I used two hidden layers and one output layer, with "relu" and "sigmoid" functions respectively.
  - Were you able to achieve the target model performance?
    - No. I was unable to achieve target performance. 
  - What steps did you take in your attempts to increase model performance?
    - For  optimization, I tried dropping an additional column, while adding an "Other" bin for "ASK_AMT", which increased the number of hidden layers from two to three, and increased the number of nodes from 5 to 10 and then to 16 for the first layer. The highest accuracy score came from using two hidden layers with nodes 16 and 10 respectively, both dropped columns, and hard cutoffs for the classifications binning.
3. **Summary:** Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and then explain your recommendation.
  Overall, the optimization model could predict success for an organizations application for funding correctly most of the time. Despite the fact that the optimization attempts weren't successful, I still feel that increasing nodes with increasing the layers is likely to have a good outcome due to the added complexity of the model. Also, improving the quality or amount of training data can also lead to a more accurate model
