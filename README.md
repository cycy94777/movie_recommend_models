#### Movie_Recommend_Model

### Project Requirements: Demystifying Ml
1. Find a problem worth solving, analyzing, or visualizing
2. Use machine learning (ML) with the technologies we’ve learned.
3. You must use Scikit-learn and/or another machine learning library.
4. You must use at least two of the following:
    1) Python Pandas
    2) Python Matplotlib
    3) HTML/CSS/Bootstrap
    4) JavaScript Plotly
    5) JavaScript Leaflet
    6) Tableau
    7) SQL Database
    8) MongoDB Database
    9) Google Cloud SQL
    10) Amazon AWS

### The requirements for this project are broken into 5 categories:
    1) Data and data delivery
    2) Back end (ETL)
    3) Visualizations
    4) Group presentations
    5) Slide deck

### Our Work
## Data Delivery and ETL: 
1) Import dependencies
2) Download the dataset from https://grouplens.org/datasets/movielens. Then, we filter the movie based on their published year which are in or after 2010 and get the rating df according the average rating of each movieId. We also split the title into the movie name and year. 
3) Combine the movie dataframe and rating dataframe together to get a new dataframe which includes movieId, title, genres and rating
![image](https://github.com/cycy94777/movie_recommend_models/blob/f147db10716cc79190a4e9f591858c79cd15f767/Image/new_df.png)


## Exploratory Data Analysis
1) Find out which genres have the most movies and bar graph top 10 genres by count
 ![image](https://github.com/cycy94777/movie_recommend_models/blob/f147db10716cc79190a4e9f591858c79cd15f767/Image/movie_genre.png)


2) Find out which genres have the highest average rating and bar graph top 10 by genres
 ![image](https://github.com/cycy94777/movie_recommend_models/blob/f147db10716cc79190a4e9f591858c79cd15f767/Image/avg_ratings.png)


## Movie Recommender Model
1) Split the new dataset into training and test sets, extract features from genres using CountVectorizer on the training set, compute pairwise cosine similarity between genre vectors on the training set, extract features from genres, and then compute pairwise cosine similarity between genre vectors on the test set. Compute pairwise cosine similarity between genre vectors on the test set
2) Create a function to recommend similar movies based on a given movie from the test set. Get the index of the given movie in the test set. Get the cosine similarity scores for the given movie from the test set. Sort the movies based on similarity scores in descending order. Get the titles, genres, and ratings of top similar movies from the test set. Sort the movies by rating in descending order.
3) Reset the index of test_df.
## Movie Recommender Model Testing
1) Find out how many movies are in the test dataset.
2) Make a function to plot a bar chart showing the ratings of recommended movies. Users can enter a movie number within the rage of 0-4016 and convert it into the corresponding movie name. 
3) Find the actual genres in the DataFrame based on the movie title. Get the recommended movies and their genres. Get the genres of the recommended movies. Compute the accuracy score based on genres.
4) Show results by providing recommended movies similar to the chosen movie with rating info.
## Rating Predictor Model
1) Use vectorizer to transform text into numbered matrix, split the data into training and testing sets, initiate Random Forest Regressor model and fit on data
2) Predict on the test set, evaluate model performance by finding mean squared error and R-squared score
3) Show bar graph of feature importance by genre
 ![image](https://github.com/crystalheihei/Movie-Recommender_model/assets/118711472/a6b9a526-cdab-4df4-8d9b-2ffb09c49483)

## Rating Model Testing
1) Predict the rating by entering genre 