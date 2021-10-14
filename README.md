# Classifying Fake Job Postings

## Project Summary

## Data
The data for this project was taken from [Kaggle](https://www.kaggle.com/shivamb/real-or-fake-fake-jobposting-prediction/code). The original size is 17880 rows by 18 columns.


## Dependencies
```
re
time
numpy
pandas
nltk
sklearn
```

## Project Breakdown
The main files for this project can be found under `notebooks`:

- `1_cleaning_and_wrangling.ipynb`: 
   - Loaded the raw data, conducted some basic inspections for data types and null values. Also consolidated the textual data and cleaned it up by removing stopwords, lowercasing, removing punctuation and applying lemmatizer.
   
- `2_eda.ipynb`:
   - The main finding here was that the data is imbalanced and favors the real job postings.
   
- `3_preprocessing.ipynb`:
   
- `4_modelling.ipynb`:
   - I chose four different models to test out: 
      - Naive Bayes
      - Random Forest
      - Passive Aggressive Classifier
   - Each model was hyperparameter tuned using **GridSearchCV** and a 5 fold cross validation.

A report and presentation for this project can be found in `reports`.


