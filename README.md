# Brief Summary:
The dataset comes from the UCI Machine Learning repository. The data is from a Portugese banking institution and is a collection of the results of multiple marketing campaigns. The dataset collected is related to 17 campaigns that occurred between May 2008 and November 2010. The goal is to compare the performance of the classifiers (k-nearest neighbors, logistic regression, decision trees, and support vector machines) using this dataset.

# Approach:
We will be using the CRISP-DM methodology for achieving this goal.

## Business Understanding
Business Objective: <br />
For targeted direct marketing campaign Identify the main driving factors that contribute to customer able to sucessfully open a long term direct deposit account.

## Data Understanding

The Dataset has 20 features:<br />
<br />
<b>Input variables: </b><br />
* Bank client data:<br />
1 - age (numeric) <br />
2 - job : type of job (categorical: 'admin.','blue-collar','entrepreneur','housemaid','management','retired','self-employed','services','student','technician','unemployed','unknown') <br />
3 - marital : marital status (categorical: 'divorced','married','single','unknown'; note: 'divorced' means divorced or widowed)<br />
4 - education (categorical: 'basic.4y','basic.6y','basic.9y','high.school','illiterate','professional.course','university.degree','unknown')<br />
5 - default: has credit in default? (categorical: 'no','yes','unknown')<br />
6 - housing: has housing loan? (categorical: 'no','yes','unknown')<br />
7 - loan: has personal loan? (categorical: 'no','yes','unknown')<br />
<br />
* Related with the last contact of the current campaign:<br />
8 - contact: contact communication type (categorical: 'cellular','telephone')<br />
9 - month: last contact month of year (categorical: 'jan', 'feb', 'mar', ..., 'nov', 'dec')<br />
10 - day_of_week: last contact day of the week (categorical: 'mon','tue','wed','thu','fri')<br />
11 - duration: last contact duration, in seconds (numeric). Important note: this attribute highly affects the output target (e.g., if duration=0 then y='no'). Yet, the duration is not known before a call is performed. Also, after the end of the call y is obviously known. Thus, this input should only be included for benchmark purposes and should be discarded if the intention is to have a realistic predictive model.<br />
<br />
* Other attributes:<br />
12 - campaign: number of contacts performed during this campaign and for this client (numeric, includes last contact)<br />
13 - pdays: number of days that passed by after the client was last contacted from a previous campaign (numeric; 999 means client was not previously contacted)<br />
14 - previous: number of contacts performed before this campaign and for this client (numeric)<br />
15 - poutcome: outcome of the previous marketing campaign (categorical: 'failure','nonexistent','success')<br />
<br />
* Social and economic context attributes<br />
16 - emp.var.rate: employment variation rate - quarterly indicator (numeric)<br />
17 - cons.price.idx: consumer price index - monthly indicator (numeric)<br />
18 - cons.conf.idx: consumer confidence index - monthly indicator (numeric)<br />
19 - euribor3m: euribor 3 month rate - daily indicator (numeric)<br />
20 - nr.employed: number of employees - quarterly indicator (numeric)<br />
<br />

<b>Output variable (desired target):</b>
<br />21 - y - has the client subscribed a term deposit? (binary: 'yes','no')<br />
<br />
- Applied the pandas crosstab function to plot the feature and output variable 'y' (whether user opened the long term deposit yes/no)
- Generated the heatmap to see the correlation between different features

## Data Preparation
In Data preparation phase
- Checked for null values if any records need to be removed or imputed based on the null values
- Identified the outliers for feature by applying iqr.

## Modeling
Created a simple Logistic Regression model and determined its accuracy score of 0.896
Compared the performance of the Logistic Regression model to our KNN algorithm, Decision Tree, and SVM models. Using the default settings for each of the models, fit and score each. 

## Evaluation

Each of the models used were compared with respect to train and test score, average training fit time taken. Plotted the ROC curve and AUC value determined for each of the model

# Conclusion:












