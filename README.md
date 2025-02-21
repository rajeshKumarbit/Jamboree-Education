# Jamboree-Education
## Context

- Jamboree has helped thousands of students make it to top colleges abroad. Be it GMAT, GRE or SAT, their unique problem-solving methods ensure maximum scores with minimum effort.
- They recently launched a feature where students/learners can come to their website and check their probability of getting into the IVY league college. This feature estimates the chances of graduate admission from an Indian perspective.


## Problem Statement : 

- Help Jamboree in understanding what factors are important in graduate admissions and how these factors are interrelated among themselves. It will also help predict one's chances of admission given the rest of the variables.


### Column Profiling:

    Serial No. (Unique row ID)
    GRE Scores (out of 340)
    TOEFL Scores (out of 120)
    University Rating (out of 5)
    Statement of Purpose and Letter of Recommendation Strength (out of 5)
    Undergraduate GPA (out of 10)
    Research Experience (either 0 or 1)
    Chance of Admit (ranging from 0 to 1)
    

- Exploratory Data Analysis
    - Null value detection
    - Outliers value detection
    - Descriptive analysis of numerical features
    - Graphical Analysis
    - Univariate Analysis
    - Distribution of categorical variables
    
- Linear Regression
    - Standardization
    - train test split
    - training the model
    - r2 score
    - Adjusted r2
    - Assumptions of Linear Regression
    - Regularisation
         - L1 regularization (Lasso)
         - L2 regularization (Ridge)
         - L1 and L2 regularization (ElasticNet)

## Insights , Feature Importance and Interpretations and Recommendations : 
- first column was observed as unique row identifier which was dropped and was not required for model building.
- University Rating , SOP and LOR strength and research are seems to be discrete random Variables , but also ordinal numeric data. 
- All the other features are numeric, ordinal and continuous.
- No null values were present in  data.
- No Significant amount of outliers were found in data.
- Chance of admission(target variable) and GRE score(an independent feature) are nearly normally distrubted. 


- Independent Variables (Input data): GRE Score, TOEFL Score, University Rating, SOP, LOR, CGPA, Research 
- Target/Dependent Variable : Chance of Admit (the value we want to predict)

- From correlation heatmap , we can observe GRE score, TOEFL score and CGPA have very high correlation with Change of admission.

- University rating, SOP ,LOR and Research have comparatively slightly less correlated than other features.


- Chances of admit is a probability measure , which is within 0 to 1 which is good (no outliers or missleading data in column). 
- Range of GRE score looks like between 290 to 340.
- Range of TOEFL score is between 92 to 120.
- University rating , SOP and LOR are distributed between range of 1 to 5.
- CGPA range is between  6.8 to 9.92.


- From boxplots (distribution of chance of admition (probability of getting admition) as per GRE score ) : with higher GRE score , there is high probability of getting an admition .

- Students having high toefl score , has higher probability of getting admition .




- From count plots, we can observe , statement of purpose SOP strength is positively correlated with Chance of Admission .
- We can also similar pattern in Letter of Recommendation Stength and University rating , have positive correlation with Chaces of Admission .
- Student having research has higher chances of Admission , but also we can observe some outliers within that caregory.

##### Actionable Insights and  Recommendations : 

* Education institute can not just help student to improve their CGPA score but also assist them writing good LOR and SOP thus helping them admit to better university.
* The education institute can not just help student to improve their GRE Score but can also assist them writing good LOR and SOP thus helping them admit to a better University.
* Awareness of CGPA and Reserach Capabilities : Seminars can be organised to increase the awareness regarding CGPA and Research Capablities to enhance the chance of admit.
* Any student can never change their current state of attributes so awareness and marketing campaign need to surveyed hence creating a first impression on student at undergraduate level, which wont just increase company's popularity but will also help sudent get prepared for future plans in advance. 
* A dashboard can be created for students whenever they loged in into your website, hence allowing a healthy competition also to create a progress report for students.
* Additional features like number of hours they put in studing, watching lectures, assignments soved percentage, marks in mock test can result a better report for every student to judge themselves and improve on their own.


### Regression Analysis : 

- From regression analysis (above bar chart and REPORT file), we can observe the CGPA is the most Important feature for prediciing the chances of admission. 
- Other important features are GRE and TOEFL score . 

- After first Regression Model, checked for Multicolinearity . Getting all the VIF scores below 5 , showing there's no high multicolinearity.
- All the residuals are not perfectly normally distributed. and so residual plot we can observe some level of heteroscedasticity.
- Regularised model ridge and lasso both give very similar results to Linear Regression Model. 
- Similarly ElasticNet (L1+L2) also returns very similar results. along with rest of all the model metrics.

