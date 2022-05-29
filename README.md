# Lookalike Modeling using Locality-Sensitive Hashing Technique

This repository contains the code for the lookalike model using LSH approach on a subset of [Adform Click Prediction Dataset](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/TADBY7).

### Installation

To install the dependencies run:
```
pip install -r requirements.txt
```

### Adform Click Prediction Dataset
The dataset from Adform consists consists of user records from a particular online advertisement campaign. The dataset contains 10 features. All the features are hashed to preserve privacy. The features include a couple of features that can have multiple values per user. The dataset also has a label column indicating whether the user clicked on the ad or not.

A subset of the Adform dataset is selected and placed inside the `data` folder. We use a subset since the dataset is extremely large and requires lot of computing power.


### Cleaning the dataset
To clean the data, run:
```
python processing.py
```
The cleaning step involves the following steps:
1) Convert all columns except column that can have multiple values to integer
2) Remove user records having number of values in the list columns more than a threshold value
3) Replace null values in list columns with empty list
### Train the model

To train the model, run:
```
python train.py
```

### Use the model to make predictions
To get extended users from a seed set, run:
```
python extend.py
```
