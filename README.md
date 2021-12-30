# Article Recommendation Engine for IBM Watson Studio Platform

<p align="center"> 
    <a href="https://cloud.ibm.com/" target="_blank">
    <img src="https://github.com/joshasgard/Article-Recommendation-Engine/blob/master/static/image.jpg" height="500"></img>
  </a>
  </p>

</p>
<h2 align="center"> Article recommendation engines built for IBM Watson's platform users with collaborative filtering, content-based, ranking and knowledge-based techniques! </h2) </p>

 
 # Tools📢✏️
 - Python 3.7 and above, Jupyter Notebook
 - Pandas & Numpy for data manipulations
 - Matplotlib for charts
 - pickle for imports
 - RE and NLTK for natural language processing (tokenization)
 - Sklearn for word vectorization and term frequency-inverse document frequency transformation

    
 
# File Descriptions 📂

- `data` folder - every information on every article available to users on the platform is contained in `articles_community.csv` while tracked 'user-item-interactions.csv` holds all data of how over 5000 users interacted with 714 articles on the platform.
- `Recommendations_with_IBM.ipynb` - raw Jupyer Notebook containing all Python codes showcasing the building process and end results. 
- 'project_tests.py` - python script for testing functions in notebook
- `top_10.p`,  `top_20.p` and  `top_5.p` - pickled data of from notebook of top 10, 20 and 5 articles on the platform
- `user-item-matrix.p` - pickled user to article matrix. 



# Summary 🎯

As I mentioned earlier, I built out different article recommendation systems for the IBM Watson Studio Platform for users on the platform to receive more personalised article recommendations and to mitigate the cold start problem for new users. The Jupyter Notebook containing this work has been divided into sections to improve the readability and structure. 
    
### Exploratory Data Analysis
I explored the data provided by IBM for the project to answer the following questions:

- What is the distribution of how many articles a user interacts with in the dataset?
- The number of unique articles that have an interaction with a user.
- The number of unique articles in the dataset (whether they have any interactions or not).
- The number of unique users in the dataset. (excluding null values)
- The number of user-article interactions in the dataset.
- The most viewed article_id

### Rank-based Recommendations
One way to create recommendations is to rank items (articles) based on existing user rating, but the data provided does not have such information. Hence, we can only assume that the most popular articles are the ones with the most user interactions, i.e. how often an article was interacted with.
This means we created functions to: 
- return the names of top articles with most interactions
- return the IDs of these top article  

### User-User Based Collaborative Filtering 
In order to build better recommendations for the users of IBM's platform, we can explore the similarity of users on the platform based on the range of articles they have interacted with, then we can make recommendations based off of the differences in the most similar users. This is a step towards making more personalised recommendations for the users on the platform. 
Our measure of similarity between the users was found by simply taking vector dot products between users. Here are the major steps I followed to achieve this:

- Re-formatted user-items interaction data to show unique users and articles
- Created a boolean matrix between each user and each article (user-item pairs) to show interaction. 1 for interation, 0 otherwise
- Found similar users based on similarity of their interactions
- Returned article names based on user IDs
- Made recommendations by defining a User-user collaborative Filtering function.
  
### Content-based Recommendations with NLP
Since we have sufficient content information about the articles in our `articles_community.csv` file, there are different ways we can use the article content to find similarities between the articles so we can make recommendations to interested users. 
- Using article titles to find similarity
- Using article description to find similarity
- Using entire article body to find similarity
- Using any combination of the 3 above. 
    
Here, I have opted for a combination of the article titles and description to determine which articles are most similar. I implemented this as follows:
- Wrote a Tokenization function to tokenize the title of each article
- Created df_merged to combine all the articles available on the platform, whether or not any user interacted with the article
- Found similar articles function using the output vector of tfidf class to determine which articles are the most similar to the article
- Wrote a function that performs content recommendations
 
### Matrix Factorization with ML for COLD-START
Lastly, I completed a machine learning approach to building recommendations. Using the user-item interactions, I built out a matrix decomposition with SVD. Using this decomposition, I evaluated how accurate our predictions might be for articles that new users might interact. 
Finally, I discussed which methods we might use for recommending articles on the platform to new users and established users on the IBM Watson Studio Platform. 
    
# Licence 📃
The MIT License (MIT)

Copyright (c) 2021 Idowu Odesanmi. All rights reserved. 

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.. 

# Credits 🚀
* Thanks to <a href = https://cloud.ibm.com/> IBM Watson Studio </a> for making the platform dataset available for use. 
* Project reviewed by <a href = udacity.com> UDACITY </a> Data Science Team
