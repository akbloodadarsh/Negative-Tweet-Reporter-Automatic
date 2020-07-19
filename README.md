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

<a href="https://github.com/akbloodadarsh/Negative-Tweet-Reporter-Automatic/blob/master/test.py.py">test.py</a>: 
- The TwitterAuthenticator class inherits the OAuthHandler class and passes in the credentials to allow access to Twitter’s API features.
- The TwitterClient class contains all the methods to interact with Twitter API and parsing tweets. Use __init__ function to handle the authentication of API client.
- Create a object of class TwitterClient() and use the objetc to get twitter client api using get_twitter_client_api() function.
- create a window using tkinter and let the user input the hashtag.
- Use api to search for the tweets of inputted hastag and store the tweets.
- Extract the labels and sentences and store the outcomes in y and after preprocessing the tweets store them in x.
- Then used count Vectorizer to lowercases text,performed tokenization (converts raw text to smaller units of text),used word level tokenization (meaning each word is treated as a separate token),ignored single characters during tokenization.
- Now one iterate the tweets and one by one preprocess and transform the tweets and do predictions.

<a href="https://github.com/akbloodadarsh/Negative-Tweet-Reporter-Automatic/blob/master/twitter_credentials.py">twitter_credentials.py</a>: 
In this file we store our access token,access token secret, consumer key and consumer secret.
