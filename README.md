<h1 align="center"> Cardiovascular Heart Disease risk prediction</h1>
<h3 align="center"> AlmaBetter Verfied Project - <a href="https://www.almabetter.com/"> AlmaBetter </a> </h5>

<p align="center"> 
<img src="https://github.com/tushar8668/Cardiovascular_Heart-_disease_risk-_Prediction-using-Classification_Technique/blob/main/cardiovascular_risk_imag.png" alt="AEP.jpg"  height="320px">
</p>


## Introduction 

Cardiovascular Risk Prediction dataset provides the patients' information. The dataset contains information on 3,390 individuals with 16 predictor variables and 1 target variable. Each variable (attribute) is a potential risk factor. 
There are demographic, behavioral, and medical risk factors. We were tasked to predict the 10-year risk of developing coronary heart disease (CHD).

After understanding the data and getting variables, we first gathered and cleaned the data, handled the null values by checking the distribution and outliers in the data after that we have also typecasted the needed features into required format by type casting in order to visualize them properly. We performed indepth EDA and plotted different types of graphs by separating them into univariate, bivariate and multivariate categories as a result, We came accross some meaningful insights that helped us to make future decisions of ML model pipeline. Then further on, using feature engineering and data preprocessing we have extracted new features like pulse_pressure and glucose_diabetes with the help of some features which are not directly impacting to tenYearCHD. We also tried to get some impacting features by removing multicollinearity within the independent variables with the help of various inflation factor(VIF). In this dataset we have not handled outliers as removing them could potentially lead to a loss of important information and biased results. Also, we noticed that some of the features were categorical in nature and ML model can not understand the language of alphabets(strings).So, we have encoded them into numericals using BINARY LABEL ENCODING .

In order to get normally distributed data we have applied various transformation techniques such as Logarithmic Transformation, Exponential Transformation, Square root Transformation and some others as well and plotted the quantie-quantile plot to visualize how far our data points are from the normal distribution.To scale the data We used the sklearn library StandardScaler.

It was an highly imbalanced dataset as the distribution of the target variable, TenYearCHD, was found to be imbalanced, with only 15% of individuals being classified as having a high risk of developing CHD. So we used SMOTE(Synthetic Minority Oversampling Technique) to create a balanced dataset.

## Business Problem Statement 
The dataset is from ongoing cardiovascular study on residents of the town of Framingham, Massachutts. The classification goal is to predict whether the patient has a 10-year risk of failure coronary heart disease(CHD). The dataset provides the patient's information . It includes over 4000 records and 15 attributes. Each attribute is a potental risk factor. There are both demographic, behavioral, and medical risk factor.

### project dataset summary
* sex - Gender
* age - Age
* is_smoking - Wether smoking currently or not
* CigsPerDay - Cigerettes smoked per day
* BPMeds - Wether takes BP medicines or not
* PrevalenStroke - if the patient has history of strokes 
* PrevalentHyp - if the patient has history of hypertension
* Diabetes - Wethe person has diabetes or not
* totChol - Cholestrole measure
* sysBP - Systolic blood pressure
* DiBP - Diastolic blood pressure
* BMI - Body mass index
* heartRate - Heart rate of individual

### Machine learning model 
- Logistic Regression
- Random Forest Classifier
- Naive Bayes Classifier
- K - Nearest Neighbors Classifer
- Support Vector Machine Classifer
- 
### Which model you choose and why ?
As a result, I chosen the Random Forest classifier as the preferred model for our cardiovascular disease classification task. We believe this model provides a robust and reliable solution, minimizing the risk of false negatives and ensuring that individuals at risk receive the necessary medical attention.

## **Conclusion :**
  - **In this dataset**, 56.7% of individuals are female and rest are male. 50.24% of the individual in the dataset are smoke. Only 2.9% people are taking BP Medicines. 0.6% people had a history of strokes and 31.5 % hypertension respectively. 2.6% people have diabetes. 15.1% people have a chance of getting heart diseases in ten years.
     - Individual with cholestrol which having diabetes and individual with cholestrol not having diabetes having equal change of having risk of CHD.
     - Residents who are at education Level-1 are having slightly more percentage of getting suffered from CHD as compared to other education levels.
     - Individual with high glucose has risk of having cardiovascular disease, which increase the chance of diabetic patient to has risk of cardiovascular disease.
     - Patient who are on BP medication are having high sysBP and diaBP.Even these patients are having high chances of getting suffered from CHD.
     - The patient with high heart rate who is on BP medication has high risk of having Cardiovascular disease.

  - **Implemented five machine learning models** Logistic regression, Random forest, Naive bayes, Support vecor machine and KNN.
     - Considered Random forest classifier as our final optimal model as we are getting highest recall, precision, f1 score, accuracy and auc-roc score from it.
     - Out of 1152 patients our optimal model is correcly predicting 513 of class 0 and 462 of class 1 patients, other 90 and 87 are FN and FP cases.
     - *Age, pulse_pressure, education and Bpmeds* are the **highest contributing features** towards the predictions.
     - Best parameters of Random forest classifier found out to be learning_rate: 0.1, max_depth: 10 and n_estimators: 300.
