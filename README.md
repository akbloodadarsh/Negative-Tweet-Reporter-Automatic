# Negative-Tweet-Reporter(GUI)

## How to use 
#### 1. Insert Your Twitter Credentials in `TwitterCredentials.py`
#### 2. Run the `test.py`
#### 3. Enter the hashtag you want to target.Ex:- #NameOfHashtag
#### 4. Let the program fetch and analyse the tweets and it will automatically report them
#### 5. The cycle will continue until it reaches the maximum extraction limit


**Note:-** 
- The program will fetch 10 tweets at a time.
- Their is a limit of 3200 because Twitter allows a maximum of 3200 tweets for extraction currently.
- If program encounter a negative tweet, it will automatically report it.
- The program is only fetching the tweets which are using english language.

# File Details

<a href="https://github.com/akbloodadarsh/Negative-Tweet-Reporter-Automatic/blob/master/PreProcess.py">Preprocess.py</a>: It contains preprocessing function whihc performs following steps:- 
- It is getting the tweet  
- Removes url using regular expression.
- Removes emoticons using regular expression.
- Removes username using regular expression.
- Removes digit using regular expression.
- Convert more than 2 letter repetitions to 2 letter.
- Removes symbols.
- Removes extra white spaces.
- Return preprocessed tweet.

<a href="https://github.com/akbloodadarsh/Negative-Tweet-Reporter-Automatic/blob/master/twitter_credentials.py">twitter_credentials.py</a>: 
In this file we store our access token,access token secret, consumer key and consumer secret.



