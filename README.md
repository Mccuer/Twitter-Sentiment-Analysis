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
*Reshaping Data - The dataset required reshaping so that it matched the shape of the mode. Early on I was recieving a graph execution error, this solved that problem. This section also involved making sure that each training set had an equal portial of positive and negative data.

#### *Encoding and Preprocessing*
Encoding and preprocessing text data are pivotal steps in transforming words into numerical representations, enabling machine learning models to interpret language. Techniques like tokenization, vectorization, and normalization convert raw text into structured formats, capturing semantic meaning and patterns. These methods, essential for text modeling, ensure that models effectively process and extract insights from textual information, empowering the data modeling to predict accurately.

#### *Data Modeling*
The model I created takes tweet values as the input. After this data is tokenized, it is encoded to allow the sentences to have meaning and context. This allows for the model to be trained in order to make predictions. The model was then given two metrics, accuracy and precision. These metrics allow for the most insight on the quality of the model. Once the model was created it was compiled and then trained.

#### *Data Training*
The model was trained with a variety of inputs. The highest accuracy seen was about 55%, but this yielded a low level of percision. The final model is slighly less accurate, at 49%, but has a high level of precision at 100%.  
![Alt Text](https://github.com/Mccuer/Twitter-Sentiment-Analysis/blob/main/graph/Model-Training-Data.png)

## Results
Prior to training and testing I wanted to gain a better idea of breakdown and sentiment of the dataset. There were 2 key questions that helped me gain this insight.
**What is the breakdown of tweets in the dataset based on sentiment?*

The dataset was broken down by 4 catagories:
*Positive
*Negative
*Nuetral
*Irrelivent
Since the Irrelivent catagory does not add much nuance to this analysis I dropped those rows. When I graphed the data it was clear the dataset was mostly evenly split. Although all catagories were close in amount of tweets, negative had slighly more, followed by positive and then nuetral. This makes sense considering that randomly scraped data should have a variety of sentiment. 
![Alt Text](https://github.com/Mccuer/Twitter-Sentiment-Analysis/blob/main/graph/Tweet_Sentiment_Breakdown_TrainingData.png)

**What topics are most frequent when tweets are broken down by sentiment?*
*Positive Topics
When looking at positive topics, there was one topic that stood out among the rest. Assasins Creed topped the list, which makes sense considering the loyal fan base that the game has. Four topics followed behind, all similarly discussed. these topics were the PS5, Borderlands, Red Dead Redemption, and Cyberpunk 2077. These topics share much in common. The main contributing factors are that they were released close to when the dataset was created, and that they were all very well revieved products.

*Negative Topics
Negative topics seemed to have much less of a correlation when compared to the positive counterparts. Topics that had the most negative discourse included Johnson&Johnson, Nvidia, Apex Legends, Amazon, and World of Warcraft. A major difference between the positive topics is tha appearence of J&J and Amazon. These companies are not aligned in the gaming industry and instead offer healthcare/pharma products and direct to consumer goods.

*Nuetral Topics
Nuetral Topics seemed to be dominated by sporting based games, with Fifa, NBA 2k, and Madden all making the top 5 list. This section was rounded out by 2 topics that contained an overwealming amount of nuetral tweets. This topics were Verizon and Tom Clancey's Rainbow 6 Siege.

![Alt Text](https://github.com/Mccuer/Twitter-Sentiment-Analysis/blob/main/graph/Topic-Breakdown-by-Sentiment.png)


**Testing Results*
When the model was tested against the validation data, in performed worse then expected. The biggest surprise was the drop in percision to 62%. When comparing this to the training data it is a stark difference. I believe the biggest downfall of the model comes from encoding, which could be limiting the power of the model.
![Alt Text](https://github.com/Mccuer/Twitter-Sentiment-Analysis/blob/main/graph/Testing-Result.png)


## Discussion
Overall the model provided interesting information about how people are speaking about a variety of topics on twitter. This information has a wide amount of applications. The biggest real world use case would be being able to see how your brand is being discusses, and using predictive modeling to eliminate needing someone to sit through and sort millions of tweets by hand. This offers a level of automation and predictability that would be valuable to many companies. This project laid the groundwork for being able to itterate and provide more and more accurate models.
