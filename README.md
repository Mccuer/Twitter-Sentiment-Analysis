# Twitter-Sentiment-Analysis
## Introduction
Twitter(now referred to commonly as X) is one of the most prolific social medias. What makes Twitter unique to many other social platforms is that it is primarily text based. The language used in tweets is full of useful data. 
By using language modeling we can use the data of tweets in a more robust way. One benifit of this is by sentiment modeling. Sentiment modeling allows us to sort tweets by if they are positive, negative, or nuetral. By feeding the model data from tweets that have been marked by sentiment we can train the model to predict the sentiment of new tweets.

## Dataset
Dataset used: https://www.kaggle.com/datasets/jp797498e/twitter-entity-sentiment-analysis

The dataset I will be using is a compiled dataset of tweets. It contains 2 files, one meant to be used for training and another that is meant to be used for validation. The dataset contains columns for the sentiment, the topic, a tweet id, and the contents of the tweet. The data will need to be cleaned and altered slightly to help with readability but it is very usable and will be perfect for this modeling.

## Methodology
To complete this project I will use Pandas, Numpy, and NLTK(Natural Language Toolkit). This will allow me to analyse the words in each tweet, analyse them, and compare the sentiment to the model that is trained using linear regression modeling.

## Questions
What is the breakdown of tweets in the dataset based on sentiment and topic?
What are the most common words in the positive and negative tweets respectivly?
How can we train a model to predict sentiment and how accurate can the model be?
