# Analyzing the Correlation Between Anime Genres and Viewer Ratings

## Overview
This project explores how anime genres relate to viewer ratings and popularity. It combines **exploratory data analysis**, **statistical testing**, **feature engineering**, and **machine learning** to:
- Reveal patterns in ratings across genres.
- Measure the strength of genre effects on ratings.
- Build predictive models for anime ratings.

## Motivation
Understanding which genres resonate most can help:
- **Studios & Producers** tailor content to audience preferences.
- **Streaming Platforms** optimize recommendations.
- **Marketers** target key fan demographics.

## Project Objectives
1. **Statistical Analysis**: Test whether average ratings differ significantly between genres (ANOVA + Tukey HSD + effect size).
2. **Feature Engineering**: Derive new predictors (e.g., `genre_count`, `log_members`) to improve model performance.
3. **Predictive Modeling**: Compare regression and classification models (Linear, Ridge, Lasso, Random Forest, XGBoost) to predict ratings or classify high/low ratings.
4. **Data Enrichment**: Demonstrate how to append fresh anime data via API to keep the analysis up to date.

## Hypotheses
- **H₀**: Mean ratings are equal across all genres.  
- **H₁**: At least one genre’s mean rating differs.  
- Ratings positively correlate with the number of members (popularity).

## Methodology

### 1. Data Collection
- Source: `data/anime.csv` (anime ID, name, genres, type, episodes, rating, members).  
- Example enrichment: Jikan API scripts to fetch top-n popular anime and their metrics.

### 2. Data Processing & Cleaning
- **Missing values**: Drop or impute rows missing critical fields (`genre`, `rating`, `members`).  
- **Data types**: Ensure genres are strings, convert numeric fields.

### 3. Feature Engineering
- **`genre_count`**: Number of genres per title.  
- **`log_members`**: Log-transform of membership counts to reduce skew.  
- **One-hot / Multi-hot encoding**: Turn comma-separated genres into binary columns.

### 4. Exploratory Data Analysis (EDA)
- **Distributions**: Histograms of raw vs. transformed features (`members`, `log_members`).  
- **Correlation matrix**: Numeric feature correlations.  
- **Genre boxplots**: Rating distributions for top-5 frequent genres.

### 5. Statistical Testing
- **ANOVA**: Compare mean ratings by genre.  
- **Effect size (η²)**: Quantify how much variance genre explains.  
- **Tukey HSD**: Identify which genre pairs differ significantly.

### 6. Machine Learning
- **Regression**: Linear, Ridge, Lasso, Random Forest, XGBoost (compare MSE, MAE, R², CV-R²).  
- **Classification**: Binary classification of high (≥7.0) vs. low ratings (Random Forest, ROC/AUC).  
- **Feature importances**: XGBoost top-10 predictors.

## Key Findings
- **Statistical Test**: ANOVA yielded p < 0.01, η² ≈ 0.03 (small effect), with post-hoc differences between specific genres.  
- **Best Model**: XGBoost achieved **R² ≈ 0.54** and **MAE ≈ 0.51**, outperforming linear and tree-based baselines.  
- **Top Predictors**: `log_members`, `genre_count`, and specific genres (e.g., Drama, Action) drove rating predictions.

## Limitations
- **Subjectivity**: Ratings reflect viewer bias.  
- **Genre overlap**: Many titles span multiple genres.  
- **Feature scope**: Excludes studio, release year, review sentiment.

## Future Work
- Incorporate **production studio** and **release year** data.  
- Perform **sentiment analysis** on user reviews.  
- Extend to **time-series** analysis of rating trends.  
- Automate data enrichment via scheduled API pulls.


