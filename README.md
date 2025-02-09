# 📹YouTube Channel Performance Analysis: Ayusy

## ✏️ Overview
This project focuses on analyzing the performance of the **Ayusy** YouTube channel using data extracted via the YouTube API. The goal is to identify patterns and actionable insights to improve the channel's reach and engagement. The analysis covers key metrics such as views, likes, comments, video duration, tags, and more.

---

## ✏️ Aim and Objectives
### Aim
To conduct an exploratory data analysis (EDA) of video performance data from the Ayusy YouTube channel and provide data-driven recommendations to optimize content strategy and engagement.

### Objectives
1. **Utilize YouTube API**: Extract and analyze video data to understand YouTube analytics.
2. **Analyze Video Performance**: Investigate factors influencing video performance, including:
   - Impact of engagement (likes, comments) on views.
   - Effect of video duration on engagement.
   - Influence of title length and tags on video performance.
3. **Audience Interaction**: Analyze viewer comments to identify common themes and improve future content.

---

## ✏️ Data Collection
Data was collected using the **YouTube Data API v3**. The following steps were performed:
1. **Channel Statistics**: Extracted channel-level metrics (subscribers, views, total videos).
2. **Video Details**: Retrieved metadata for all videos (title, description, tags, views, likes, comments, duration).
3. **Comments**: Collected top-level comments for each video (limited to 10 comments per video due to API constraints).

### ✏️ Libraries Used
- **Pandas, NumPy**: Data manipulation and analysis.
- **Matplotlib, Seaborn, Plotly**: Data visualization.
- **Google API Client**: Access YouTube API.
- **NLTK**: Natural Language Processing for comment analysis.

---

## ✏️ Data Preprocessing
1. **Handling Missing Values**: Checked for null values and converted count columns to numeric types.
2. **Feature Engineering**:
   - Converted `publishedAt` to datetime format and extracted the day of the week.
   - Transformed video duration from ISO format to seconds.
   - Calculated metrics like tags count, likes/comments per 1000 views, and title length.

---

## ✏️ Exploratory Data Analysis (EDA)
### Key Insights
1. **Engagement Distribution**:
   - Most videos have low engagement, with a few outliers achieving high views and likes.
   - Right-skewed distributions for views, likes, and comments indicate that only a small subset of videos performs exceptionally well.

2. **Publish Day Analysis**:
   - **Optimal Days**: Saturday and Sunday yield the highest average views, likes, and comments.
   - **Less Effective Days**: Monday to Wednesday show lower engagement.

3. **Video Duration**:
   - Videos shorter than 8 minutes (500 seconds) tend to perform better.
   - Longer videos (>500 seconds) see a drop in engagement.

4. **Engagement Ratios**:
   - Videos with higher likes and comments per 1000 views are considered high-engagement.
   - Identifying patterns in these videos can help replicate success.

5. **Correlation Analysis**:
   - Strong positive correlation between views and likes (0.94).
   - Moderate correlation between views and comments (0.65).
   - Weak negative correlation between video duration and engagement.

6. **Tags and Titles**:
   - No clear relationship between the number of tags and views.
   - Title length does not significantly impact views, but concise and descriptive titles are recommended.

---

## ✏️ Visualisations
1. **Distribution of Views, Likes, and Comments**:
   [Distribution Plots](/Plots/1.Distribution of Views, likes and comments.png)
2. **Average Engagement by Publish Day**:
   [Publish Day Analysis](/Plots/2.Average views, likes, and comments by publish day.png) 
3. **Video Duration vs Engagement**:
   [Duration Analysis](/Plots/3.Scatter plot for video duration vs views, likes, comments.png)
4. **Correlation Heatmap**:
   [Correlation Heatmap](/Plots/5.Correlation heatmap.png)

---

## ✏️ Conclusion
- **Optimal Publishing**: Post videos on weekends (Saturday and Sunday) for higher engagement.
- **Video Length**: Keep videos under 8 minutes to retain viewer interest.
- **Engagement Strategies**: Focus on creating content that encourages likes and comments to boost engagement ratios.
- **Tags and Titles**: Use relevant tags and concise, descriptive titles to improve discoverability.

---

## ✏️ Future Work
1. **Content Experimentation**: Test different video formats and lengths to identify what resonates with the audience.
2. **Audience Analysis**: Dive deeper into viewer demographics and preferences.
3. **Advanced NLP**: Perform sentiment analysis on comments to gauge audience sentiment.
4. **A/B Testing**: Experiment with different titles, thumbnails, and tags to optimize performance.
