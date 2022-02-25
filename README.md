# Classifying NYFD Cardiac Arrest Outcomes

## **Abstract**

The goal of this project is to provide an interpretable classification model for cardiac arrest outcomes using FDNY EMS data from NYC Open Data. By identifying features associated with cardiac arrest deaths, this model can assist FDNY in making informed decisions around decreasing the amount of patient deaths due to cardiac arrest. This model classifies cardiac arrest incidents as either on-scene deaths or transports, and provides interpretable results that suggest which features present have associations with cardiac arrest outcomes. 

## **Design**

This project uses [EMS dispatch data](https://data.cityofnewyork.us/Public-Safety/EMS-Incident-Dispatch-Data/76xm-jjuj) to classify cardiac arrests as either deaths or transports. The model is focused on interpretability, as learning what features most associate with cardiac arrest deaths can provide insight on how to prevent them.

## **Data**

The original dataset contains 21 million rows of FDNY EMS calls from 2008 to 2021. I filtered the data to only include calls with a final disposition of cardiac arrest. Features included incident datetime, response time in seconds, initial and final call types, zipcode, borough, and patient outcome, among others. 

## **Algorithms**

*Feature Engineering*

1. Created binary feature for initial call type = final call type, representing if the patient was in cardiac arrest when the call was initiated
2. Converted categorical features into binary dummy variables
3. Converted categorical features into numeric categories for tree-based models
4. Converted datetime features to categorical month feature

*Models*

Logistic regression, k-nearest neighbors, Bernoulli naive bayes, decision tree, and random forest classifiers were tested. Model performance and interpretability were taken into consideration.

*Model Evaluation and Selection*

The training dataset of 293,655 incidents was split into 60/20/20 train, validation, and test.

Accuracy, precision, recall, F1, and ROC AUC were all considered in choosing a model, with more weight given to F1. Both precision and recall were important, and neither a false positive nor a false negative were significantly worse in this case.

Logistic Regression and Naive Bayes had identical F1 scores, so I chose Logistic Regression due to the higher ROC AUC score and interpretability.

**Final Logistic Regression scores:** 

- Accuracy 0.6180
- Precision 0.6651
- Recall 0.6804
- F1 0.6727
- ROC AUC 0.6066

## **Tools**

- Numpy and Pandas for data manipulation
- Scikit-learn for modeling
- Matplotlib and Seaborn for plotting

## **Communication**

Presentation slides are attached to this repo.
