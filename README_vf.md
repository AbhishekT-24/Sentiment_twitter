# Sentiment Analysis Of French Presidential Candidates Using Twitter Data

The Notebook in this project was used to collect, clean, and anlayse
twitter data to analyse the perception of the public on the
presidential candidates for the French elections 2022. While
the current file is specific to this topic, the analysis can
be generalized to any topic that requires similar analysis.

The following has been done in the file:

1. **Data collection using Twint -** For this, we first need
a set of relevant which we want to "scrape" from twitter.
Then, using the twint package available on github, the repository
of all the relevant tweets is made


2. **Data pre-processing -** The next step is to clean the tweets
for all the candidates, for ease of analysis. The following steps are taken:
   1. Any columns which are not required are removed
   2. Equal number of tweets for each candidate to avoid weighting
   3. Each tweet goes through a process of removing punctuations, numbers, mentions, hashtags, links, extra spacing, retweets
   4. The next thing is to look at the emoticons. There are two ways we can deal with them:
      1. Remove the emojis completely
      2. Replace them with text<br/>
   Now the issue here is that the system is not too proficient
   in recognising sarcasm, and emojis are used in an ironic way,
   so it is hard to decrypt the text. That is why, emojis have been
   removed altogether <br/>
      <br/>
   5. Removing stop-words - Stop words are those words
   which do not add much information for the machine. Here,
    the primary languagaes are English, French and Spanish, so the stopwords from those languages are removed
   6. Specific case by case words to be removed - This depends on the search conditions. For example, 
   in this case, the names of the candidates are removed from the tweets, because they will not add any meaning to the analysis
<br/>
<br/>
3. **Sentiment Analysis-** To analyse the tweets, we use
the hugging face's BERT model to "score" the tweets on a scale of 1 to 5,
where 1 = very negative and 5 = very positive. The reason to use
the Bert model is because the model can take many languages and the sentiments can
be classified over a wider range, instead of just 3
<br>
<br>
### Analysis of the sentiment data
Now, after the scores for each tweet for each candidate is received, the next step is to analyse the information.
There are many different analyses one can do, but here, the following have been conducted for each candidate:<br/>

1. Distribution of sentiments
2. Word cloud to see the topics associated with each candidate
3. Generation of top 5 unigrams and bigrams
4. Policy field analysis - here, certain policies were evaluated using keywords. We considered covid, foreign policy, minorities, climate and healthcare.
The sentiment score was then used to see how the public perceives each candidate on these policies
      


