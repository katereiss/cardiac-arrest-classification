The goal of this project is to provide an interpretable classification model for cardiac arrest outcomes using FDNY EMS data. By identifying features associated with cardiac arrest deaths, FDNY will be able to make informed decisions around decreasing the amount of patient deaths due to cardiac arrest. This model will classify unseen cardiac arrest incidents as either on-scene deaths or transports. 

The initial logistic regression model used the following features:

- Dispatch time in seconds
- Response time in seconds
- Travel time in seconds
- Total time in seconds

The initial accuracy score was 0.57.

Then, a feature for initial call type = final call type was added. Initial call type represents bystander’s initial impression of the call- for example, heart problems, trouble breathing, or drug overdose. Final call type is cardiac arrest for all incidents in this dataframe. This feature quantifies whether the bystander initiating the call is aware that the patient is in cardiac arrest when the incident is initiated.

Adding this feature increased the logistic regression accuracy score to 0.606.

The K-nearest-neighbors accuracy score for all features previously mentioned was 0.552. 

Next steps would include additional feature engineering: there are available categorical data for location, including zip code, congressional district, and borough. Adding location features may further increase the score of the model.

Additional evaluation metrics would be appropriate, including precision, recall, and F1 score. This will be helpful in determining if the model is more correct predicting one outcome more than another.

Increasing regularization for a logistic regression model would be an appropriate next step, as total time is closely related to other time metrics that are already considered in the model. Other models to consider would be random forest, which may be able to better accomodate the categorical features present in the dataset, and XGBoost.
