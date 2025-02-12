# Movie Recommendation System with Collaborative Filtering
## Project Objective
 In this project, we will build a collaborative filtering recommender system using surprise library.
 Some of the key highlights of this project are:
 1. Use surprise's built-in reader class to process data to work with recommender algorithms
 2. Obtain a prediction for a specific user for a particular item
 3. Introduce a new user with rating to a rating matrix and make recommendations for them
 4. Create a function that will return the top 5 movie recommendations for a user, based on
 their ratings of other movies
 We will be making a movie recommendations based on the MovieLens
 https://grouplens.org/datasets/movielens/latest/
 (https://grouplens.org/datasets/movielens/latest/) dataset from the GroupLens research lab at
 the University of Minnesota.
 The MovieLens dataset contains the following files links.csv, movies.csv, ratings.csv and
 tags.csv. For this project, we will only focus on the movies.csv and ratings.csv to make our
 recommendations.

## Determine the Best Model
### Check item-item similarity versus user-user similarity
For the sake of computation time, it's best to calculate the similarity between whichever number
 is fewer, users or items. 

### Memory Based/Neighbourhood Models
We start with the memory based/neighbourhood models and use RMSE to test the model
 predictions. The lower the values of RMSE the better the model
 1. Approach 1: Check which is the better similarity matrix i.e cosine or pearson
 2. Approach 2: Apply the better performing similarity matrix to KNNBasic, KNNBaseline,
 KNNWithMeans
 The one with lowest RMSE will be the best performing model under memmory
 based/neighbourhood models

### Model Based Method
The next approach to determine the best model is to try out the Model based method with
 SVD(Singular Value Decomposition)
