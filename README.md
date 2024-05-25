# Social Media Analytics
![Valorant](images/valorant_banner.jpg)

social media analytics for Riot Gaming, Conducted sentiment analysis on gamers' discussions from Reddit utilizing the Google BERT model, and Llama2 through LangChain. Leveraged PRAW for data extraction and applied LDA Topic Modeling to identify topics within positive and negative sentiment labels, aiming to optimize player satisfaction and retention strategies. 
## Introduction
This project aims to analyze gamer discussions on Reddit regarding the popular game Valorant by Riot Games. We focused on player sentiments towards the introduction of a new agent, Clove, and conducted comprehensive sentiment analysis and topic modeling. Our goal is to optimize player satisfaction and retention strategies through data-driven insights.

## Table of Contents
1. [Introduction](#introduction)
2. [Problem Statement](#problem-statement)
3. [Data Collection](#data-collection)
4. [Data Preprocessing](#data-preprocessing)
5. [Sentiment Analysis](#sentiment-analysis)
6. [Topic Modeling](#topic-modeling)
7. [Insights](#insights)
8. [Future Scope](#future-scope)
9. [Conclusion](#conclusion)
10. [Contributors](#contributors)

## Problem Statement
We aimed to understand players' reactions to the new agent Clove before and after its release on March 26, 2024. The analysis was conducted by scraping Reddit comments and performing sentiment analysis to uncover player sentiments and key discussion topics.

## Data Collection
We used the PRAW (Python Reddit API Wrapper) library to collect user-generated comments from the following subreddits:
- r/Valorant
- r/ValorantCompetitive
- r/ValorantPBE
- r/ValorantClips
- r/Eggwick

![Data Collection](images/data_collection.png)

[Data Collection Code](https://github.com/yourusername/valorant-analytics/blob/main/data_collection.py)

## Data Preprocessing
The preprocessing phase involved:
- Lowercasing text
- Tokenization
- Removing punctuation and stopwords
- Lemmatization

![Data Preprocessing](images/data_preprocessing.png)

[Preprocessing Code](https://github.com/yourusername/valorant-analytics/blob/main/preprocessing.py)

## Sentiment Analysis
We employed Google BERT and Llama 2 models to conduct sentiment analysis on the preprocessed data.

### BERT Model
- **Training Data:** IMDB Dataset
- **Challenges:** Longer execution time and context mismatch

### Llama 2 Model
- **Setup:** Ollama and LangChain
- **Challenges:** High CPU utilization and model download issues

![Sentiment Analysis](images/sentiment_analysis.png)

[Sentiment Analysis Code](https://github.com/yourusername/valorant-analytics/blob/main/sentiment_analysis.py)

## Topic Modeling
We used Latent Dirichlet Allocation (LDA) to identify topics within different sentiment groups (positive and negative) before and after Clove's release.

![Topic Modeling](images/topic_modeling.png)

[Topic Modeling Code](https://github.com/yourusername/valorant-analytics/blob/main/topic_modeling.py)

## Insights
### Pre-Release Positive Comments
- **Keywords:** great, aggressive, cool

### Pre-Release Negative Comments
- **Keywords:** hype, useless

### Post-Release Positive Comments
- **Keywords:** ult, ability, duelist

### Post-Release Negative Comments
- **Keywords:** smoke, team, lurk

![WordCloud](images/wordcloud.png)

## Future Scope
- **Automated Data Retrieval:** Deploy API wrappers on remote VMs
- **Enhanced Data Collection:** Include more pre-release data and explore other social media platforms
- **Advanced Data Processing:** Implement refined keyword filtering and advanced algorithms
- **Optimized Data Management:** Consider NoSQL for scalability

## Conclusion
The analysis provided valuable insights into player sentiments and discussions surrounding the new agent Clove, which can help Riot Games improve player satisfaction and retention strategies. The consistent themes and evolving discussions indicate areas for future focus and enhancement.


[View Full Presentation](https://github.com/yourusername/valorant-analytics/blob/main/Team2_Valorant.pptx)

### [PRAW Code](https://github.com/saisadhan/Social-Media-Analytics/blob/d0b7455c04de8599c844df9d40d5fcfa6a5ed1ae/PRAW%20(Python%20Reddit%20API%20Wrapper)%20Code.ipynb)
 This Python script utilizes the PRAW (Python Reddit API Wrapper) library to collect user-generated comments from specified subreddits on Reddit. It streams comments in real-time, extracts relevant information such as comment ID, author, timestamp, thread ID, thread title, message body, and permalink, and writes this data to a CSV file. The script is designed to be flexible, allowing users to specify the subreddit(s) they want to collect data from and customize the output format.

### [Text Preprocessing in NLP with Python codes](https://github.com/saisadhan/Social-Media-Analytics/blob/cab37945764cae015441f2c39218494b6205cb09/text_preprocessing.ipynb)

This above Python script imports data from a CSV file, preprocesses each message by lowercasing, tokenizing, removing punctuation and stopwords, and lemmatizing the words. The processed text is then saved to a CSV file for further analysis. This code streamlines the initial steps of text data preparation, facilitating efficient analysis of social media content.

### [Latent Dirichlet allocation Topic Modelling](https://github.com/saisadhan/Social-Media-Analytics/blob/f4903a564fd7c4ccba74ec924a72520b4394cc62/Latent%20Dirichlet%20allocation.ipynb)

The script utilizes Latent Dirichlet Allocation (LDA) to uncover latent topics within the extracted dataset. It imports Reddit data from a CSV file, preprocesses it, and generates a document-term matrix. Then, it applies LDA to identify topics and prints the top words associated with each topic. The script facilitates insightful analysis of social media discussions by revealing underlying themes present in the data.
