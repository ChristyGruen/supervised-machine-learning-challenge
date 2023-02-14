#  <span style="color:tan"> **Module 19 Supervised Machine Learning Challenge**  </span>
### Chris Gruenhagen 14Feb2023
---

## **Purpose**

Lending services companies allow individual investors to partially fund personal loans as well as buy and sell notes backing the loans on a secondary market.

Use the provided lending data to create Logistic Regression and Random Forest Classifier machine learning models to classify the risk level of given loans and compare the performance of the two models.

## **Prediction**

Prior to creating the machine learning models, make a prediction as to which model will perform better and provide justification.

### ***Logistic Regression Model:***

  The logistic regression model can define a non-linear separation between the approved and rejected applications based on the variables provided.
  The logistic regression model is an equation that models probability of output in terms of input - but it can be used as a binary classifier due to it's limits at 0 and 1. https://en.wikipedia.org/wiki/Logistic_regression

### ***Random Forest Classifier:***
  The random forests classifier uses a multitude of decision trees to determine the best fit.  Each individual decision tree splits the data based on the variables provided, however they are prone to overfitting their training sets.  The random forest classifier is able to pick the individual decision tree model that best describes the test data.  The random forest classifier does not weight the results.  Data characteristics can affect their performance.  https://en.wikipedia.org/wiki/Random_forest
  
  "A large number of relatively uncorrelated models(trees) operating as a committee will outperform any of the individual constituent models." - Tony Yiu

  "The random forest is a classification algorithm consisting of many decisions trees. It uses bagging and feature randomness when building each individual tree to try to create an uncorrelated forest of trees whose prediction by committee is more accurate than that of any individual tree." - Tony Yiu

  "What do we need in order for our random forest to make accurate class predictions?
  * We need features that have at least some predictive power. After all, if we put garbage in then we will get garbage out.
  * The trees of the forest and more importantly their predictions need to be uncorrelated (or at least have low correlations with each other). While the algorithm itself via feature randomness tries to engineer these low correlations for us, the features we select and the hyper-parameters we choose will impact the ultimate correlations as well." - Tony Yiu

  https://towardsdatascience.com/understanding-random-forest-58381e0602d2

### ***Prediction:***
  I think that the logistic regression model will provide a better fit as the accuracy of the random forest classifier can be affected by correlated variables. 

## **Results**

|Model|Training Score|Testing Score|Computation Time|
|--------|--------|--------|--------|
|Logistic Regression| 0.9942908240473243|0.9936545604622369|0.1s|
|Random Forest Classifier|0.9974893382858715|0.9910751134956666|0.9s|
---

## **Conclusion**


<p>In conclusion, both models are acceptable with returned testing scores of 0.99.  The Logistic Regression model score (0.9936545604622369) is slightly higher than the Random Forest Classifier score (0.9910751134956666).  The Logistic Regression model took 0.1 seconds to fit the data and the Random Forest Classifier took 0.9 seconds to fit the data with n_estimators = 50.  
The Logistic Regression model performed better as it provides the best fit and least computation time.</p>
<p>
I did predict that the logistic regression model would perform better, but my rationale for why the Random Forest Classifier (RFC) did not seem to hold true for this dataset.  The accuracy of the RFC was not impacted by correlated variables (if present) and did not overfit to the training data.  The RFC provided acceptable testing scores, but it took 9x as long as the logistic regression to return the fit.
</p>

---

# 💰 💵 🔢 📈 &#x1F469;&#x200d;&#x1F4bb; 📈 🔢 💵 💰
     emoji & format references:
        https://emojipedia.org
        https://commons.wikimedia.org/wiki/Emoji/Table
        https://www.markdownguide.org/basic-syntax/

        
***See below for original homework instructions***
# <span style="color:tan"> Module 19 Supervised Machine Learning Challenge</span>
Due Feb 22, 2023 by 11:59pm 

Points 100 

Submitting a text entry box or a website url
_________________________________________________________
## <span style="color:red"> **Background**  </span>

Lending services companies allow individual investors to partially fund personal loans as well as buy and sell notes backing the loans on a secondary market.

You will be using this data to create machine learning models to classify the risk level of given loans. Specifically, you will be comparing the Logistic Regression model and Random Forest Classifier.

##  <span style="color:orange"> **Before You Begin** </span>

1. Create a new repository for this project called supervised-machine-learning-challenge. Do not add this Challenge to an existing repository.
2. Clone the new repository to your computer.
3. Inside your local git repository, create a directory for the Supervised Machine Learning Challenge.
4. Push the above changes to GitHub.

##  <span style="color:yellow"> **Files** </span>

Download the following files to help you get started:

<a href = "https://static.bc-edx.com/data/dl-1-1/m19/lms/starter/Starter_Code.zip " target = "_blank"> Module 19 Challenge files </a>


##  <span style="color:green">  **Instructions** </span>

### ***Retrieve the Data***
The data is located in the Challenge Files Folder: lending_data.csv

Import the data using Pandas. Display the resulting dataframe to confirm the import was successful.

### ***Predict Model Performance***
You will be creating and comparing two models on this data: a Logistic Regression, and a Random Forests Classifier. Before you create, fit, and score the models, make a prediction as to which model you think will perform better. You do not need to be correct!

Write down your prediction in the designated cells in your Jupyter Notebook, and provide justification for your educated guess.

### ***Split the Data into Training and Testing Sets***
Create the features DataFrame, X, by removing the loan_status column. Create y, the labels set, by using the loan_status column. Split the data into training and testing datasets by using the train_test_split function.

### ***Create, Fit and Compare Models***
Create a Logistic Regression model, fit it to the training data that you created in the previous step. Then, determine the model's score by using the score function and the testing data from the previous step. Do the same for a Random Forest Classifier. You may choose any starting hyperparameters you like.

Review the scores of each model. Which model performed better? How does that compare to your prediction? Write down your results and thoughts in the designated markdown cell.


##  <span style="color:blue"> **Requirements** </span>
### ***Retrieve the Data (5 points)***
* Import the lending_data.csv file as a Pandas dataframe (3 points)
* Confirm that the import was successful by displaying the dataframe (2 points)

### ***Predict Model Performance (15 points)***
* Make a prediction on which model will perform better on the data (5 points)
* Justify the prediction with information about the models (10 points)

### ***Split the Data into Training and Testing Sets (30 points)***
* Create the features DataFrame, X, by removing the loan_status column (10 points)
* Create y, the labels set, by using the loan_status column (10 points)
* Split the data into training and testing datasets by using the train_test_split function (10 points)

### ***Create, Fit and Compare Models (50 points)***
* Create and train a Logistic Regression model (10 points)
* Score the Logistic Regression model (10 points)
* Create and train a Random Forest Classifier model (10 points)
* Score a Random Forest Classifier model (10 points)
* State which model performed better (5 points)
* Compare the actual model performance with your predictions (5 points)

## <span style="color:indigo"> **References**  </span>
Loan Approval Dataset (2022). DData for this dataset was generated by edX Boot Camps LLC, and is intended for educational purposes only.

© 2023 edX Boot Camps LLC
