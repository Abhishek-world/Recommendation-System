# Recommendation-System
Recommendation System on Movielens dataset

Abstract: - Today in real world to sustain in the market commercialized websites needs to recommend the most suitable product and services based the user preferences and choices. For this websites like Netflix and Amazon uses the Artificial Intelligence based engines to recommend most suitable products to the users.
Introduction: - A recommender system refers to a system that is capable of predicting the future preference of a set of items for a user, and recommend the top items. One key reason why we need a recommender system in modern society is that people have too much options to use from due to the prevalence of Internet. In the past, people used to shop in a physical store, in which the items available are limited. 
For instance, the number of movies that can be placed in a Blockbuster store depends on the size of that store. By contrast, nowadays, the Internet allows people to access abundant resources online. Netflix, for example, has an enormous collection of movies. Although the amount of available information increased, a new problem arose as people had a hard time selecting the items they actually want to see. This is where the recommender system comes in.
Dataset: - For this project we are going to use famous Movie lens dataset which is taken from the https://grouplens.org,which is one of the most common datasets used when implementing and testing the recommender engines. It contains 100k movie ratings from 943 users and a selection of 1682 movies. It has 24 columns but the last 19 columns are genre which are the zero and 1 values so we can drop these columns we have used only 5 columns for this project.
There is no column title section in the file so we have added the column titles which are ‘user_id’, ‘item_id’, ‘rating’, ‘timestamp’. 

 
As this dataset is already cleaned the records which have less than 20 ratings are removed and there is not much scope of data pre-processing we have used a variation of this data set which is also taken from the movielens datasets. 

This dataset which has 20 columns named 'adult', 'belongs_to_collection', 'budget', 'genres', 'homepage', 'id','imdb_id', 'original_language', 'original_title', 'popularity','revenue', 'runtime', 'spoken_languages', 'status', 'tagline', 'title','video', 'vote_average', 'vote_count'.


 

Data Processing:-
Dataset used in this project is already clean so there is no need for preprocessing, 
hence we took other data set and applied some data preprocessing techniques to it. 
Replacing null values by calculating mean, decimal scaling normalization, Min-max normalization, changing categorical attribute to numerical (binary), binning are 
some of the techniques which we used for data pre processing.
 
 
 
 
 

Proposed Methodology: - 

•	We have divided the project in two sections in the first section we have made the basic Recommendation system by suggesting items that are most similar to a particular item. 
•	It just tells you what movies/items are most similar to your movie choice. 
•	In the later project we made a more robust form of recommendation system which uses the advance python libraries.
Collaborative Filtering
In general, Collaborative filtering (CF) is more commonly used than content-based systems because it usually gives better results and is relatively easy to understand (from an overall implementation perspective). 
The algorithm has the ability to do feature learning on its own, which means that it can start to learn for itself what features to use.
CF can be divided into 
•	Memory-Based Collaborative Filtering 
•	 Model-Based Collaborative filtering.

Memory-Based Collaborative Filtering
Memory-Based Collaborative Filtering approaches can be divided into two main sections: user-item filtering and item-item filtering.
A user-item filtering will take a particular user, find users that are similar to that user based on similarity of ratings, and recommend items that those similar users liked.
In contrast, item-item filtering will take an item, find users who liked that item, and find other items that those users or similar users also liked. It takes items and outputs other items as recommendations.
•	Item-Item Collaborative Filtering: “Users who liked this item also liked …”
•	User-Item Collaborative Filtering: “Users who are similar to you also liked …”
In this Project, we implemented Model-Based CF by using singular value decomposition (SVD) and Memory-Based CF by computing cosine similarity.
Movie title file is separate from the dataset so we need to merge this file with the original dataset.

Libraries and Methods:- 
•	For the purpose of data visualization we used matplotlib ans seaborn libraries.

•	For the purpose of splitting the dataset into training and test set we used sklearn library.


•	We used pairwise_distances method from skleran.metrics library to find the cosine similarity between the user_similarity and item_similarity that will range from 0 to 1 since the ratings are all positive.

•	We used the turicreate library that is the built-in library for Recommender Systems. To feed the model in turicreate library function   turicreate.popularity_recommender.create() we need to convert the train and test inti Sframe.


