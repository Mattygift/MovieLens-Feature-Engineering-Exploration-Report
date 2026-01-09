# MovieLens-Feature-Engineering-Exploration-Project

## Table of Content
- [Project Overview](#project-overview)
- [Dataset Overview](#dataset-overview)
- [Tools](#tools)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
- [Feature Engineering](#feature-engineering)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Key Insights](#key-insights)
- [Conclusion and Future Recommendations](#conclusion-and-future-recommendations)
- [Visualizations Tables](#visualizations-tables)

### Project Overview
This report summarizes the process and findings from the project. The main goal is to learn and apply feature engineering and exploratory data analysis (EDA) on the MovieLens dataset to generate insights that could support a future recommendation system.

### Dataset Overview
The dataset used is a small portion of the MovieLens dataset, containing movie ratings and metadata.
Files used:
* ratings.csv – Contains user IDs, movie IDs, ratings, and timestamps.
* movies.csv – Contains movie titles and genres.
  
After merging, the dataset included: - userId: Unique identifier for each user. - movieId: Unique identifier for each movie. - rating: User rating (0.5–5.0 scale). - timestamp: Time when the rating was given. - title and genres: Movie metadata.

### Tools
* Excel to clean 
* Python libraries like Panda,Matplotlib and Seaborn to visualize and  sumarize 

### Data Cleaning and Preparation
In the initial Data preparation phase we preformed the following tasks:
1. Data loading and inspection.
2. Handling missing values.
3. Data cleaning and formatting.

### Feature Engineering
We created six (6) new features to enrich the dataset and make it more suitable for analysis.

|Feature Name|Description|Why It’s Useful|
|-------------|-----------|---------------|
|release_year|Extracted from movie title (e.g., Toy Story (1995) → 1995)|Allows trend analysis over time.|
|num_genre|Count of genres per movie|Helps see if diverse-genre movies perform differently.|
|avg_movie_rating|Average rating of each movie|Useful for ranking movies and recommendations.|
|avg_user_rating|Average rating given by each user|Helps identify generous or critical users.|
|rating_year|Extracted from rating timestamp|Enables time-based analysis of rating trends.|
|is_classic|1 if movie released before 2000, else 0|Helps compare older vs newer movies.|


### Exploratory Data Analysis
We performed exploratory analysis using Python libraries (pandas, matplotlib, seaborn) to visualize and summarize key patterns.
* Distribution of Ratings
  - Most ratings are between 3.0 and 4.0, indicating generally positive reviews.
* User Rating Behavior
  - Users tend to give moderate ratings — very high or very low scores are less common.
* Average Rating by Release Year
  - Classic movies (1990s and earlier) maintain strong ratings.
  - Ratings fluctuate slightly across decades but remain stable overall.
* Genres and Ratings
  - Movies with fewer genres (1–2) often receive slightly higher ratings.
  - Popular genres include Drama, Comedy, and Action.
* Classic vs Modern Movies
  - Classic movies (before 2000) show marginally higher ratings than modern ones.

### Key Insights
- Positive bias in ratings – Users generally rate movies above 3.0.
- Genre diversity – Multi-genre movies exist but may dilute strong audience focus.
- Classic movies – Maintain enduring appeal among viewers.
- User tendencies – Some users consistently rate higher or lower, suggesting personal bias.
- Genre popularity – Drama and Comedy dominate the dataset.
- Rating stability – Ratings have remained steady across years.

### Conclusion and Future Recommendations
This analysis demonstrates how feature engineering and EDA can uncover meaningful insights from raw data. 
These insights can help inform a movie recommendation system in several ways:
  - Use avg_movie_rating and avg_user_rating for baseline predictions.
  - Combine genre and year-based trends to personalize recommendations.
  - Identify user preferences based on genre or time period.

### Visualizations Tables


