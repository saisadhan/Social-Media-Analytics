# Social Media Analytics
![Valorant](https://github.com/saisadhan/Social-Media-Analytics/blob/98fcc3791d4ab3c203d16a3a828a5ace0730f90f/valorant_banner.jpg)

social media analytics for Riot Gaming, Conducted sentiment analysis on gamers' discussions from Reddit utilizing the Google BERT model, and Llama2 through LangChain. Leveraged PRAW for data extraction and applied LDA Topic Modeling to identify topics within positive and negative sentiment labels, aiming to optimize player satisfaction and retention strategies. 

## Problem Statement
I aimed to understand players' reactions to the new agent Clove before and after its release on March 26, 2024. The analysis was conducted by scraping Reddit comments and performing sentiment analysis to uncover player sentiments and key discussion topics.

## [Data Mining Code](https://github.com/saisadhan/Social-Media-Analytics/blob/98fcc3791d4ab3c203d16a3a828a5ace0730f90f/PRAW%20(Python%20Reddit%20API%20Wrapper)%20Code.ipynb)
I used the PRAW (Python Reddit API Wrapper) library to collect Reddit's user comments from the following subreddits:
- r/Valorant
- r/ValorantCompetitive
- r/ValorantPBE
- r/ValorantClips
- r/Eggwick

### [Text Preprocessing in NLP with Python codes](https://github.com/saisadhan/Social-Media-Analytics/blob/cab37945764cae015441f2c39218494b6205cb09/text_preprocessing.ipynb)
The preprocessing phase involved:
- Lowercasing text
- Tokenization
- Removing punctuation and stopwords
- Lemmatization

## Sentiment Analysis
I employed Google BERT and Llama 2 models to conduct sentiment analysis on the preprocessed data.

### BERT Model
- **Training Data:** IMDB Dataset
- **Challenges:**
***1. Longer Execution Time:*** Training the BERT model and obtaining predictions was time-consuming.
***2. Context Mismatch:*** Despite using the IMDB dataset for training, we observed some incorrect sentiment predictions during manual checks, likely due to contextual differences between movie reviews and gaming discussions.

### Llama 2 Model
To overcome the above challenges, we shifted to the open-source Llama 2 model. Initially, we attempted to implement it on Google Colab, but faced issues such as the need for multiple dependencies and the requirement for a Colab Pro subscription due to high CPU utilization.

I utilized Ollama to locally pull and run the Llama 2 model. However, I encountered difficulties in processing CSV files directly with Llama 2 for sentiment analysis. To resolve this, I employed ***LangChain***, a framework designed to interact with large language models (LLMs). This setup allowed me to feed data from a CSV file row by row into Llama 2 and store the sentiment predictions back into the CSV file.


# Sentiment Comparison

**Google BERT Results**

<img src="https://github.com/saisadhan/Social-Media-Analytics/blob/06180bcee102fc670cdacc1ae02a097de767d0fd/positive%20percentage%20comparison%20before%20and%20after%20release%20using%20BERT.jpeg" width="400">



**Llama 2 Results**

<img src="https://github.com/saisadhan/Social-Media-Analytics/blob/06180bcee102fc670cdacc1ae02a097de767d0fd/positive%20percentage%20comparison%20before%20and%20after%20release%20using%20Llama2.jpeg" width="400">


### [Latent Dirichlet allocation Topic Modeling](https://github.com/saisadhan/Social-Media-Analytics/blob/f4903a564fd7c4ccba74ec924a72520b4394cc62/Latent%20Dirichlet%20allocation.ipynb)

I used Latent Dirichlet Allocation (LDA) to identify topics within different sentiment groups (positive and negative) before and after Clove's release.

## Insights
### Pre-Release Positive Comments
- **Keywords:** great, aggressive, cool

### Pre-Release Negative Comments
- **Keywords:** hype, useless

### Post-Release Positive Comments
- **Keywords:** ult, ability, duelist

### Post-Release Negative Comments
- **Keywords:** smoke, team, lurk

**Consistent Themes**

1. **"Smoke" as a Focal Point**: Both pre and post-release negative comments emphasize "smoke" as a contentious gameplay element. Players perceive it as affecting visibility and strategy negatively, indicating dissatisfaction with its implementation.

2. **Pronouns and Misgendering**: The recurrent mention of "pronouns" in both negative and positive comments highlights ongoing discussions about gender identity representation. This suggests a need for clearer communication from developers or a more supportive community culture regarding this issue.

**Evolving Discussions**

1. **From Speculation to Experience**: Pre-release comments display a mix of anticipation and skepticism, transitioning to more focused discussions on the agent's abilities and impact on the competitive meta post-release.

2. **Shift in Gameplay Focus**: The prominence of the term "comp" in pre-release negative comments diminishes in post-release discussions. This implies that initial concerns about Clove's fit in competitive play may have been alleviated once players experienced the agent in action.

**Sentiment Improvements**

1. **Increased Positivity in Abilities**: Post-release discussions reflect a positive shift with players discussing "ult" and "ability" more favorably. This suggests that Clove's abilities were well-received and may have exceeded players' expectations.

2. **Recognition as a Duelist**: Post-release, players positively identify Clove as a "duelist," indicating appreciation for the aggressive playstyle the agent enables.

**Areas for Attention**

1. **Community Sensitivity**: The recurring mention of "pronouns" in both positive and negative contexts post-release highlights a need for a more inclusive and sensitive community environment.

2. **Game Balance Concerns**: Negative sentiments surrounding "team" and "lurk" post-release may suggest that Clove has introduced new dynamics perceived as unbalancing team play or encouraging negative gameplay behaviors. These concerns warrant attention from developers to ensure a balanced and enjoyable gaming experience for all players.


## Future Scope
- **Automated Data Retrieval:** Deploy API wrappers on remote VMs
- **Enhanced Data Collection:** Include more pre-release data and explore other social media platforms
- **Advanced Data Processing:** Implement refined keyword filtering and advanced algorithms
- **Optimized Data Management:** Consider NoSQL for scalability

## Conclusion
The analysis provided valuable insights into player sentiments and discussions surrounding the new agent Clove, which can help Riot Games improve player satisfaction and retention strategies. The consistent themes and evolving discussions indicate areas for future focus and enhancement.


## [View Full Presentation](https://github.com/yourusername/valorant-analytics/blob/main/Team2_Valorant.pptx)

