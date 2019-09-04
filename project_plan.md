### Projects

[Text Classficiation with Naive Bayes](https://github.com/cs109/2015lab10)
In the mini-project, you'll learn the basics of text analysis using a subset of movie reviews from the rotten tomatoes database. You'll also use a fundamental technique in Bayesian inference, called Naive Bayes. 

[Amazon Product Recommendation System](http://jmcauley.ucsd.edu/data/amazon/)
The Amazon product review datasets contains product reviews and metadata from Amazon, including 142.8 million reviews. We can build a recommendation system using possible tools like [SparkML ALS](https://spark.apache.org/docs/2.2.0/ml-collaborative-filtering.html)

```bash
for line in open('Movies_and_TV_5.json','r'): 
     data.append(json.loads(line)) 
```

[Tranlation/Summarization system using Transformer](https://github.com/fastai/course-nlp/blob/master/8-translation-transformer.ipynb)
We can possibly build a summarization system using IA's diagnosis --> impression data and the transfomer architecture.

[Vehicle Detection and Tracking in Videos](http://www.gti.ssr.upm.es/data/Vehicle_database.html)
Using SVM, HoG features and OpenCV to identify and track vehicles from a video stream.


TODO: make one of the projects deployed to cloud, and use mongoDB or another SQLDB to store requests/ model returns, also add comprehensive logging modules to the application, and integrate the logging files to Elastic Search, and make a dashboard to display key metrics for the application. 
