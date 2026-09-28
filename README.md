# Social Media Engagement Analytics Using Python

## Project Overview

* This project analyzes social media engagement data using Python.
* The dataset contains 5,000 social media records and 19 columns.
* The analysis focuses on data cleaning, exploratory data analysis, data wrangling, statistical analysis, and visualization.
* The goal is to understand engagement patterns and identify useful insights from social media data.

## Dataset

* Dataset Name: `social_media_engagement_5000.csv`
* Number of Records: 5,000
* Number of Columns: 19

### Main Columns

* `user_id` - Unique user identifier
* `age` - User age
* `gender` - User gender
* `country` - User country
* `post_id` - Unique post identifier
* `post_type` - Type of post such as image, reel, text, or video
* `post_category` - Content category
* `likes` - Number of likes
* `comments` - Number of comments
* `shares` - Number of shares
* `watch_time_sec` - Watch time in seconds
* `impression_count` - Number of impressions
* `posted_at` - Date of the post
* `follower_count` - Number of followers
* `is_verified` - Indicates whether the account is verified
* `device_type` - Device used by the user
* `sentiment` - Sentiment of the post
* `hashtags` - Hashtags used in the post
* `engagement_rate` - Engagement rate of the post

## Tools and Technologies

* Python
* Pandas
* Matplotlib
* Seaborn
* Plotly
* Google Colab
* GitHub

## Project Workflow

### 1. Data Import and Setup

* Imported the dataset using Pandas.
* Checked the first and last few records.
* Examined the shape, columns, data types, and basic information.
* Converted the `posted_at` column into datetime format.

### 2. Data Cleaning

* Checked for missing values using `isnull()` and `isna()`.
* Calculated missing-value percentages.
* Identified missing values in:

  * `age`
  * `gender`
  * `likes`
  * `comments`
  * `shares`
  * `sentiment`
* Checked for duplicate records.
* Checked categorical values and data types.
* Checked potentially unrealistic engagement values.
* Created hashtag counts from the `hashtags` column.

### 3. Exploratory Data Analysis

* Examined categorical distributions using:

  * `unique()`
  * `nunique()`
  * `value_counts()`
* Analyzed numerical variables using descriptive statistics.
* Created a correlation matrix for numerical variables.
* Used groupby analysis to compare:

  * Post types
  * Countries
  * Sentiments
  * Post categories

### 4. Data Wrangling

* Created an `engagement_score` using likes, comments, and shares.

```python
df['engagement_score'] = (
    df['likes'] +
    df['comments'] +
    df['shares']
)
```

* Created `hashtag_count` from the hashtags column.
* Performed groupby analysis using post type, country, and sentiment.
* Since the project uses a single main dataset, merge, join, and concat operations were not required.

### 5. Statistical Analysis

* Calculated:

  * Mean
  * Median
  * Mode
  * Standard deviation
  * Variance
  * 25th percentile
  * 50th percentile
  * 75th percentile
  * Skewness
  * Kurtosis

* Statistical analysis was performed on important engagement-related variables such as:

  * Likes
  * Comments
  * Shares
  * Watch time
  * Engagement rate
  * Follower count

## Outlier Analysis

* Used a box plot to visually inspect the distribution of `engagement_rate`.
* Applied the IQR method to identify potential outliers.
* Calculated:

  * Q1
  * Q3
  * IQR
  * Lower bound
  * Upper bound
* The engagement rate showed a strong right-skewed distribution.
* Skewness and kurtosis were also calculated to understand the distribution and extreme observations.
* Potential outliers were identified but were not automatically removed because an outlier does not necessarily represent an incorrect data value.

## Verified Account Performance

* Compared verified and non-verified accounts using:

  * Average likes
  * Average comments
  * Average shares
  * Average engagement rate
* The comparison showed differences between verified and non-verified accounts across these metrics.
* Verified accounts had slightly higher average shares and engagement rate, while non-verified accounts had higher average likes and comments.

## Data Visualization

### Matplotlib

* Likes vs impressions scatter plot
* Daily engagement trend
* Number of posts by category
* Gender distribution pie chart
* Age distribution histogram
* Engagement rate box plot

### Seaborn

* Post type count plot
* Average likes by post category
* Follower count distribution by sentiment
* Pair plot of numerical variables
* Correlation heatmap
* Engagement score by device type

### Plotly

* Interactive engagement analysis by post type

## Key Insights

* Social media engagement varies across different post types and categories.
* Likes, comments, and shares provide different perspectives on content engagement.
* Engagement rate has a strong right-skewed distribution with extreme high-value observations.
* The correlation analysis helps identify relationships between numerical engagement variables.
* Verified and non-verified accounts show differences across engagement metrics.
* Post category and post type can be compared to understand content performance.
* Country and sentiment-based analysis can help identify differences in user engagement patterns.

## Conclusion

* This project demonstrates the complete data analysis workflow using Python.
* The project covers data loading, cleaning, exploration, wrangling, statistical analysis, visualization, and insight generation.
* The analysis provides a better understanding of social media engagement patterns and demonstrates practical use of Python for Data Analytics.

