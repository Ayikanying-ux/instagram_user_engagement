# Instagram Analytics

![Instagram Analytics](https://example.com/instagram-analytics.png)

## Overview

Instagram Analytics is a Python tool designed to analyze user engagement on the Instagram platform. The tool processes a sample of user data and their interactions with photos, tags, likes, follows, and comments. By leveraging this data, the product team can derive valuable insights for marketing, product development, and business strategies.

## Features

- Load and clean user data, likes, follows, photos, tags, photo tags, and comments from CSV files.
- Explore user demographics, photo characteristics, and user interactions.
- Visualize user age distribution and user gender distribution.
- Analyze user engagement by merging relevant data based on common columns.
- Extract insights on photo popularity, tag trends, and user interactions.

## Installation

1. Clone the repository from GitHub:
2. Install the required dependencies:
3. Prepare the data files:

Place the CSV data files (`users.csv`, `likes.csv`, `follows.csv`, `photos.csv`, `tags.csv`, `photo_tags.csv`, `comments.csv`) in the project's data directory.

## Usage

1. Import the `InstagramAnalytics` class:

```python
from instagram_analytics import InstagramAnalytics
analytics = InstagramAnalytics()
datasets = {
    "users": "data/users.csv",
    "likes": "data/likes.csv",
    "follows": "data/follows.csv",
    "photos": "data/photos.csv",
    "tags": "data/tags.csv",
    "photo_tags": "data/photo_tags.csv",
    "comments": "data/comments.csv"
}

analytics.load_data(datasets)
analytics.clean_data()
# Display the first 5 rows of users_df
analytics.users_df.head()

# Visualize user age distribution
analytics.plot_user_age_distribution()
# Merge DataFrames for specific analysis
merged_users_likes, merged_photos_likes_comments, merged_photos_tags = analytics.merge_dataframes()

# ... Further analysis based on merged DataFrames
```
