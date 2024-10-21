I have worked on the Healthcare Dataset Project.The purpose of this dataset is to help predict whether a patient has diabetes based on a variety of medical factors. The dataset includes several medical test results (such as Urea, HbA1c, Cholesterol levels, etc.) and demographic information (age, gender), and the goal is to classify whether the patient is diabetic or not (indicated by the CLASS column).

  ID: This is just a unique identifier for each patient and won’t be needed for analysis or modeling.

  No_Pation: Another identifier that might not add value in predicting diabetes. We’ll check if this can be removed.

  Gender: Categorical variable with male (M) and female (F) values. We would have to fix the values for Gender.

  AGE: Continuous variable representing the age of the patient.

  Urea, Cr, HbA1c, Chol, TG, HDL, LDL, VLDL: These are various medical test results, which might be important in diagnosing diabetes. We'll analyze each in detail during EDA.

  BMI: Body Mass Index, which is likely an important predictor for diabetes.

  CLASS: This is the target variable (diabetic or non-diabetic). It’s categorical with Y (Yes, diabetic) and N (No, non-diabetic).

I have performed Exploratory Data Analytics in the collab notebook like checking for missing values, duplicate values, changing the datatypes, imbalance check, correlation analysis,
visualizations for better analysis.

After the EDA, I inferred that age group between 50-55 is most likely to be diabetic. The count plot of Gender shows that there are more female patients reported than male so there might be a bias if we make predication according to gender. From the correlation heatmap, we can visualise that Cr and Urea are most highly correlated.

Moving ahead, I carried ML modelling in the collab notebook. The ML models that I used are LR,KNN,NB,SVC,RFC,DTR,XGB.

Using this, a binary classification problem was solved by predicting whether a patient has diabetes (`Y` or `N`) based on medical and demographic data. I trained multiple models to tackle this classification task. Another key issue addressed was the imbalance in the dataset, where diabetic patients were more prevalent than non-diabetic ones, which required careful model evaluation using precision, recall, and F1-score to ensure fair predictions for both classes. To ensure the models generalized well to new data, I also split the dataset into training and testing sets, ultimately selecting the best-performing model based on a variety of evaluation metrics.

 To evaluate our model, we have split the dataset into training and testing data and also performed cross-validation to check if the model can generalize well to unseen data. Then we created a classification report to find the best-performing model.

The best performing model is XGB as it had the maximum accuracy score based on the cross-validation results, hence giving the most accurate prediction.
