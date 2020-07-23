## Defining user segmentation in social media through the use Twitter mining

An informed insight of how an individual has influence on others in a circle can help a business create social media campaigns that aid in marketing and advertising. An approach to determine this is summarized here with explanations of how to use tweepy API in python to exctract data and how to use the data obtained
to rank the users. Users are ranked based on their influence.

This blog is among the challenges undertaken at [10 Academy](https://www.10academy.org/)training in July 2020.

## Problem statement
What determines the level of influence a user has on social media?
A study is made to make an understanding of the effects of the social media influencers are in Africa to inform a Social media campaign based on the following factors;

1. Popularity (Retweet Influence): measured by the number of Retweets and Likes users get
2. Reach (Indegree Influence): measured by the size of their audience.
3. Relevance (Mentions Influence): measured by the relevancy of their content.

## Methodology
## Data Extraction
## Webscraping
In exctraction of the data, I scrapped [Africa Influential Tweeter](https://africafreak.com/100-most-influential-twitter-users-in-africa)
and [Africa	leaders response to Corona virus](https://www.atlanticcouncil.org/blogs/africasource/african-leaders-respond-to-coronavirus-ontwitter/#east-africa) websites  to obtain the twitter accounts of the most influential twitter users and top African leaders respectively.
## Twitter mining data.
Next, I use the tweeter API's to extract data for the twitter users obtained.
First, I import needed packages. Tweepy is a must when dealing with data from Twitter. Pandas is always the  best  for munging and process data.
```
import tweepy
import pandas as pd
```
Next I provide four keys/tokens from  my Twitter App Developer as this is  second step for any Tweepy operation.Then I initiate the authentication and pass it with 
Tweepy API to access information about the Twitter handles obtained above
```
#providing twitter Api
consumer_key = (YOUR TWITTER_API_KEY)
consumer_secret = (YOUR TWITTER_API_SECRET)
access_token = ( YOUR TWITTER_ACCESS_TOKEN)
access_token_secret = ( YOUR TWITTER_ACCESS_TOKEN_SECRET)

#Initiating the aunthetication
auth = OAuthHandler(consumer_key, consumer_secret)
auth.set_access_token(access_token, access_token_secret)
self.auth = auth
self.api = tweepy.API(auth, wait_on_rate_limit=True)
```
## Data Processing
In ensuring data quality control, empty entries  were droppped to ensure completeness of the data and correct inference of the results during analysis.
### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/Bessy-Mukaria/Blog_2/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
