# Marketing-Campaigns
 The marketing campaigns were based on phone calls. Often, more than one contact to the same client was required, in order to access if the product (bank term deposit) would be ('yes') or not ('no') subscribed.
## DataSet
Datasetr elated to direct marketing campaigns (phone calls) of a Portuguese banking institution. The classification goal is to predict whether the client will subscribe (1/0) to a term deposit (variable y). 
- **age:** (numeric)
- **job:** type of job (categorical: “admin”, “blue-collar”, “entrepreneur”, “housemaid”, “management”, “retired”, “self-employed”, “services”, “student”, “technician”, “unemployed”, “unknown”)
- **marital :** marital status (categorical: “divorced”, “married”, “single”, “unknown”)
education (categorical: “basic.4y”, “basic.6y”, “basic.9y”, “high.school”, “illiterate”, “professional.course”, “university.degree”, “unknown”)
- **default:** has credit in default? (categorical: “no”, “yes”, “unknown”)
- **housing:** has housing loan? (categorical: “no”, “yes”, “unknown”)
- **loan:** has personal loan? (categorical: “no”, “yes”, “unknown”)
- **contact:** contact communication type (categorical: “cellular”, “telephone”)
- **month:** last contact month of year (categorical: “jan”, “feb”, “mar”, …, “nov”, “dec”)
- **day_of_week:** last contact day of the week (categorical: “mon”, “tue”, “wed”, “thu”, “fri”)
- **duration:** last contact duration, in seconds (numeric). Important note: this attribute highly affects the output target (e.g., if duration=0 then y=’no’). The duration is not known before a call is performed, also, after the end of the call, y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model
- **campaign:** number of contacts performed during this campaign and for this client (numeric, includes last contact)
- **pdays:** number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted)
- **previous:** number of contacts performed before this campaign and for this client (numeric)
- **poutcome:** outcome of the previous marketing campaign (categorical: “failure”, “nonexistent”, “success”)
- **emp.var.rate:** employment variation rate — (numeric)
- **cons.price.idx:** consumer price index — (numeric)
- **cons.conf.idx:** consumer confidence index — (numeric)
- **euribor3m:** euribor 3 month rate — (numeric)
- **nr.employed:** number of employees — (numeric)
## Logistic Regression
Logistic Regression is a Machine Learning classification algorithm that is used to predict the probability of a categorical dependent variable. In logistic regression, the dependent variable is a binary variable that contains data coded as 1 (yes, success, etc.) or 0 (no, failure, etc.). In other words, the logistic regression model predicts P(Y=1) as a function of X.
## Over-sampling using SMOTE
At a high level, SMOTE:
- Works by creating synthetic samples from the minor class (no-subscription) instead of creating copies.
- Randomly choosing one of the k-nearest-neighbors and using it to create a similar, but randomly tweaked, new observations.
## Recursive Feature Elimination
Recursive Feature Elimination (RFE) is based on the idea to repeatedly construct a model and choose either the best or worst performing feature, setting the feature aside and then repeating the process with the rest of the features. This process is applied until all features in the dataset are exhausted. The goal of RFE is to select features by recursively considering smaller and smaller sets of features.
### Accuracy: 0.81
