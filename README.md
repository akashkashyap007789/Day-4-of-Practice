# Day 4 — Working With ColumnTransformer (Imputation + Encoding)

Today’s task was to take a mixed-type dataset (covid_toy.csv) and build a preprocessing pipeline using ColumnTransformer.
Goal: handle missing values, encode categorical columns, and prepare the data for model training.

🔧 Steps Completed
1. Loaded the dataset

Target column: has_covid

Features include numerical + categorical data

2. Performed Train-Test Split
X_train, X_test, y_train, y_test = train_test_split(
    df.drop(columns=['has_covid']), 
    df['has_covid'], 
    test_size=0.2
)

3. Applied ColumnTransformer

Components used:

SimpleImputer → for numerical column: fever

OrdinalEncoder → for ordered category: cough (Mild < Strong)

OneHotEncoder → for nominal categories: gender, city (drop='first')

remainder='passthrough' → keep untouched columns

4. Output Shapes

transformer.fit_transform(X_train).shape

transformer.transform(X_test).shape

Shows the final encoded feature space.
