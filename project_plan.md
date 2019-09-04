### Projects

[Text Classficiation with Naive Bayes](https://github.com/cs109/2015lab10)
In the mini-project, you'll learn the basics of text analysis using a subset of movie reviews from the rotten tomatoes database. You'll also use a fundamental technique in Bayesian inference, called Naive Bayes. 

[Amazon Product Recommendation System](http://jmcauley.ucsd.edu/data/amazon/)
The Amazon product review datasets contains product reviews and metadata from Amazon, including 142.8 million reviews. We can build a recommendation system using possible tools like [SparkML ALS](https://spark.apache.org/docs/2.2.0/ml-collaborative-filtering.html)
- Read [recommendation system overview Chapter 9](http://infolab.stanford.edu/~ullman/mmds/ch9.pdf)
- Downloading the movies and TV dataset, read and explore it:
```bash
for line in open('Movies_and_TV_5.json','r'): 
     data.append(json.loads(line)) 
```
- Transform the json format into utility matrix table-alike data which contains: userid(row), itemid(col) and rating(values)
- EDA: exploratory data analysis: examine the sparseness of the data, very likely
large amount of less known items(movies) don't have ratings or very few ratings at all.
Plot a distribution of moving rating frequency on log scale, then filter out items that
have very few ratings since those ratings are highly sensitive to individual person preferences.
- Get familiar with the 3 common approaches, [an overview of recommendation system](http://datameetsmedia.com/an-overview-of-recommendation-systems/):
     - content based approach: utilizes a series of discrete characteristics of an item in order to recommend additional items with similar properties, we need to downloa the metadata of the movies to use this approach.
     - collaborative filtering approach:builds a model from a user’s past behaviors (items previously purchased or selected and/or numerical ratings given to those items) as well as similar decisions made by other users. [various implementations of collaborative filtering](https://towardsdatascience.com/various-implementations-of-collaborative-filtering-100385c6dfe0)
     - matrix factorization: state of art, using this approach won't need the data filtering preprocessing any more, the idea behind matrix factorization is to use latent factors to represent user preferences or movie topics in a much lower dimension space. With matrix factorization, less-known movies can have rich latent representations as much as popular movies have, which improves recommender’s ability to recommend less-known movies. recommended library, [pyspark ALS](https://spark.apache.org/docs/2.2.0/ml-collaborative-filtering.html)

[Tranlation/Summarization system using Transformer](https://github.com/fastai/course-nlp/blob/master/8-translation-transformer.ipynb)
We can possibly build a summarization system using IA's diagnosis --> impression data and the transfomer architecture.

[Vehicle Detection and Tracking in Videos](http://www.gti.ssr.upm.es/data/Vehicle_database.html)
Using SVM, HoG features and OpenCV to identify and track vehicles from a video stream.


TODO: make one of the projects deployed to cloud, and use mongoDB or another SQLDB to store requests/ model returns, also add comprehensive logging modules to the application, and integrate the logging files to Elastic Search, and make a dashboard to display key metrics for the application. 
