# EA - Twitter Sentiment Classification
This project entails the creation of a Machine Learning model that is able to classify whether or not a person believes in climate change, based on their novel tweet data. 
## Project Summary
- Cleaned and feature engineered the dataset in order to make it in an optimal form for model prediction 
- Performed Exploratory Data Analysis (EDA) on the data set in order to gain insight from it
- Split the dataset in train and testcset
- Trained several models (Support Vector Machine, Ridge Classifier, Random Forest Classifier, K-Nearest Neighbour and Light Gradient Boosting Machine) using the trained dataset and tested how they performed on the test data set.
- Performed model optimization
- Deployed the solution using Streamlit
### Background Story
Many companies are built around lessening one’s environmental impact or carbon footprint. They offer products and services that are environmentally friendly and sustainable, in line with their values and ideals. They would like to determine how people perceive climate change and whether or not they believe it is a real threat. This would add to their market research efforts in gauging how their product/service may be received.

With this context, EA is challenging you during the Classification Sprint with the task of creating a Machine Learning model that is able to classify whether or not a person believes in climate change, based on their novel tweet data.

Providing an accurate and robust solution to this task gives companies access to a broad base of consumer sentiment, spanning multiple demographic and geographic categories - thus increasing their insights and informing future marketing strategies.

### Data SET:
The collection of this data was funded by a Canada Foundation for Innovation JELF Grant to Chris Bauch, University of Waterloo. The dataset aggregates tweets pertaining to climate change collected between Apr 27, 2015 and Feb 21, 2018. In total, 43,943 tweets were collected. Each tweet is labelled as one of 4 classes, which are described below.

#### Class Description

2 News: the tweet links to factual news about climate change

1 Pro: the tweet supports the belief of man-made climate change

0 Neutral: the tweet neither supports nor refutes the belief of man-made climate change

-1 Anti: the tweet does not believe in man-made climate change Variable definitions

#### Features

sentiment: Which class a tweet belongs in (refer to Class Description above)

message: Tweet body

tweetid: Twitter unique id

### Data Cleaning:
In this stage of the process the following steps were followed to ensure the data was in an apprpriate form that could be fed to the model

- Removal of all punctuation marks
- Removal of all URLs
- Removal of all twitter mentions
- Removal of all special characters (#,&,% etc.)
- Removal of all non-English characters(á, ó etc.)
### Exploratory Data analysis:
This are some of the exploratory analysis that was carried out during the course of the project 

- We plotted bar plots of all the sentiments to see their distribution.This was important to tell if there was any data imbalance
- We made worcloud plots as well as barplots of the top 10 most commonly used words in each sentiment. This was useful in creting insights
### Model Building 
For this project , five different models were used and compared against each other based on the F1-Score performance:
Support Vector Machine: 0.70

Classification Report:

               precision    recall  f1-score   support

          -1       0.83      0.26      0.39       278
           0       0.64      0.34      0.45       425
           1       0.72      0.91      0.81      1755
           2       0.76      0.69      0.73       706

    accuracy                           0.73      3164
    macro avg       0.74      0.55      0.59      3164
    weighted avg       0.73      0.73      0.70      3164


Random Forest: 0.67

Classification Report:

               precision    recall  f1-score   support

          -1       0.82      0.20      0.32       278
           0       0.61      0.33      0.43       425
           1       0.70      0.89      0.78      1755
           2       0.72      0.64      0.68       706

    accuracy                           0.70      3164
    macro avg       0.71      0.51      0.55      3164
    weighted avg       0.70      0.70      0.67      3164


Ridge Classifier: 0.68

Classification Report:

               precision    recall  f1-score   support

          -1       0.61      0.40      0.48       278
           0       0.47      0.41      0.44       425
           1       0.75      0.80      0.77      1755
           2       0.67      0.70      0.68       706

    accuracy                           0.69      3164
    macro avg       0.62      0.58      0.59      3164
    weighted avg       0.68      0.69      0.68      3164


K-Nearest Neighbour: 0.63

Classification Report:

               precision    recall  f1-score   support

          -1       0.85      0.21      0.33       278
           0       0.57      0.33      0.42       425
           1       0.70      0.89      0.78      1755
           2       0.73      0.65      0.69       706

    accuracy                           0.70      3164
    macro avg       0.71      0.52      0.55      3164
    weighted avg       0.70      0.70      0.67      3164


Light Gradient Boosting Machine: 0.68

Classification Report:

               precision    recall  f1-score   support

          -1       0.67      0.32      0.43       278
           0       0.54      0.37      0.44       425
           1       0.72      0.86      0.78      1755
           2       0.70      0.66      0.68       706

    accuracy                           0.70      3164
    macro avg       0.66      0.55      0.58      3164
    weighted avg       0.69      0.70      0.68      3164



This showed that the Support Vector Machine performed better than the other models, although its predictions are stil not perfect.


 
 ### Model Deployment
 Finally!! , the project was deployed using a streamlit app.
 Note: Run the base_app.py file to view the web based application

## Stremlit Application
The we created a a web based application using streamlit.
Streamlit is an open-source app framework for Machine Learning and Data Science uses.

### Functionality
Our application has one type of input and out
  - Input - Text data, which in our case are the tweets
  - Output - The sentiment associated with the input tweet, predicted by our model.
The application then allows the user to classify the tweet using any of 3 different clasiffiers:
  - Support Vector Classifier
  - Ridge Classifier
  - Random Forest Classifier
  
  
