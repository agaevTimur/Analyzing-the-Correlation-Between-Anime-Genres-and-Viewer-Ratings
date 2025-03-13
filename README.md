# Analyzing the Correlation Between Anime Genres and Viewer Ratings

## Overview
This project aims to explore and analyze the relationship between anime genres and their corresponding viewer ratings. By investigating this relationship, the study seeks to identify whether certain genres consistently achieve higher ratings or attract more viewers.

## Motivation
Understanding viewer preferences can significantly impact content creators, streaming services, and anime studios. This analysis provides valuable insights into trends in anime popularity, potentially guiding decisions related to anime production, licensing, and recommendations to viewers.

## Project Objectives
- Identify patterns in viewer ratings across various anime genres.
- Analyze if specific genres consistently outperform others in terms of ratings and popularity.
- Provide insights that could aid content recommendation systems or anime marketing strategies.

## Hypotheses
- **First Hypothesis:** Certain anime genres consistently have higher viewer ratings.
- **Second Hypothesis:** Viewer ratings positively correlate with the popularity (number of members) of anime titles.

## Methodology

### Data Collection
The dataset includes:
- Anime ID
- Name of the anime
- Genre(s)
- Type (TV, Movie, OVA, etc.)
- Number of episodes
- Viewer rating
- Number of members (popularity metric)

### Data Processing
- Data cleaning to handle missing or inconsistent values.
- Categorization and encoding of genres for effective analysis.
- Merging genre information with ratings and popularity metrics.

### Data Analysis
- **Exploratory Data Analysis (EDA):** Visualization of ratings distributions across genres.
- **Statistical Analysis:**
  - Correlation analysis between genres, ratings, and popularity metrics.
  - Hypothesis testing (e.g., ANOVA, Chi-square tests).
- **Machine Learning Techniques:** Classification or regression models (Random Forest, Linear Regression, Decision Tree) to predict anime ratings based on genre and popularity metrics.

## Findings
(This section will be updated upon completion of data analysis.)

## Limitations
- Ratings might be subjective and influenced by viewer bias.
- Genre definitions can overlap, complicating analysis.

## Future Work
- Extend the analysis to include additional variables such as production studio, year of release, and episode length.
- Explore temporal trends to understand changes in viewer preferences over time.
- Utilize user reviews for sentiment analysis to enhance rating predictions.

## Repository Structure
- `data/`: Dataset used for analysis.
- Python scripts (`.ipynb`): Include data preprocessing, exploratory analysis, and machine learning models.
- `requirements.txt`: Project dependencies.
- `README.md`: Instructions for reproducing the analysis.
