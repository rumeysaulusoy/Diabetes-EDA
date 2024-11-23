![DIABETES EDA   PREDICTION](https://github.com/user-attachments/assets/f36a8c7e-ed41-4ff3-832d-f2e2880977c8)

The Diabetes Dataset is a collection of health-related information used to predict the likelihood of diabetes in individuals. It contains a mix of numerical and categorical features that describe various physical and clinical attributes.

Diabetes Dataset: www.kaggle.com/datasets/prosperchuks/health-dataset?select=diabetes_data.csv

## Variable Details

Age: Represents the age group of the patient. The "13-level age category (_AGEG5YR)" is a classification that categorizes the population into age ranges. (1: 18-24, 2: 25-29, 3: 30-34, 4: 35-39, 5: 40-44, 6: 45-49, 7: 50-54, 8: 55-59, 9: 60-64, 10: 65-69, 11: 70-74, -12: 75-79, 13: 80 and above)

Sex: The gender of the patient. (0: Female, 1: Male)

HighChol: Indicates the high cholesterol status of the patient. (0: No, 1: Yes)

CholCheck: Indicates whether the patient has had a cholesterol test in the past 5 years. (0: No, 1: Yes)

BMI: The Body Mass Index (BMI) of the patient.

Smoker: Indicates whether the patient has smoked at least 100 cigarettes in their lifetime. (0: No, 1: Yes)

HeartDiseaseorAttack: Indicates whether the patient has ever had coronary heart disease or myocardial infarction. (0: No, 1: Yes)

PhysActivity: Indicates whether the patient has engaged in physical activity outside of work in the past 30 days. (0: No, 1: Yes)

Fruits: Indicates whether the patient has consumed one or more fruits during the day. (0: No, 1: Yes)

Veggies: Indicates whether the patient has consumed one or more vegetables during the day. (0: No, 1: Yes)

HvyAlcoholConsmp: Indicates whether adult males consume 14 or more alcoholic drinks per week, and adult females consume 7 or more alcoholic drinks per week. (0: No, 1: Yes)

GenHlth: The patient's self-rated health status on a scale of 1 to 5. (1: Excellent, 2: Very good, 3: Good, 4: Fair, 5: Poor)

MentHlth: The number of days the patient experienced mental health issues in the past 30 days.

PhysHlth: The number of days the patient experienced physical illness or injury in the past 30 days.

DiffWalk: Indicates whether the patient has difficulty walking or climbing stairs. (0: No, 1: Yes)

Stroke: Indicates whether the patient has had a stroke. (0: No, 1: Yes)

HighBP: Indicates whether the patient has high blood pressure. (0: No, 1: Yes)

Diabetes: Indicates whether the patient has diabetes. (0: No, 1: Yes)

 All variables in the dataset are of the data type float64.

## Analysis and Conclusions

- The dataset contains 18 columns, with 70,692 records for each column.

- Categorical columns with numerical features include: Sex, HighChol, CholCheck, Smoker, HeartDiseaseorAttack, PhysActivity, Fruits, Veggies, HvyAlcoholConsmp, DiffWalk, Stroke, HighBP, Diabetes, GenHlth, and Age.

- Numerical columns include: BMI, MentHlth, and PhysHlth.

- The dataset does not contain missing values. Missing values added using the random library were filled with the mean for numerical columns and with the mode for categorical columns.

  **Age**

- The minimum age is 18-24, and the maximum age is 80 and above. This indicates that the dataset only contains adult patients.

- The average age of patients with diabetes is higher than that of patients without diabetes. A direct correlation between age and the likelihood of having diabetes has been observed.

  **Sex**

- The number of male patients in the dataset is higher than that of female patients.

- The diabetes rate for males is slightly higher. No direct connection between sex and diabetes is observed.

  **HighChol & CholCheck**

- The significant majority of patients in the dataset have had a cholesterol test (CholCheck) in the last five years. More than half of the patients have been diagnosed with high cholesterol. When considering only those who had the test in the last five years, the proportion shows very little change, and since there is no connection between this variable and diabetes or other factors, it has been removed from the dataset.

- Since the rate of high cholesterol is higher in patients with diabetes, a direct correlation between high cholesterol and the likelihood of having diabetes has been observed.

  **BMI**

- The minimum BMI is in the underweight range, while the maximum BMI is in the extreme obesity range.

- Unlike patients without diabetes, the BMI distribution in patients with diabetes is observed to fall within the overweight and obese ranges, indicating a direct correlation between BMI and the likelihood of having diabetes.

  **Smoker**

- Less than half of the patients in the dataset have smoked at least 100 cigarettes.

- Since no significant difference was observed between diabetic and non-diabetic patients regarding smoking, it has been observed that there is no direct connection between smoking and diabetes.

  **HeartDiseaseorAttack**

- A small portion of the patients in the dataset have had a history of heart disease or a heart attack.

- The majority of patients with diabetes who have not had heart disease suggests that there is no direct connection between heart disease and diabetes.

  **PhysActivity**

- Most of the patients in the dataset have engaged in physical activity outside of work in the past 30 days.

- Although physical activity may reduce the risk of diabetes, no direct connection between physical activity and diabetes has been observed.

  **Fruits & Veggie**

- More than half of the patients in the dataset consume one or more servings of fruit per day. Since there is no significant difference in fruit consumption between diabetic and non-diabetic patients, no direct connection between fruit consumption and diabetes has been observed.

- Most patients in the dataset consume one or more servings of vegetables per day. Since there is no significant difference in vegetable consumption between diabetic and non-diabetic patients, no direct connection between vegetable consumption and diabetes has been observed.

- A high correlation has been observed between fruit and vegetable consumption. Since they impact diabetes in similar proportions, these two variables have been combined to create a new variable named Fruit_Veggie_Consumption.

  **HvyAlcoholConsmp**

- A very small portion of the patients in the dataset consume high amounts of alcohol.

- Since the majority of diabetic patients do not consume high amounts of alcohol, no direct connection between high alcohol consumption and diabetes has been observed.

  **GenHlth & MentHlth & PhysHlth**

- The general health status of patients in the dataset is generally rated between 'very good' and 'good.' The distribution of diabetic patients' general health status is positioned between 'good' and 'fair,' while the distribution of non-diabetic patients is positioned between 'very good' and 'good.

- The average number of days patients experienced mental health issues in the past 30 days is low. Since diabetic patients also have a low number of days with mental health issues, no direct connection between mental health information and diabetes has been observed.

- The average number of days patients experienced physical health issues in the past 30 days is moderate. A difference was observed in the distribution of diabetic and non-diabetic patients, suggesting a direct correlation between the likelihood of diabetes and physical health issues.

- Since there is a high correlation between the GenHlth, MentHlth, and PhysHlth variables, GenHlth has been retained as a representative variable, and the other two variables have been removed from the dataset."

  **DiffWalk**

- A small portion of the patients in the dataset reported difficulty walking. Since the majority of diabetic patients do not experience difficulty walking, it has been observed that there is no direct connection between difficulty walking and diabetes.

  **Stroke**

- A very small portion of the patients in the dataset have had a stroke. Since this rate is also very low among diabetic patients, it has been determined that there is no direct connection between stroke and diabetes.

  **HighBP**

- More than half of the patients in the dataset have high blood pressure. Since this rate is also high among diabetic patients, a direct correlation between high blood pressure and the likelihood of having diabetes has been observed.

  **Diabetes**

- The target variable is diabetes. The proportion of diabetic and non-diabetic patients in the dataset is similar. HighBp, GenHlth, BMI, Age, and HighChol are among the most important variables for predicting diabetes.


- As a result, after making changes to the variables a model was built using Gradient Boosting, and the accuracy of this model is approximately 75%. The model's ability to identify non-diabetic patients is slightly higher than its ability to identify diabetic patients. This is thought to be due to data imbalance.


Kaggle Notebook Link: https://www.kaggle.com/code/rumeysaulusoy/diabetes-eda-prediction
