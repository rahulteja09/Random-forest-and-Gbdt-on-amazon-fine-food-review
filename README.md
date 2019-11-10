# Random-forest-and-Gbdt-on-amazon-fine-food-review
Given a review, Using Random forest and Gbdt  models determine whether the review is positive (rating of 4 or 5) or negative (rating of 1 or 2). 
[Q] How to determine if a review is positive or negative? 
[Ans] We could use Score/Rating. A rating of 4 or 5 can be cosnidered as a positive review. A rating of 1 or 2 can be considered as negative one. A review of rating 3 is considered nuetral and such reviews are ignored from our analysis. This is an approximate and proxy way of determining the polarity (positivity/negativity) of a review.


Models used: Sklearn Random forest classifier and XGboost XGBClassifier ,Vectorizers used : Bow (sklearn-CountVectorizer),Tfidf(sklearn-TfidfVectorizer),Avg-W2v(trained a gensim model),Tfidf-W2v Metrics used: auc(sklearn's roc_auc) and Accurcy

Results obtained:

+------------+---------------+-----------+------------+----------+------+
| Vectorizer |     Model     | Max Depth | Estimators | Accuracy | AUC  |
+------------+---------------+-----------+------------+----------+------+
|    Bow     | Random Forest |     29    |    112     |  86.13   | 0.91 |
|   Tfidf    | Random Forest |     38    |    103     |  87.47   | 0.92 |
|  Avg-W2v   | Random Forest |     12    |     98     |  88.659  | 0.93 |
| Tfidf-W2v  | Random Forest |     12    |    126     | 87.2621  | 0.9  |
|    Bow     |    XGBoost    |     14    |     67     |  89.529  | 0.93 |
|   Tfidf    |    XGBoost    |     10    |     13     |  87.053  | 0.88 |
|  Avg-W2v   |    XGBoost    |     9     |     24     |  89.54   | 0.93 |
| Tfidf-W2v  |    XGBoost    |     9     |    100     |  88.788  | 0.92 |
