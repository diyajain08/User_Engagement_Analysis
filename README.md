# Restaurant Success Analysis Using Yelp Dataset

This project explores the factors contributing to the success of restaurants, specifically analyzing their user engagement metrics such as review counts and average ratings. The analysis is based on the **Yelp Dataset** available on Kaggle, which contains information about businesses, reviews, and users across multiple locations in the USA and Canada.

Dataset: [Yelp Dataset on Kaggle](https://www.kaggle.com/datasets/yelp-dataset/yelp-dataset)

## Project Overview

The project is divided into several stages, including data extraction, cleaning, analysis, and visualization. The goal is to understand how factors like review count, star rating, and user engagement vary across cities and states and how they contribute to the overall success of restaurants.
<br>

### Dataset Information

The Yelp dataset contains multiple JSON files, but we have primarily used the following:
- **business.json**: Contains information about businesses, including their `business_id`, name, location, review count, and average star rating.
- **review.json**: Contains reviews made by users on different businesses, including text, star rating, and helpfulness metrics.
- **user.json**: Information about Yelp users, including their reviews, number of friends, and elite status.
- **tip.json**: Tips left by users about businesses, similar to short reviews.
- **checkin.json**: Information about check-ins at businesses, providing insight into user engagement trends.
<br>
<br>

### Key Objectives

1. **Correlation Analysis**: Investigating the relationship between user engagement (reviews, tips, check-ins) and business success (measured by review count and average star rating).
2. **Geographical Insights**: Analyzing how the success metrics of restaurants vary across different states and cities.
3. **Time Trends**: Observing engagement trends over time and the impact of factors like seasonality and external events (e.g., COVID-19).
4. **Sentiment Analysis**: Exploring the impact of review sentiment on ratings and review counts.
<br>

## Analysis Overview

### Data Cleaning and Preprocessing

- **Database Creation (Notebook: Database Creation.ipynb)**:
    - Extracted data from the Yelp JSON files.
    - Created SQL databases for efficient querying and data analysis.
    - Cleaned the dataset, handling missing values and outliers.

### Exploratory Data Analysis (EDA)

The EDA phase aimed to uncover trends and patterns related to restaurant success using key metrics such as `review_count` and `stars`. The following analyses were performed:

1. **Descriptive Statistics**: Summarized key variables like `review_count` and `stars` to understand the distribution and central tendencies.
   
3. **Distribution & Correlation**: Explored the distribution of review counts and star ratings, identifying a moderate positive correlation between the two, though higher review counts didn't always guarantee better ratings.
   
4. **Geographical Insights**: Analyzed the performance of restaurants by **state** and **city**, highlighting top-performing cities such as Philadelphia and Tampa based on user engagement and ratings.

5. **Outlier Detection**: Identified businesses with unusually high or low review counts and ratings, further exploring characteristics of outliers.

6. **Time Trends**: Investigated changes in engagement over time, noting significant drops during the COVID-19 pandemic and gradual recovery.

7. **Visualization**: Created visualizations, including **scatter plots**, **histograms**, and a **Folium map**, to illustrate the relationships and geographic variations in restaurant success.

### Key Findings

1. **Geographical Trends**:
    - Cities such as Philadelphia, Tampa, and Indianapolis emerged with the highest success scores, reflecting both high user engagement and positive ratings.
  
2. **Rating and Engagement**:
    - Higher ratings generally correlate with more reviews, tips, and check-ins, though a decline in engagement is observed in restaurants with perfect 5-star ratings.
  
3. **User Engagement Patterns**:
    - There is a strong correlation between review count, check-ins, and tips. Higher engagement in one area often corresponds to higher engagement in others.
  
4. **Impact of Elite Users**:
    - Elite users, while fewer in number, contribute significantly more to review counts. They tend to engage more deeply with businesses, making them key drivers of restaurant visibility.

### Visualizations

1. **Histograms**: Used to display the distribution of `review_count` and `stars`, helping to identify skewness, common rating ranges, and outliers in the dataset.
  
2. **Scatter Plots**: Plotted `review_count` against `stars` to visually analyze the correlation between user ratings and engagement. These plots highlighted that while higher ratings are generally associated with more reviews, the relationship is not always linear.

3. **Heatmaps**: Generated correlation heatmaps to understand the relationships between various metrics, such as review counts, check-ins, and tips, revealing strong links between different forms of user engagement.

4. **Bar Charts**: Used to compare average star ratings and total review counts across different cities and states, making it easier to identify top-performing locations.

5. **Time Series Plots**: Visualized changes in user engagement metrics (e.g., review counts, check-ins) over time, especially focusing on dips during the COVID-19 pandemic and subsequent recovery trends.

6. **Folium Map**: Created an interactive map that visualizes restaurant success across different cities and states. The markers are color-coded based on success scores, allowing for an intuitive comparison of geographic performance.

### Recommendations

1. **Increase Engagement**:
    - Businesses should focus on boosting user engagement across multiple metrics, as increases in one type (reviews, tips, or check-ins) tend to drive increases in others.
  
2. **Leverage Elite Users**:
    - Restaurants should foster relationships with Yelp elite users to increase their visibility and drive more reviews and engagement.
  
3. **Optimize for Peak Hours**:
    - Knowing the peak engagement times (typically 4 PM - 1 AM) can help businesses better manage resources and improve service during busy periods.
<br>
<br>
   
## Files in This Repository

- **Database Creation.ipynb**: This notebook covers the process of data extraction, database creation, and data cleaning. It transforms the JSON files into SQL tables for easier querying.
  
- **Analysis.ipynb**: This notebook contains the exploratory data analysis, success metric calculation, and geographical visualizations using libraries such as Pandas, NumPy, and Folium.

- **yelp1.pdf**: A detailed report of the findings from the analysis, summarizing the key insights and recommendations based on the data.
<br>

## Technologies Used

- **Python**: For data manipulation, analysis, and visualization.
- **Pandas and NumPy**: Used for data wrangling and numerical calculations.
- **SQL**: For querying the Yelp dataset after converting the JSON files into SQL tables.
- **Folium**: For interactive map visualization to explore geographical trends.
- **Matplotlib/Seaborn**: For data visualization and plotting trends.
<br>

## Conclusion

This project provides an in-depth analysis of the success factors for restaurants using the Yelp dataset. The interactive map and success score metric offer a unique way to visualize and understand restaurant performance across various cities and states.

