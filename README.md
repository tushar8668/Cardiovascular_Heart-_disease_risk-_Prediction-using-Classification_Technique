# Cardiovascular_Heart-_disease_risk-_Prediction-using-Classification_Technique
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
