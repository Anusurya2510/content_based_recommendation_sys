# Movie Recommendation System

This project implements a simple movie recommendation system using collaborative filtering based on user ratings. The system recommends movies to a user based on their past ratings and the genres of the movies they liked.

## Installation

```bash
pip install pandas numpy seaborn matplotlib scikit-learn
```
## Dataset

The dataset used in this project consists of two main files:

1. **movies.csv**: Contains movie information including `movieId`, `title`, and `genres`.
2. **ratings.csv**: Contains user ratings for movies, including `userId`, `movieId`, `rating`, and `timestamp`.

## Steps

1. **Data Preprocessing**:
   - Extract the year from the movie title.
   - Clean the movie titles by removing the year and any extra whitespace.
   - Split the genres into a list for each movie.
   - Create a binary matrix indicating the presence of each genre for each movie.

2. **User Input**:
   - The user provides a list of movies they have watched along with their ratings.

3. **Matching User Input with Dataset**:
   - Match the user-provided movie titles with the titles in the dataset to get the corresponding `movieId`.

4. **User Profile Creation**:
   - Create a user profile by calculating the weighted average of the genres based on the user's ratings.

5. **Recommendation Generation**:
   - Generate recommendations by calculating the weighted average of the genres for all movies and sorting them to get the top recommendations.
