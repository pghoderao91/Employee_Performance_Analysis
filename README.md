# Employee_Performance_Analysis



## PROJECT SUMMARY:
### BUSINESS CASE & GOAL OF PROJECT: BASED ON GIVEN FEATURE OF DATASET WE NEED TO PREDICT THE PERFOMANCE RATING OF EMPLOYEE


**The Data science project which is given here is an analysis of employee performance**

###  Analysis
Data were analyzed by describing the features present in the data. the features play the bigger part in the analysis. The features tell the relation between the dependent and independent variables. Pandas also help to describe the datasets answering following questions early in our project. The data present in the dataset are divided into numerical and categorical data.

### Categorical Features:
1.EmpNumber

2.Gender

3.EducationBackground

4.MaritalStatus

5.EmpDepartment

6.EmpJobRole

7.BusinessTravelFrequency

8.OverTime

9.Attrition


### Numerical Features:

1.Age

2.DistanceFromHome

3.EmpHourlyRate

4.NumCompaniesWorked

5.EmpLastSalaryHikePercent

6.TotalWorkExperienceInYears

7.TrainingTimesLastYear

8.ExperienceYearsAtThisCompany

9.ExperienceYearsInCurrentRole

10.YearsSinceLastPromotion

11.YearsWithCurrManager


### Ordinal Features:

1.EmpEducationLevel

2.EmpEnvironmentSatisfaction

3.EmpJobInvolvement

4.EmpJobLevel

5.EmpJobSatisfaction

6.EmpRelationshipSatisfaction

7.EmpWorkLifeBalance

8.PerformanceRating


## Data Pre-Processing
1. Check Missing Value: Their is no missing value in data

2. Categorical Data Conversion: Handel categorical data with the help of frequency and mannual encoding, because feature is contain lot's of labels

* Mannual Encoding: Mannual encoding is a best techinque to handel categorical feature with the help of map function, map the labels based on frequency.

* Frequency Encoding: Frequency encoding is an encoding technique to transform an original categorical variable to a numerical variable by considering the frequency distribution of the data getting value counts.

3. Outlier Handling Some features are contain outliers so we are impute this outlier with the help of IQR because in all features data is not normally distributed

4. Scaling The Data: scaling the data with the help of Standard scalar, Standard Scaling: Standardization is the process of scaling the feature, it assumes the feature follow normal distribution and scale the feature between mean and standard deviation, here mean is 0 and standard deviation is always 1.


## Feature Selection

1.  Drop unique and constant feature: Dropping employee number because this is a constant column as well as drop Years Since Last Promotion because we create a new feaure using square root transformation

2. Checking Correlation: Checking correlation with the help of heat map, and get the their is no highly correlated feature is present.**Heatmap:** A heatmap is a graphical representation of data that uses a system of color-coding to represent different values.

3. Check Duplicates: In this data Their is no dupicates is present.

4. PCA: Use pca to reduce the dimension of data, Data is contain total 27 feature after dropping unique and constant column,from PCA it shows the 25 feature has less varaince loss, so we are going to select 25 feature.Principal component analysis (PCA) is a popular technique for analyzing large datasets containing a high number of dimensions/features per observation, increasing the interpretability of data while preserving the maximum amount of information, and enabling the visualization of multidimensional data. Formally, PCA is a statistical technique for reducing the dimensionality of a dataset.

5. Saving Pre-Process Data: save the all preprocess data in new file and add target feature to it.

## Machine learning Model Creation & Evaluation
1. Define Dependant and Independant Features:

2. Balancing the data: The data is imbalance, so we need to balance the data with the help of SMOTE

**SMOTE:** SMOTE (synthetic minority oversampling technique) is one of the most commonly used oversampling methods to solve the imbalance problem. It aims to balance class distribution by randomly increasing minority class examples by replicating them. SMOTE synthesises new minority instances between existing minority instances.
3.Splitting Training And Testing Data: 80% data use for training & 20% data used for testing

## Algorithms:
* AIM: Create a sweet spot model (Low bias, Low variance)

**HERE WE WILL BE EXPERIMENTING WITH THREE ALGORITHM**

1. Support Vector Machine
2. Random Forest
3. Artificial Neural Network [MLP Classifier]

* Support vector machine well perform on training data with accuracy 96.61% but the test score is 94.66 after applying Hyperparameter tunning score is 98.28 means model is overfit.
* Random forest very well perform in training data with 100% accuracy but in testing 95.61% after doing hyperparameter tunning testing score is decreases.
* Artifical neural network[Multilayer percepton] perform very well on training data with 98.95% accuracy and testing score is 95.80%.
So we are select Artifical neuranl network [Multilayer percepton] model.
