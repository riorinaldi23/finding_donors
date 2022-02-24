# finding_donors
A supervised learning project using census data to predict income. Part of Udacity's Intro to Machine Learning with Tensorflow Nanodegree

## Dataset

The census dataset being used is a shortened version of the 1994 US Census dataset, involving 14 columns (13 features and income as the predicted variable).

* **age**: continuous. 
* **workclass**: Private, Self-emp-not-inc, Self-emp-inc, Federal-gov, Local-gov, State-gov, Without-pay, Never-worked. 
* **education**: Bachelors, Some-college, 11th, HS-grad, Prof-school, Assoc-acdm, Assoc-voc, 9th, 7th-8th, 12th, Masters, 1st-4th, 10th, Doctorate, 5th-6th, Preschool. 
* **education-num**: continuous. 
* **marital-status**: Married-civ-spouse, Divorced, Never-married, Separated, Widowed, Married-spouse-absent, Married-AF-spouse. 
* **occupation**: Tech-support, Craft-repair, Other-service, Sales, Exec-managerial, Prof-specialty, Handlers-cleaners, Machine-op-inspct, Adm-clerical, Farming-fishing, Transport-moving, Priv-house-serv, Protective-serv, Armed-Forces. 
* **relationship**: Wife, Own-child, Husband, Not-in-family, Other-relative, Unmarried. 
* **race**: Black, White, Asian-Pac-Islander, Amer-Indian-Eskimo, Other. 
* **sex**: Female, Male. 
* **capital-gain**: continuous. 
* **capital-loss**: continuous. 
* **hours-per-week**: continuous. 
* **native-country**: United-States, Cambodia, England, Puerto-Rico, Canada, Germany, Outlying-US(Guam-USVI-etc), India, Japan, Greece, South, China, Cuba, Iran, Honduras, Philippines, Italy, Poland, Jamaica, Vietnam, Mexico, Portugal, Ireland, France, Dominican-Republic, Laos, Ecuador, Taiwan, Haiti, Columbia, Hungary, Guatemala, Nicaragua, Scotland, Thailand, Yugoslavia, El-Salvador, Trinadad&Tobago, Peru, Hong, Holand-Netherlands.


## Data Preprocessing

Preprocessing included:

1. Transforming continuous variables that were skewed using logarithmic transformation.
2. Utilizing a 0 to 1 normalization using MinMaxScaler
3. One-hot encoding of categorical variables

## Model Selection and Tuning

I selected 3 initial machine learning algorithms that were selected based on the data we had.

* Decision Tree
* Support Vector Machine
* Logistic Regression

Using GridSearchCV, we optimized the Support Vector Machine to get the best F0.5 score that we could. Interestingly, the best model we got was a linear model (did not utilize the kernel trick) and a small C parameter. This could explain why the logistic regression model, despite requiring much less computing power, had similar results.

