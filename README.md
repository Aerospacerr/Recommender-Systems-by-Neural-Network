# Collaborative Movie Recommendation System with Neural Network

<p align="center">
	<img src=" https://miro.medium.com/max/1000/1*x8gTiprhLs7zflmEn1UjAQ.png " /> 

</p>

## Table of contents
* [General info](#general-info)
* [Project info](#project-info)
* [Dataset info](#dataset-info)
* [Technologies](#technologies)
* [Setup](#setup)
* [Further Development Ideas](#further-development-ideas)
* [References](references)

## General info
* Creating an embedding layer having embedding vectors of user and movie ids.
* Creating a reasonable scoring function that can capture interactions between users and items.
* Compute loss between scores and ground truth using mean square error and minimize it.
* Check decrease on loss by adding a feed-forward neural network stacked to embedding layer and tune the model.
* Report performance metrics over hyper-parameters.
* Create a script to recommend any given user to 5 most relevant items

## Project info
* Project include 4 parts with dataset preparation.
* We tried to build embedding layers for users and movies.
* Dataset downloaded automatically, created as pandas dataframe, preprocessed to be used. 
* Firstly, simply dot production of users and movies have been used to calculate interaction between them.
* Secondly, we created a neural network with Tensorflow.
* We added activation function as relu and sigmoid. Concat user and movie items.
* Added dense and dropout layers.
* Lastly, we normalize out target values and run neural network again for normalized target values. We get the biggest impact with normalization.
* Tried fine tune hyper-parameters trial by error. (For example: Embedded size taken as 50 from Jeremy Howard's fast.ai lessons)

## Dataset info
Name: MovieLens 1M Dataset 
Link: http://files.grouplens.org/datasets/movielens/ml-1m.zip  
You can download it from the link, it is bigger than 25MB, therefore couldn't upload here.

--RATINGS--

All ratings are contained in the file "ratings.dat" and are in the
following format:
UserID::MovieID::Rating::Timestamp

- UserIDs range between 1 and 6040 
- MovieIDs range between 1 and 3952
- Ratings are made on a 5-star scale (whole-star ratings only)
- Timestamp is represented in seconds since the epoch as returned by time(2)
- Each user has at least 20 ratings

--MOVIES--

Movie information is in the file "movies.dat" and is in the following
format:

MovieID::Title::Genres

- Titles are identical to titles provided by the IMDB (including
year of release)
- Genres are pipe-separated and are selected 


## Technologies
Project is created with:
* Google Colab
* Tensorflow
* Keras
* Pandas
* Numpy 

Imports are done in the necessary cells.

## Setup
To run this project, you need data prepation steps after downloading the data. Or you could just get the last part for neural network which is called as "NNmodel". 

## Further Development Ideas
* We nicely get predictions with our model.
* Tried fine tuning for hyper-parameters and best possible solution is normalization of target. Maybe accuracy can be more successfull with tuning.
* We can create new embedding layers for timestamps, movie genres etc. 
* We could tune the size of the movie and user embeddings independently.
* With more dense layers we can add more learning capability to model.

## References
* Deep Learning based Recommender System: A Survey and New Perspectives, Shuai ZHANG, 2017
* Item-based collaborative filtering recommendation algorithms, Badrul SARWAR, 2001
* Neural Collaborative Filtering, Xiangnan HE, 2017
* Jeremy Howard's Fast.Ai lessons
* https://www.tensorflow.org/
* https://keras.io/
* https://developer.nvidia.com/

