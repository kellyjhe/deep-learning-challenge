# Deep Learning Challenge

## 🔎 Overview
The purpose of this analysis is to aid Alphabet Soup by developing a machine learning model that can predict applicant success based on data from 34,000 organizations that have previously been approved and received funding. The model aims to identify applicants that are successful given known variables such as application type, affliated sector of industry, government organization classification, organization type, income classification, funding amount requested, and use case for funding.

In this analysis, I preprocessed the data by importing the CSV file and cleaning the data for machine learning. I consolidated the categories in 'APPLICATIION_TYPE' and 'CLASSIFICATION' and converted categorical data into numeric values. I then split the data into our target and feature arrays by isolating the 'IS_SUCCESSFUL' column, the outcome of which is the focus of our model and what we aim to predict. After fitting and scaling the data using 'StandardScalar', I then created the model by compiling, training and evaluating the data.

## 🔬 Results
1. **Data Preprocessing**
  - The variable that we are targeting is the 'IS_SUCCESSFUL' variable.
  - The variables that are features for the model include 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'STATUS', 'INCOME_AMT', 'SPECIAL_CONSIDERATIONS', and 'ASK_AMT'.
  - I removed the variables 'EIN' and 'NAME' because they are neither targets nor features.
 
2. **Compiling, Training and Evaluating the Model**
  - For the initial test, I opted to use a number of 'len(X_train[0])' neurons, 850 layers, and the relu activation function. I chose to use these as a random selection. Because the 'relu' function is the most commonly used, I chose it to begin the evaluation.
  - I was unable to achieve the target model performance. I reached about 72% accuracy, lower than the ideal percentage of 75%.
  - To increase model performance, I made three attempts by changing several characteristics of the model. For the first attempt, I increased the number of hidden layers to 950 and lowered the number of epochs to 50. In the second attempt, I kept the amount of layers at 950 but changed the activation function to tanh, and increased the number of epochs back to 100. In the third attempt, I singled one variable and decreased the number of layers to 750 while keeping the rest of the characteristics from the second attempt. All of the attempts yielded the same results, at 72% accuracy.

## 📖 Summary
Although I did not achieve an accuracy score of 75%, the model was able to predict the success rate with 72% accuracy. A different model that minimizes the loss amount and increases the accuracy score would perform better for making predictions. There are the relu, tanh and sigmoid functions that could be tested to determine which fits the best. Increasing the amount of layers could improve the strength of the neural network as well, creating a deeper and more complex learning model.
