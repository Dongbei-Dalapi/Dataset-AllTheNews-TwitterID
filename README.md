# Dataset-AllTheNews-TwitterID
This dataset provides the twitter ID and the tweets from Kaggle-all-the-news dataset, which can be used for authorship attribution tasks. \
There are only twitter ID of the authors who has more than 30 articles (about 600 authors) in [all the news](https://www.kaggle.com/snapcrack/all-the-news#)
I had checked the description of each account manually. However, these ids might still be incorrect.  \
&nbsp;

## File Description
twitter_id.json : {"Author Name1": TwitterID1, "Author Name2": TwitterID2 ...} \
twitter_id.csv : twitter name and id in csv file \
tweets.json: {"Author Name1": [[tweet1-date, tweet1], [tweet2-date, tweet2]...], "Author Name2": [[tweet1-date, tweet1], [tweet2-date, tweet2]...] ...} 

## Load the dictionary - example in Python
```
>>>import json
>>>tweets_dict = json.load(open('tweets.json'))
>>>tweets_dict['Maggie Haberman'][0][0]
'2021-02-13'
>>>id_dict = json.load(open('twitter_id.json'))
>>>id_dict['Maggie Haberman']
'@maggieNYT'
```
