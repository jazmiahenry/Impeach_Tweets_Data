# Impeach_Tweets_Data

February 9, 2021 marks the first day of the Second Impeachment Trial of former President Donald J. Trump.
This repository features a dataset of 100,000 tweets taken on the morning of Day 1 of the Impeachment trial in four different forms:

    1. Raw Text Data
    2. Unleaned CSV Data
    3. Cleaned CSV Data
    4. Cleaned and Sentiment Tagged CSV Data

### Raw Text (Impeach_tweets.txt.zip)

Data was collected by Tweet Streaming using Stream Listener from the Tweepy PyPi package coupled with Twitter Developer API access. Source Code for Tweet Streaming is also included in this repository.

### Unleaned CSV Data (Impeach_tweets.csv.zip)

Once data was collected, I transformed the resulting raw txt file of Tweet Data into a Pandas DataFrame with the following columns of information:

* Time Created: Datatime column with time tweet was created
* Tweet Text: Object column with text of tweet
* Source: Object column with tweet source
* Possibly Sensitive: Object column with True, False, or NaN designating if tweet has NSFW content
* Language: Object column with language tweet was written in

### Cleaned CSV Data (Impeach_tweets_clean.csv.zip)

I then cleaned the data of punctuation for ease of textual analysis and data visualization. I also removed all instances of NSFW content in the dataset reducing the dataset from 100,000 tweets to 99,463. Dataset columns:

* Time Created: Datatime column with time tweet was created
* Tweet Text: Object column with text of tweets that have not been flagged as potentially sensitive
* Source: Object column with tweet source
* Possibly Sensitive: Object column with non-NSFW content
* Language: Object column with language tweet was written in

### Cleaned and Sentiment Tagged CSV Data (Impeach_tweets_sentiment.csv.zip)

Lastly, I tagged Sentiment of tweets using the TextBlob package. Dataset columns:

* Time Created: Datatime column with time tweet was created
* Tweet Text: Object column with text of tweet
* Source: Object column with tweet source
* Possibly Sensitive: Object column with True, False, or NaN designating if tweet has NSFW content
* Language: Object column with language tweet was written in
* Polarity: polarity scores of tweets on a -1, 1 scale
* Subjectivity: subjectivity scores of tweets on a -1, 1 scale
* Sentiment: sentiment scores of tweets: negative, positive, and neutral

*Disclamer: NSFW designation is made by Twitter. I did not independently verify NSFW content.*
