# Classifying Fake Job Postings
<p align="center">
  <img src="./images/fake.png"  width="500" height="200">
</p>

## Project Summary
According to the [FBI](https://www.fbi.gov/contact-us/field-offices/elpaso/news/press-releases/fbi-warns-cyber-criminals-are-using-fake-job-listings-to-target-applicants-personally-identifiable-information) "Fake Job or Employment Scams occur when criminal actors deceive victims into believing they have a job or a potential job. Criminals leverage their position as “employers” to persuade victims to provide them with personally identifiable information (PII), become unwitting money mules, or to send them money." As a matter of fact, as reported from that same FBI article, "16,012 people reported being victims of employment scams in 2020, with losses totaling more than $59 million". These kinds of scams and illegal behaviors are exactly the reasons why companies such as Indeed and Linkedin have put practices into place that limit the the number of fraudulent job postings on their site. 

In this project, I created my own job posting classifier to tag jobs postings as real or fake. This is primarily an NLP project, as I only used textual data for modelling, but I did look at other numerical and categorical features from the original data during EDA. 

 
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
   - Since all of the cleaning and lemmatization was done in the first notebook, all that was left for me to was to convert the data into some numerical format. I decided to go with **TF-IDF** to accomplish this and limited the number of features to 10,000.
   
- `4_modelling.ipynb`:
   - I chose four different models to test out: 
      - Naive Bayes
      - K-Nearest Neighbor
      - Passive Aggressive Classifier
   - Each model was hyperparameter tuned using **GridSearchCV** and a 5 fold cross validation.


## Results


## Future Work
Down the line, I would like to transform this project from being machine learning based to deep learning based. Instead of using TF-IDF for preprocessing, I would like to explore word embedding techniques with tools like **Word2Vec**. I also think it would be useful to use a POS tagger in addition to word tokens.


