# Movie_Recommendation_System
    A movie recommention system using information retrieval techniques.

Installation
------------
This project requires Python and the following Python libraries installed:

* pandas
* numpy
* sklearn

You will also need to have software installed to run and execute a Jupyter Notebook

If you do not have Python installed yet, it is highly recommended that you install the Anaconda distribution of Python, which already has the above packages and more included.



Overview
--------
This project contains i) Statistical Filtering , ii) Content based filtering to recommend top movies and iii) Model Fitting.

Setup steps
-----------
- Download Numpy & Pandas
```
$ sudo apt-get install python-pip
$ sudo pip install numpy
$ sudo pip install pandas
```

- Download Scikit-Learn <br/>
```
$ pip3 install -U scikit-learn`
```

Run steps
---------
- To run statistical filtering,
  - From /code/Statistical filtering/ <br/>
  `python3 topMovies.py`

- To run content based filtering,
  - From /code/Content based filtering/ <br/>
  `python3 topSimilarContentMovies.py`

Results
-------

For our statistical filtering, we got the top 10 movies in TMDB dataset as,

```
The list of top 10 movies are:
                original_title  score
1881  The Shawshank Redemption    8.5
3337             The Godfather    8.4
2294                  千と千尋の神隠し    8.3
3865                  Whiplash    8.3
2731    The Godfather: Part II    8.3
3232              Pulp Fiction    8.3
1818          Schindler's List    8.3
662                 Fight Club    8.3
2170                    Psycho    8.2
1847                GoodFellas    8.2
```

For our content based filtering, finding similarity between movie's overview, we got the top 10 movies similar to 'The Shawshank Redemption' as,
```
Movies similar to The Shawshank Redemption are:
4531               Civil Brand
3785                    Prison
609                Escape Plan
2868                  Fortress
4727              Penitentiary
1779    The 40 Year Old Virgin
2667          Fatal Attraction
3871         A Christmas Story
434           The Longest Yard
42                 Toy Story 3
Name: title, dtype: object
```
For our model fitting, we got the classification report and the accuracy score for the Random Forest and the Naive Bayes models as,
```
Classification Report Of Random Forest:
               precision    recall  f1-score   support

           0       0.95      0.98      0.97      1139
           1       0.05      0.02      0.02        62

    accuracy                           0.93      1201
   macro avg       0.50      0.50      0.49      1201
weighted avg       0.90      0.93      0.92      1201


 Model Accuracy for Random Forest: 
 	 93.255620316403

 Training Accuracy: 
 	 93.75347029428096

 Testing Accuracy: 
 	 93.255620316403

 Classification Report Of Naive Bayes:
               precision    recall  f1-score   support

           0       0.95      1.00      0.97      1363
           1       0.00      0.00      0.00        78

    accuracy                           0.95      1441
   macro avg       0.47      0.50      0.49      1441
weighted avg       0.89      0.95      0.92      1441


 Model Accuracy for Naive Bayes:
 	 94.58709229701596

 Training Accuracy:
 	 93.48602022605593

 Testing Accuracy:
 	 94.58709229701596
```

References
----------
Our methods are based on [Hands-On Recommendation Systems with Python](https://www.oreilly.com/library/view/hands-on-recommendation-systems/9781788993753/) by [Rounak Banik](https://github.com/rounakbanik)
