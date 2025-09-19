# Student-Performance-Prediction-Model
This project was completed as part of DTSC 670 – Foundations of Machine Learning (Eastern University, 2024). The goal was to build and evaluate machine learning models to forecast student academic outcomes based on demographic, social, and academic factors.
Project Overview

Built predictive models using Linear Regression, Support Vector Regression (SVR), and Lasso Regression.

Evaluated model performance with RMSE and R².

Applied cross-validation to ensure robustness and generalizability.

Found that midterm grades (G1/G2) significantly improved predictive accuracy, enabling early identification of at-risk students.

Analyzed feature importance (e.g., parental education, past failures), offering actionable insights for academic advising and intervention.

## Data Overview
The original dataset comprises various features into 34 columns, related to student demographics, educational background, and academic performance, including but not limited to: 

 age, sex, famsize, guardian -identified as demographic features; 
 Medu (mother's education), Fedu (father's education), studytime, failures – identified as Academic Background;
 schoolsup (school support), famsup (family support), paid (extra paid classes), activities- identified as Support Features;
 absences_G1, absences_G2, absences_G3, G1, G2, G3 -identified as Absences and Grades;
 and finally freetime, goout, health -identified as Behavioral Attributes. 

These attributes are relevant because they can influence a student's academic performance. For instance, parental education levels (Medu, Fedu) often correlate with better academic outcomes, while behavioral factors like freetime and goout can impact study habits and grades specially in young ages.

The target variable is G3, the final grade of the students. During data exploration, it was noticed that there was a strong positive correlation between G3 and the midterm grades G1 and G2, indicating that students who perform well in the earlier terms tend to maintain their performance. Study Time as well shows a positive correlation with G3, suggesting that more study time is associated with better final grades. Conversely, failures have a negative correlation, indicating that past academic failures are linked to lower final grades.

I created models both with and without G1/G2 grades for two main reasons:

 1.	Early Intervention: Excluding G1 and G2 makes the prediction more challenging but valuable, as it allows for early   identification of students at risk before midterm grades are available. This enables proactive interventions at the  beginning of the academic year.
    
 2.	Prediction Accuracy: Including G1 and G2 enhances model accuracy due to their strong correlation with G3. This model can  provide more precise predictions later in the year when midterm grades are available, helping refine support strategies for  students.

## Methods & Tools

Languages/Frameworks: Python, Jupyter Notebook

Libraries: scikit-learn, pandas, numpy, matplotlib, seaborn

Techniques: Regression (Linear, SVR, Lasso), Cross-validation, Feature importance analysis

## Key Results

 Best performing model: SVR with midterm grades included.

 Strong predictors: Midterm grades, prior academic failures, parental education levels.

 Impact: Provides a framework for early detection of at-risk students and supports targeted academic interventions.
