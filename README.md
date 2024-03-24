![image](https://github.com/Trixiemoek/Phase-4-Recommendation-Systems-Project/assets/145706145/e3520e1c-6b38-428c-964f-beca7f09ed56)

# Movie Recommendation System 

Welcome to the Movie Recommendation System repository! This project aims to provide a comprehensive guide and implementation of a movie recommendation system using collaborative filtering techniques. Collaborative filtering is a popular approach to recommend items (in this case, movies) by leveraging user interactions and similarities.

The repository consists of the following components:

1.	**MovieLens Dataset:** The MovieLens dataset, which contains user ratings for movies, is hosted at this location. Please download the dataset and place it in the data/ directory of this repository.

2.	**Jupyter notebook:** The core functionality of the recommendation system is implemented in jupyter notebook available here. These scripts handle data preprocessing, model training, hyperparameter tuning, and recommendation generation.


3.	**README.md:** The main README file provides an overview of the repository and instructions for running the code. It also includes information about the project structure, usage guide, references and contributors.


## Introduction
Recommendation systems have become popular in today's digital world, aiding users in discovering new items based on their preferences and past interactions. Collaborative filtering is a prominent technique employed in recommendation systems, where recommendations are made based on the preferences of similar users or items.
   

 ## Objectives

The objectives of this project are:
•	Developing a user-based recommender system for a movie streaming platform or an online movie rental service.
•	Providing personalized movie recommendations to users based on their viewing history and preferences, as well as the preferences of similar users.
•	Enhancing the user experience by suggesting relevant and engaging movies tailored to each user's tastes.
•	Increasing user satisfaction, retention, and potentially higher revenue through improved engagement and movie consumption.
 

 # Business and Data Understanding
    
# Business Problem:
Developing a user-based recommender system for a movie streaming platform or an online movie rental service. The goal is to provide personalized movie recommendation system to users based on their viewing history, ratings, as well as the preferences of similar users.

## Implementation Overview;

## Data Preparation: 
We used the MovieLens dataset, which contains ratings.csv, movies.csv, links.csv, and tags.csv, each providing different aspects of movie-related data.
The columns are described as follows:
•	**User ID:** A unique identifier for each user who rated the movies.
•	**Movie ID:** A unique identifier for each movie being rated.
•	**Rating:** The numerical rating given by the user for the movie on a scale of 1 to 5
•	**Timestamp:** The timestamp indicating when the rating was provided.
•	**Title:** The title of the movie.
•	**Genres:** The genre(s) or category associated with the movie.
•	**IMDb ID:** The identifier of the movie on the IMDb (Internet Movie Database) website.
•	**Tag:** The actual tag or keyword assigned by the user.

The dataset was explored, cleaned and preprocessed to ensure compatibility with the recommendation system.
     
 

# Modelling

## Collaborative Filtering
Collaborative filtering operates on the assumption that users who have agreed in the past tend to agree again in the future. In the modeling phase, we implemented both memory-based and model-based collaborative filtering techniques:

1.	**Memory-Based Collaborative Filtering:** This approach computes similarities between users or items based on their interactions. Recommendations are then made by identifying items that are similar to those preferred by the user. We  explored;

•	**User-Based Collaborative Filtering:** This method suggests movies by comparing users' past interactions. It calculates similarity between users using metrics like cosine similarity or Pearson correlation coefficient, then predicts unseen movies by combining ratings from similar users.

•	**Item-Based Collaborative Filtering:** This technique recommends movies similar to those a user has engaged with previously. It assesses item similarity based on user ratings, typically using cosine similarity or Pearson correlation coefficient. Recommendations are made by identifying movies akin to those highly rated or liked by the user.

We used the following steps for memory based collaborative system:

- User Similarity Calculation:  This involves calculating the pairwise similarity between users/item based on their rating patterns. Similarity measures to be calculated include; Pearson correlation coefficient.

- Neighborhood Formation: This entails identifying, for each user/item, a set of similar users (neighbors) based on the calculated similarities. The neighborhood size will be determined by setting a threshold or selecting the top-k most similar users/items.

- Prediction and Recommendation: This involves predicting, for a given user/item, the rating for an unseen movie by aggregating the ratings of that movie from the user's/item’s neighbors. Aggregation techniques adopted include; weighted average, mean. Out of this, recommendation will be done for the movies with the highest predicted ratings to the user.


 
**Model-Based Collaborative Filtering:** This approach learns latent factors representing users and items from observed interactions. We explored;  

•	**Singular Value Decomposition (SVD):** We explored the Surprise library to implement SVD, a matrix factorization technique that decomposes the user and item matrix by extracting latent factors.

•	**Non-Negative Matrix Factorization (NMF):** Decomposes the user-item matrix into non-negative factors.

   
Evaluation of the performance of the model based collaborative filtering was done by using RMSE and its effectiveness could was influenced by hyper parameter tuning (grid search). The ratings was sorted in a descending order and recommendations is given to the user.


 **Deep learning with neural Networks:** Techniques such as embedding layers has been used to learn low-dimensional representations of users and items (movies).Recommendations are made based on predictions from the neural network model.
   

# Recommendations and conclusions     

## Recommendations:

1.	Continuous Monitoring and Optimization: it's crucial to continuously monitor thei performance and optimize them accordingly. Implement monitoring tools and metrics to track the effectiveness of recommendations over time. Regularly update algorithms and parameters to adapt to changing user preferences and behaviors.

2.	User Engagement Strategies: To further enhance user engagement and satisfaction, consider implementing additional features and strategies beyond movie recommendations. Explore opportunities for interactive content, personalized notifications, and community engagement features to keep users actively involved and invested in the platform.


3.	Content Diversification: Although the recommendation systems excel at providing personalized movie suggestions, consider expanding the content library to offer a diverse range of movies and genres. Cater to a broader audience by including niche and independent films, international cinema, and exclusive content not available elsewhere. This diversification can attract new users and cater to varying tastes and preferences.

4.	Experiment with Novel Approaches: As technology evolves, explore emerging trends and innovations in recommendation systems. Experiment with novel approaches such as reinforcement learning, contextual recommendations based on user context (time of day, device type, etc.), and interactive recommendation interfaces. These innovations can provide unique user experiences and differentiate your platform in the competitive market.


5.	User Feedback and Iteration: Leverage user feedback as a valuable source of insight for further refinement and iteration. Implement feedback mechanisms such as ratings, reviews, and surveys to gather user opinions and preferences. Use this feedback to fine-tune recommendation algorithms, improve content curation, and address user pain points effectively.

 
## Conclusions:

Through the development of both memory-based and model-based collaborative filtering recommendation systems, significant progress has been made towards addressing the business problem of providing personalized movie recommendations to users. 

These systems leverage user viewing history, ratings, and preferences, as well as the behaviors of similar users, to deliver tailored movie suggestions that enhance the overall user experience.

The implementation of these recommendation systems has the potential to drive various business objectives, including increased user satisfaction, retention, and engagement. By providing relevant and engaging movie recommendations tailored to each user's tastes, the platform can foster deeper user engagement and potentially increase revenue through improved movie consumption.

Moving forward, continued investment in research and development, as well as leveraging advanced recommendation techniques and continuously refining the recommendation algorithms, the platform can create a more personalized and immersive movie-watching experience for its users, driving business growth and success in the process.

## Usage Guide

Follow these steps to set up and use the Movie Recommendation System:

1.	Clone the Repository: Start by cloning this repository to your local machine.
bashCopy code git clone https://github.com/Trixiemoek/Phase-4-Recommendation-           Systems.git cd Phase-4-Recommendation-Systems 

2.	Download the Dataset: Download the MovieLens dataset from this link and place it in the data/ directory of the repository.

3.	Run the notebook codes and explore the recommendations References

•	Surprise documentation: Official documentation for the Surprise library.
•	MovieLens dataset: Dataset used for training and evaluation.

**Contributors**
•	Trixie
•	Peter
•	Mercy 
•	Ahmed

