# Day 4 — Working With ColumnTransformer (Imputation + Encoding)

Today’s task was to take a mixed-type dataset (covid_toy.csv) and build a preprocessing pipeline using ColumnTransformer.
Goal: handle missing values, encode categorical columns, and prepare the data for model training.

What Was Done

Loaded the dataset containing symptoms and basic information

Separated the target column (has_covid) from the features

Split the data into training and testing parts

Applied three transformations in a single pipeline:

Filled missing values in numerical data

Converted ordered categories like Mild → Strong into numeric form

Applied one-hot encoding to non-ordered categorical columns such as gender and city

Why This Matters

Machine learning algorithms don’t understand raw text or missing values.
This step ensures:

Consistent preprocessing

Clean numeric features

A ready-to-train dataset for the next stage

Less manual work and fewer errors

Output

After the transformations, both the training and test sets were successfully converted into their final numeric form.
The feature shapes confirmed that the pipeline worked exactly as intended.
