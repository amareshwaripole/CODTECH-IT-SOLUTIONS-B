# CODTECH-IT-SOLUTIONS-B

Titanic Survival Prediction Using Machine Learning

Challenge
Build a predictive model that answers the question: "what sorts of people were more likely to survive the Titanic sinking?"

Data
To take a look at the competition data, click on the Data tab at the top of the competition page. Then, scroll down to find the list of files. There are three files in the data: (1) train.csv, (2) test.csv, and (3) gender_submission.csv.

Column Name - customers.csv	Description
Survival	Survival (0 = No; 1 = Yes). Not included in test.csv file
Pclass	Ticket Class/ A Proxy for socio-economic status(SES) (1 = 1st/Upper ; 2 = 2nd/Middle; 3 = 3rd/Lower)
Name	Name
Sex	Sex
Age	Age is fractional if less than 1. If the age is estimated, is it in the form of xx.5
Sibsp	Number of Siblings (brother, sister, stepbrother, stepsister) /Spouses (husband, wife (mistresses and fiancés were ignored)) Aboard
Parch	Number of Parents (mother, father)/Children (daughter, son, stepdaughter, stepson) Aboard; Some children travelled only with a nanny, therefore parch=0 for them.
Ticket	Ticket Number
Fare	Passenger Fare
Cabin	Cabin
Embarked	Port of Embarkation (C = Cherbourg; Q = Queenstown; S = Southampton)
Workflow stages
The competition solution workflow goes through seven stages described in the Data Science Solutions book.

Question or problem definition
Wrangle, prepare, cleanse the data
EDA (Exploratory Data Analysis) - Analyze, identify patterns, and explore the data
Acquire training and testing data
Model, predict and solve the problem
Visualize, report, and present the problem solving steps and final solution
Supply or submit the results

1. Question or problem definition
The competition is simple: Use the Titanic passenger data (name, age, price of ticket, etc.) to try to predict who will survive and who will die. This is a binary classification.
Binary classification is the task of classifying the elements of a set into two groups on the basis of a classification rule.
The values in the second column (“Survived”) can be used to determine whether each passenger survived or not: if it’s a “1”, the passenger survived. if it’s a “0”, the passenger died.

2. Wrangle, prepare, cleanse the data
Here is my workflow for cleaning the data. I am not going to show all the step here, you can check my Kaggle for full code. Check my Kaggle and GitHub to took a look at all my projects🍀

3. Exploratory Data Analysis
Analyze, identify patterns, and explore the data Analysis 
Only 350 out of 891 passengers (38.4%) survived in the training set.

Sex
The number of men on board the ship is much higher than the number of women, but the number of women saved is more than twice that of the number of males survived. The survival rates for a women on the ship is around 75% while that for men in around 19%.

Pclass
Passenegers Of Pclass 1 has a very high priority to survive. The number of Passengers in Pclass 3 were a lot higher than Pclass 1 and Pclass 2, but still the number of survival from Pclass 3 is low compare to them Pclass 1 %survived is around 63%, for Pclass2 is around 48%, and Pclass3 survived is around 25%

Sex and class are important factors for survival. Let’s determine survival rate based on sex and class together
Female from Upper class is about 95–96% survived. Only 3 out of 94 Women from Upper class died.
Female Upper class has high priority to survive
Lower class female has more survived rate than Upper class male
Sex is positively corrlated with Survived (with a Person’s correlation coefficient of 0.54) ; Female is more likely to survive
Pclass is negatively correlated with Survived(with a Pearson’s correlation coefficient of -0.34) ; Obviously, better the ticket class (1 = 1st/Upper ; 2 = 2nd/Middle; 3 = 3rd/Lower), higher the chance of survival.
Those important feature for prediction the Survived people

4. Acquire training and testing data

5. Model, predict and solve the problem

Model selection
Random Forests and Decision Trees are the most accurate (96.97%) in predicting the survival of passengers and they are select to predicted the testing data.

Visualize the decision tree

Finding :
According to the analysis, passengers were more likely to survive if:
Upper class ticket
Women/Lady On the contrary, being a Lower class old man lowered the chances of survival. 
