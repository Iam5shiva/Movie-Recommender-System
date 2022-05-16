# Movie-Recommeder-System
This project aims to build a movie recommendation system which recommends new movies to users based on the user input using content based recommendation.

![image](https://user-images.githubusercontent.com/41468555/168633251-798b0442-22f4-49ef-a340-2cdf06d70b12.png)


## Dataset
The dataset used in this project was obtained from the tmdb site. There are 2 files-
* tmdb_5000_movies.csv - This contains all information related to movies like - title, budget, status, revenue, release date, genre etc
* tmdb_5000_credits.csv - This contains data about cast and crew of a movie
  
  These 2 datasets are merged based on title

## Approach
Created tags for each movies based on different features which helps us find out content similarity. Before creating tags, data is preprocessed
i.e removal of missing values, columns formatting, converting string of list into list. After that,
created a new feature 'tags' by merging data of columns - overview, genres, keywords, cast,crew. For finding similarity between movies, we
need to find similarity between their tag column values using text vectorization technique - Bag of words and applied stemming to get the root word. For calculating distance
between each movie (vector) used cosine distance and then sorted these distance in descending order to recommend movies.
Deployed the project as a web application using streamlit and heroku.

Link to application - [https://your-movies-recommender.herokuapp.com/](https://your-movies-recommender.herokuapp.com/)

