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



### Rank-based Recommendations
    
    
### User-User Based Collaborative Filtering 
    
    
### Content-based Recommendations
    
    
### Matrix Factorization
  


# Licence 📃
The MIT License (MIT)

Copyright (c) 2021 Idowu Odesanmi. All rights reserved. 

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.. 

# Credits 🚀
* Thanks to <a href = https://cloud.ibm.com/> IBM Watson Studio </a> for making the platform dataset available for use. 
* Project reviewed by <a href = udacity.com> UDACITY </a> Data Science Team
