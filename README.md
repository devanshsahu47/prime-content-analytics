# Prime Data Explorer: Data-Driven Insights on Amazon Prime Content

## Problem Statement & Business Objective
Companies and streaming platforms often struggle to understand the dynamics of content performance and audience engagement. With an ever-growing library of movies and TV shows, identifying trends, assessing content quality, and optimizing production strategies can be challenging. This project addresses these challenges by leveraging a comprehensive dataset comprising Amazon Prime Titles and Credits to extract actionable insights. Our objectives are to:

-  **Assess Content Quality:** Evaluate ratings and runtime distributions to gauge audience satisfaction.
-  **Identify Trends:** Analyze release years, genre popularity, and production countries to understand market evolution.
-  **Enhance Strategic Decision-Making:** Provide data-driven insights that help optimize content acquisition, production, and marketing strategies.
-  **Improve Audience Engagement:** Uncover patterns that lead to higher engagement and identify potential areas of negative performance.

## Approach & Methodology
The project follows an end-to-end data analysis process:
1. **Data Exploration:**
    We begin by loading and exploring the datasets using commands like df.head(), df.info(), and df.describe(include='all') to assess structure, duplicates, and missing values.
2. **Data Wrangling & Preprocessing:**
   - Cleaning: Duplicate records are removed and missing values are addressed (e.g., filling missing age_certification with 'NR' and imputing missing runtime values using the median).
   - Data Type Conversion: Key fields such as release_year are converted to appropriate data types for accurate analysis.
   - List Processing: String representations of list-like columns (e.g., genres and production_countries) are converted into actual Python lists.
   - Feature Engineering: A new column num_genres is created to capture the number of genres per title.
   - Merging Data: The Titles and Credits datasets are merged using the id column, creating a unified view that links content with its cast and crew details.
3. **Visualization & Analysis:**
   Following the Univariate, Bivariate, and Multivariate (UBM) framework, we develop over 20 visualizations that include:
     - Univariate Analysis: Bar charts, histograms, and word clouds to examine individual variable distributions.
     - Bivariate Analysis: Scatter plots, line charts, and box plots to uncover relationships between variables such as ratings and runtime.
     - Multivariate Analysis: Correlation heatmaps, pair plots, and bubble charts to explore deeper interactions and clusters within the data.
   These visualizations provide insights such as:
     - Trends over release years.
     - Popularity of genres and production regions.
     - Relationships between IMDb and TMDB ratings.
     - Identification of potential areas of underperformance or negative growth.

## Dependencies
This project requires the following Python packages:
- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- wordcloud
- jupyter

Install all dependencies using:
```bash
pip install -r requirements.txt
