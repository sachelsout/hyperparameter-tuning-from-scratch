# hyperparameter-tuning-from-scratch
This repository has the implementation of hyperparameter tuning techniques (GridSearchCV and RandomSearchCV) on K-Nearest Neighbour (KNN) algorithm, from scratch.
<h1>Dataset used</h1>
A 10,000 sampled dataset is randomly generated, having 2 classes 0 and 1. So, its a randomly generated binary classification dataset.<br>
<h1>Hyperparameter Tuning</h1>

![image](https://user-images.githubusercontent.com/86348193/216337456-718b3bb5-48aa-4dc0-ba6e-240ed10b1e18.png) <br>
Hyperparameter Tuning is the process of selecting the best set of hyperparameters which will result in the best ML model. Consider KNN algorithm which has a hyperparameter called 'k' (k is the number of nearest neighbours to the query data point). <br>For different values of k, we get different scores for train and cv/test dataset and then we select best k value given some selection criteria. Now, this set of hyperparameters can be selected randomly or we can hardcode them.<br>
<h1>Cross Validation</h1>

![image](https://user-images.githubusercontent.com/86348193/216335596-806baa8b-6846-4360-ba4f-73f4afe8ead7.png) <br>
Cross Validation is a technique in which ML models are trained on the subset of the dataset(part of the dataset), which we call training data, and then evaluate the performance of the trained model on the another subset of the same dataset, which we call cross-validated/test dataset.<br>Without cross validation we can't say much about the trained model's performance on the test data. So, cross validation plays a vital role in Machine Learning.<br>
<h2>K-Fold Cross Validation</h2>

![image](https://user-images.githubusercontent.com/86348193/216340946-c1dcc9dd-d52b-4df1-ad19-f957a9c49b97.png) <br>
In this method,the data-set is split into k number of subsets(known as folds). All the subsets/folds of data are trained except 1 which is (k-1) fold/subset which is considered for the evaluation of the trained model. In this method, we iterate k times with a different subset reserved for testing purpose each time.<br>
<h1>Hyperparameter Tuning techniques</h1>

![image](https://user-images.githubusercontent.com/86348193/216359644-cda4dcc4-7b50-4932-8e30-6f4188d5609f.png) <br>

There are different techniques to perform hyperparameter tuning. The techniques implemented in this project are RandomSearchCV and GridSearchCV.<br>
<h3>1. RandomSearchCV</h3>
In Random Search Cross Validation technique, the hyperparameter values are selected randomly from a given range. This technique is computationally more optimized way of selecting hyperparameters compared to GridSearchCV.<br>
<h3>2. GridSearchCV</h3>
In Grid Search Cross Validation technique, all the possible parameters combinations are taken into consideration, which makes it computationally more expensive than Random Search CV. Benefit however is that if you run it on a broad parameter space you will get the "best" parameter settings possible.
