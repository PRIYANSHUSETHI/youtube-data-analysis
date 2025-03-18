# YouTube Data Collection and Analysis

## Overview
This project is designed to collect and analyze trending YouTube videos using the YouTube Data API. The script fetches trending videos, extracts key metrics, processes the data, and performs exploratory data analysis to identify patterns in video engagement, content duration, and posting time.

## Features
- Fetches trending YouTube videos from the US region using the YouTube Data API.
- Extracts key metrics such as views, likes, comments, and category.
- Saves the data into a CSV file for further analysis.
- Cleans and preprocesses the data (handling missing values, converting timestamps, parsing video duration).
- Performs exploratory data analysis (EDA) with visualizations:
  - Distribution of views, likes, and comments.
  - Correlation analysis between engagement metrics.
  - Analysis of trending video categories.
  - Impact of video duration and tags on views.
  - Effect of video posting time on engagement.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo-name.git
   ```
2. Install the required Python libraries:
   ```bash
   pip install pandas google-api-python-client seaborn matplotlib isodate
   ```
3. Obtain a YouTube Data API Key from Google Cloud and replace `YOUR_API_KEY` in the script.

## Usage
Run the script to fetch and analyze trending YouTube videos:
```bash
python youtube_data_collection_and_analysis.py
```

## Functions
### `get_trending_videos(api_key, max_results=200)`
- Fetches trending YouTube videos from the US region.
- Extracts:
  - Video ID, title, description, channel details, category, tags, duration.
  - Engagement metrics (views, likes, comments, etc.).
- Supports pagination to fetch up to `max_results` videos.

### `save_to_csv(data, filename)`
- Saves the extracted data into a CSV file for analysis.

### `get_category_mapping()`
- Maps category IDs to human-readable category names.

### `parse_duration(duration_str)`
- Converts video duration from ISO 8601 format to seconds.

## Analysis Highlights
### Engagement Metrics
- **Right-skewed distribution:** Most videos have fewer views, likes, and comments.
- **High correlation:** Views, likes, and comments are strongly correlated.

### Category Insights
- Certain categories have higher engagement levels than others.
- Visualization of trending videos by category.

### Impact of Video Duration
- Categorizes videos into bins (0-5 min, 5-10 min, etc.).
- Analyzes engagement levels based on video length.

### Effect of Tags on Views
- Scatter plot analysis to see if the number of tags influences views.

### Posting Time Analysis
- Distribution of videos by posting hour.
- Scatter plot showing the relationship between posting time and views.

## Recommendations
1. **Optimize Video Length:** Videos around 5-10 minutes receive higher engagement.
2. **Category Selection:** Certain categories trend more frequently; focus on high-engagement categories.
3. **Tag Usage:** Strategic use of tags may help improve discoverability.
4. **Best Posting Time:** Posting at specific hours may impact video reach.
