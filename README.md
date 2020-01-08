# Chances-of-Admit-Predictor-Using-Logistic-Regression
This project uses Logistic Regression to estimate the Chances of Admission to a particular class of University for Graduate Studies.

### Citation for the dataset - 
Mohan S Acharya, Asfia Armaan, Aneeta S Antony : A Comparison of Regression Models for Prediction of Graduate Admissions, IEEE International Conference on Computational Intelligence in Data Science 2019
The dataset used is available [here](https://www.kaggle.com/mohansacharya/graduate-admissions). 

The dataset consists of the following features - 
1. Serial No. (was not abbreviated in the project)
2. GRE Score (abbreviated as GRE in the project)
3. TOEFL Score (abbreviated as TOEFL in the project)
4. University Rating (abbreviated as UR in the project)
5. SOP (was not abbreviated in the project)
6. LOR (was not abbreviated in the project)
7. CGPA (was not abbreviated in the project)
8. Research (was not abbreviated in the project)
9. Chance of Admit (abbreviated as COA in the project)

The task is to predict target feature **Chance of Admit** using all the input features excluding the **Serial No.**

The dataset shows the target feature in terms of probability which means that **Chances of Admit** or **COA** will be a real number between 0 and 1. Thus, the target feature is a continuous variable. However, Logistic Regression is a classification algorithm and needs finite number of target classes for prediction.

In order to resolve this, the target feature is split into 3 categories:
- Class 0: AMBITIOUS (Chances of Admit <= 0.5 or 50%)
- Class 1: REALISTIC (Chances of Admit between 0.5-0.85 or between 50%-85%)
- Class 2: AMBITIOUS (Chances of Admit > 0.85 or 85%)

After training the model and testing it's accuracy, the model is used to predict the Chances of Admit (SAFE, REALISTIC, AMBITIOUS) based on a profile entered by the user.
