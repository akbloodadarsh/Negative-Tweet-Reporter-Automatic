# Negative-Tweet-Reporter(GUI)

## How to use 
#### 1. Insert Your Twitter Credentials in `TwitterCredentials.py`
#### 2. Run the `test.py`
#### 3. Enter the hashtag you want to target.Ex:- #NameOfHashtag
#### 4. Let the program fetch and analyse the tweets and it will automatically report them
#### 5. The cycle will continue until it reaches the maximum extraction limit


**Note:-** 
- The program will fetch 10 tweets at a time.
- There is a limit of 3200 because Twitter allows a maximum of 3200 tweets for extraction currently.
- If the program encounters a negative tweet, it will automatically report it.
- The program is only fetching the tweets which are using the English language.

# File Details

<a href="https://github.com/akbloodadarsh/Negative-Tweet-Reporter-Automatic/blob/master/PreProcess.py">Preprocess.py</a>: It contains preprocessing function which performs following steps:- 
- It is getting the tweet  
- Removes URL using a regular expression.
- Removes emoticons using a regular expression.
- Removes username using a regular expression.
- Removes digit using a regular expression.
- Convert more than 2 letter repetitions to 2 letters.
- Removes symbols.
- Removes extra white spaces.
- Return preprocessed tweet.

<a href="https://github.com/akbloodadarsh/Negative-Tweet-Reporter-Automatic/blob/master/twitter_credentials.py">twitter_credentials.py</a>: 
In this file we store our access token,access token secret, consumer key and consumer secret.

<a href="https://github.com/akbloodadarsh/Negative-Tweet-Reporter-Automatic/blob/master/test.py.py">test.py</a>: 
- The TwitterAuthenticator class inherits the OAuthHandler class and passes in the credentials to allow access to Twitter’s API features.
- The TwitterClient class contains all the methods to interact with Twitter API and parsing tweets. Use __init__ function to handle the authentication of the API client.
- Create a object of class TwitterClient() and use the object to get twitter client API using get_twitter_client_api() function.
- create a window using Tkinter and let the user input the hashtag.
- Use API to search for the tweets of the inputted hashtag and store the tweets.
- Extract the labels and sentences and store the outcomes in y and after preprocessing the tweets store them in x.
- Then used count Vectorizer to lowercases text, performed tokenization (converts raw text to smaller units of text), used word-level tokenization (meaning each word is treated as a separate token), ignored single characters during tokenization.
- Now one iterate the tweets and one by one preprocess and transform the tweets and do predictions.

<a href="https://github.com/akbloodadarsh/Negative-Tweet-Reporter-Automatic/blob/master/twitter_credentials.py">twitter_credentials.py</a>: 
In this file we store our access token,access token secret, consumer key and consumer secret.

<a href="https://github.com/akbloodadarsh/Negative-Tweet-Reporter-Automatic/blob/master/MultinomialNaiveBayes.py">MultinomialNaiveBayes.py use </a>: 
This file contains the function in which we get training data testing data with features we for which we have to predict our sentiment.
We use naive Bayes to predict our sentiment and then return negative or positive emotions and in main if we got negative then we will report it using report_spam function present in the API by passing the username in it.
