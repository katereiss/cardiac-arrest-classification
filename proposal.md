### **Question/need:**

- The goal of this project is to provide an interpretable classification model for cardiac arrest outcomes using FDNY EMS data. This model will classify unseen cardiac arrest incidents as either on-scene deaths or transports. Additionally, this project aims to identify features associated with cardiac arrest outcomes.

### **Data Description:**

- Dataset: EMS Incident Dispatch Data from NYC OpenData is a CSV dataset with 29 million rows where one row is one EMS incident. Some of the 31 columns include incident datetime, call type, response time in seconds, and zip code. Only cardiac arrest data will be used, reducing the number of rows to an estimated 200,000. Almost all cardiac arrest incidents in this dataset have a disposition of death or transport, and all rows with other dispositions will be excluded.
- Incident Disposition (patient outcome) is the target variable.

### **Tools:**

- Python packages for classification models (sklearn, xgboost) will be used.

### **MVP Goal:**

- A linear regression model with feature engineering would be an MVP for this project.
- Additions will include rigorous model selection and evaluation and several other classification models.
