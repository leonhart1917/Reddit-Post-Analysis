# Reddit-Post-Analysis
## Assignment Overview
This project demonstrates how to use the Reddit API and via PRAW to collect, clean, and analyze Reddit posts.  
The project retrieves "hot" posts and performs keyword-based searches across multiple subreddits on a single topic (e.g., Data Science).  
The results are merged into a clean, structured dataset for further analysis.


## How to Run

### 1. Prerequisites
- Python **3.8+**
- Or Google Colab
- Reddit API credentials (you can generate them at [https://www.reddit.com/prefs/apps]

### 2. Installation
Install all required dependencies:
```bash
pip install -r requirements.txt
```

### 3. Configuration
Create a file named **`reddit.env`** in the same directory as your Python script.  
This file stores your Reddit API credentials securely and allows the program to authenticate with Reddit through the PRAW library.

Example `reddit.env` file:

**Important:**  
> - Do **not** upload your real credentials to GitHub or Canvas.  
> - Include only this **template** file with placeholder values.  
> - The grader can replace these placeholders with their own credentials to test the script.

---

### 4. Execution
To run the data collection script, open your terminal or IDE and execute:

```bash
python reddit_api.py
Or run file Reddit_API.ipynb on Google Colab
```
### 5 After running the script, a CSV file named **`reddit_data.csv`** will be created in your working directory.  
This file contains all collected Reddit posts — both *hot* posts and *keyword-search* posts — merged into one clean, structured dataset.

Each row in the dataset represents a single Reddit post.  
The file includes the following columns:

| Column | Description |
|---------|-------------|
| **Title** | Title of the Reddit post |
| **Score** | Number of upvotes received by the post |
| **Upvote_ratio** | Ratio of upvotes to total votes |
| **Num_comments** | Total number of comments on the post |
| **Author** | Username of the author (shows `[deleted]` if unavailable) |
| **Subreddit** | Subreddit where the post was found |
| **URL** | Direct link to the post or shared media |
| **Permalink** | Reddit permalink (URL path within reddit.com) |
| **Created_utc** | Unix timestamp for when the post was created |
| **Is_self** | Boolean indicating if it’s a self/text post |
| **Selftext** | Body text of the post (truncated to 500 characters) |
| **Flair** | User-assigned flair (if any) |
| **Domain** | The domain source (e.g., `reddit.com`, `youtube.com`, etc.) |
| **Search_query** | Keyword used for search-based posts (empty for hot posts) |. Output description

