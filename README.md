# Neural_Network_Charity_Analysis
Module 19: Neural Networks and Deep Learning Models

## Overview of the analysis

In this week's challenge, the student helps Beck create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. In the database, there's more than 34,000 organizations that received funding from Alphabet Soup, there's a column called "IS_SUCCESSFUL" with data if the money was used effectively and additional columns with the application type, affiliation (industry), classification, use case and other categories that would be used as variables to the model.

Before developing the model, the student needs to preprocess the data by removing data that is not relevant, simplify the categories to create a lower number of bins, encode the categorical varibles to numeric outputs and scale the data. After those steps, the neural network can be created, by compiling, training and evaluating the binary classification model to calculate the model’s loss and accuracy.

Since the target predictive accuracy higher than 75%, the student makes modifications to the model in order to improve accuracy. The modifications are the exclusion of noisy variables, additional neuros, additional hidden layers and a different activation function.


## Results

* Data Preprocessing

    * What variable(s) are considered the target(s) for your model?

        The "IS_SUCCESSFUL" is the target of my model, it predicts wheter applicants will be successful if funded by Alphabet Soup

    * What variable(s) are considered to be the features for your model?
    
        All data from the other columns are considered the features of my model except for the "IS_SUCCESSFUL", "EIN" and "NAME" data. For Deliverable 3, in attempt #3, I also removed "SPECIAL_CONSIDERATIONS" and "STATUS" data to see if we could improve the model.

    * What variable(s) are neither targets nor features, and should be removed from the input data?

        Columns "EIN" and "NAME" were dropped since they do not influence the outcome

* Compiling, Training, and Evaluating the Model

    * How many neurons, layers, and activation functions did you select for your neural network model, and why?
    
        For my first model in Deliverable 2, I used 2 hidden layers, the first one with 12 neurons and the second with 8 neurons, both with the "relu" activation function and the "sigmoid" as the output function.
        I used those parameters since the relu function performs well with nonlinear data and 2 hidden layers give another way to process the data nd re-weight it before the output. 

    * Were you able to achieve the target model performance?

        No, as shown below, performance achieved was 70% and the target was 75%.

        ![ScreenShot](https://github.com/liviamiyabara/Neural_Network_Charity_Analysis/blob/main/Resources/Deliverable2_results.JPG)

    * What steps did you take to try and increase model performance?

        For attempt # 1, I changed the output layer and used activation model "tahn". Unfortunately, the accuracy was below the previous one, 54%:

        ![ScreenShot](https://github.com/liviamiyabara/Neural_Network_Charity_Analysis/blob/main/Resources/Attempt1_results.JPG)


        For attempt # 2, I added an additional hidden layer (total of 3 hidden layers) and increased the neurons (25, 12, and 18). Unfortunately, the accuracy was also low, at 55%:

        ![ScreenShot](https://github.com/liviamiyabara/Neural_Network_Charity_Analysis/blob/main/Resources/Attempt2_results.JPG)

        For attempt # 3, I have made changes to the data, I removed column "SPECIAL_CONSIDERATIONS", "STATUS" from the analysis. Unfortunately, the accuracy was also low, at 53%:

        ![ScreenShot](https://github.com/liviamiyabara/Neural_Network_Charity_Analysis/blob/main/Resources/Attempt3_results.JPG)

## Summary

After four different models, I was unable to create a model that could preform a 75% accuracy rating, my best performing model achieved a 70% accuracy. Additional effort is needed to understand if a better accuracy can be achieved by changing the number of neurons, layers, activation model or pre-processing the data. Another option would be using Support Vector Machines (SVMs), since they are a type of binary classifier that use geometric boundaries to distinguish data points from two separate groups. 