# Intermediate_Kanishk_movie_lens-recommendation-system
Movie Lens Recommendation System for Cinema goers


# Movie Recommendation System

This project implements a Movie Recommendation System using two popular techniques: **Content-Based Filtering** and **Collaborative Filtering**.

## Dataset
The system utilizes the MovieLens 20M Dataset by GroupLens, a widely used dataset for building recommendation systems, containing 20 million ratings and 465,000 tag applications to 27,000 movies by 138,000 users.

## Key Features

### 1. Data Preparation
- Movie Data Cleaning: Extraction of release years from movie titles and removal of year information from the title string.
- Genre Processing: Handling of movie genres, including filling missing values and **One-Hot Encoding** genres to facilitate content-based recommendations.
- Rating Data Cleaning: Removal of unnecessary columns like `timestamp` from the ratings data.

### 2. Content-Based Filtering
This approach recommends movies based on the similarity of their attributes (content) to movies the user has liked in the past.
- User Profile Generation: Creates a 'user profile' by calculating weighted averages of genres from movies the user has rated, where ratings serve as weights.
- Movie Similarity: Recommends movies by comparing their genre vectors to the generated user profile, identifying movies with the highest similarity scores.

### 3. Collaborative Filtering (User-User Filtering)
This technique recommends movies by finding users with similar tastes to the input user and suggesting movies that those similar users enjoyed.
- Finding Similar Users: Identifies a subset of users who have rated movies in common with the input user.
- Pearson Correlation: Calculates the **Pearson Correlation Coefficient** between the input user and other users to quantify taste similarity.
- Weighted Average Recommendation: Generates recommendations by taking a weighted average of ratings from the most similar users, using the Pearson Correlation as weights.

## Technologies Used
-   Python
-   Pandas: For data manipulation and analysis.
-   NumPy: For numerical operations.
-   Matplotlib: For data visualization.
-   Seaborn: For enhanced data visualization.

## Getting Started

To run this notebook and explore the recommendation system:

1.  Clone the repository (if applicable) or download the notebook file.
2.  Ensure you have a Python environment with the necessary libraries installed (pandas, numpy, matplotlib, seaborn).
3.  Execute the cells sequentially in a Jupyter Notebook or Google Colab environment.
    *   The notebook will automatically download and extract the MovieLens 20M dataset.
    *   Follow the comments and explanations in each cell to understand the data processing and recommendation logic.

## Results
Upon execution, the notebook will output:
-   Top 10 most frequent movie genres.
-   A correlation heatmap showing relationships between different movie genres.
-   Top 20 content-based movie recommendations for a dummy user.
-   Top 10 collaborative filtering movie recommendations for a dummy user.

## Acknowledgements
-   GroupLens Research for providing the MovieLens 20M dataset.
