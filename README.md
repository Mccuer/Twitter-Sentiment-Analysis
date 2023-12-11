# Twitter-Sentiment-Analysis
## Introduction
Twitter(now referred to commonly as X) is one of the most prolific social medias. What makes Twitter unique to many other social platforms is that it is primarily text based. The language used in tweets is full of useful data. 
By using language modeling we can use the data of tweets in a more robust way. One benifit of this is by sentiment modeling. Sentiment modeling allows us to sort tweets by if they are positive, negative, or nuetral. By feeding the model data from tweets that have been marked by sentiment we can train the model to predict the sentiment of new tweets.

## Dataset
Dataset used: https://www.kaggle.com/datasets/jp797498e/twitter-entity-sentiment-analysis

The dataset I will be using is a compiled dataset of tweets. It contains 2 files, one meant to be used for training and another that is meant to be used for validation. The dataset contains columns for the sentiment, the topic, a tweet id, and the contents of the tweet. The data will need to be cleaned and altered slightly to help with readability but it is very usable and will be perfect for this modeling.

## Methodology
To complete this project I used a variety of libraries including

*TensorFlow - data modeling
*Sklearn - Creating testing and training sets, data encoding and preprocessing
*Pandas - Data manipulation
*Seaborn - Data visualization
*Matplotlib - Data Visualization

All of these libraries were used within a Google Collab Notebook, which allowed for easy and seamless developement. Github was used to share the data as well as for version control.

### Key Steps/Processes

#### *Cleaning the Data*
This dataset required alot of cleaning in order to improve usability and effectivness of the data. There were 3 key points in this portion of the project:
*Cleaning of NULL Values - The data contained several NULL Values that needed to be removed so that they did not inhibit the modeling
*Removing <unk> Values - <unk> values represented characters that could not be read during data collection. To clean these all instances of <unk> were replaced with an empty string
*Reshaping Data - The dataset required reshaping so that it matched the shape of the mode. Early on I was recieving a graph execution error, this solved that problem.

#### *Encoding and Preprocessing*
Encoding and preprocessing text data are pivotal steps in transforming words into numerical representations, enabling machine learning models to interpret language. Techniques like tokenization, vectorization, and normalization convert raw text into structured formats, capturing semantic meaning and patterns. These methods, essential for text modeling, ensure that models effectively process and extract insights from textual information, empowering the data modeling to predict accurately.

#### *Data Modeling*
The model I created takes tweet values as the input. After this data is tokenized, it is encoded to allow the sentences to have meaning and context. This allows for the model to be trained in order to make predictions. The model was then given two metrics, accuracy and precision. These metrics allow for the most insight on the quality of the model. Once the model was created it was compiled and then trained.

#### *Data Training*
The model was trained with a variety of inputs. The highest accuracy seen was about 55%, but this yielded a low level of percision. The final model is slighly less accurate, at 49%, but has a high level of precision at 100%.
!(https://github.com/Mccuer/Twitter-Sentiment-Analysis/blob/main/graph/Model-Training-Data.png)

## Results
What is the breakdown of tweets in the dataset based on sentiment and topic?
What are the most common words in the positive and negative tweets respectivly?
How can we train a model to predict sentiment and how accurate can the model be?
