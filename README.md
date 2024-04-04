# Social-Media-Analytics

social media analytics for Riot Gaming, analyzing player sentiment pre and post software patches to optimize game updates, enhancing player retention and satisfaction. Utilizing API scraping and LDA Topic Modeling for data extraction and sentiment analysis from multiple subreddits.

### [PRAW Code](https://github.com/saisadhan/Social-Media-Analytics/blob/d0b7455c04de8599c844df9d40d5fcfa6a5ed1ae/PRAW%20(Python%20Reddit%20API%20Wrapper)%20Code.ipynb)
 This Python script utilizes the PRAW (Python Reddit API Wrapper) library to collect user-generated comments from specified subreddits on Reddit. It streams comments in real-time, extracts relevant information such as comment ID, author, timestamp, thread ID, thread title, message body, and permalink, and writes this data to a CSV file. The script is designed to be flexible, allowing users to specify the subreddit(s) they want to collect data from and customize the output format.

### [Text Preprocessing in NLP with Python codes](https://github.com/saisadhan/Social-Media-Analytics/blob/cab37945764cae015441f2c39218494b6205cb09/text_preprocessing.ipynb)

This above Python script imports data from a CSV file, preprocesses each message by lowercasing, tokenizing, removing punctuation and stopwords, and lemmatizing the words. The processed text is then saved to a CSV file for further analysis. This code streamlines the initial steps of text data preparation, facilitating efficient analysis of social media content.
