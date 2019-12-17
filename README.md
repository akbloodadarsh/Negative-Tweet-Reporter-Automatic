# Negative-Tweet-Reporter

#### Follow The Steps
### 1. Insert Your Twitter Credentials in `TwitterCredentials.py`
### 2. Run the `test.py`
### 3. Enter the hashtag you want to target.Ex:- #NameOfHashtag
### 4. Let the program fetch and analyse the tweets and it will automatically report them
### 5. The cycle will continue until it reaches the maximum extraction limit

#### How this is happening

I have used training dataset to train a model using multinomial naive bayes,then we are fetching tweets 10 at a time(Their is a limit of 3200 because Twitter allows a maximum of 3200 tweets for extraction).Then we are using our tained model to analyse the tweets and if it encounter a negative twee the program will automatically report it!And the program will repeat the cycle.
(The program is only fetching the tweets which are using english language) 
