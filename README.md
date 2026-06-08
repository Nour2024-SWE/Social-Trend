# Social Media Trends Analysis

A comprehensive data analysis project examining viral social media trends and engagement patterns across multiple platforms, hashtags, content types, and regions.

## 📋 Overview

This project performs an in-depth analysis of social media engagement data to uncover patterns and insights about what makes content go viral. The analysis includes exploratory data analysis, statistical correlations, predictive modeling, and clustering to understand engagement metrics across different dimensions.

## 🎯 Key Features

- **Exploratory Data Analysis**: Distribution analysis of engagement metrics (Views, Likes, Shares, Comments)
- **Platform Analysis**: Comparison of performance across TikTok, Instagram, Twitter, and YouTube
- **Hashtag Analysis**: Top-performing hashtags and their engagement patterns
- **Content Type Analysis**: Performance comparison of Videos, Shorts, Posts, Tweets, Live Streams, and Reels
- **Regional Analysis**: Engagement patterns across different geographical regions
- **Engagement Score**: Composite weighted metric (Likes 40%, Shares 30%, Comments 30%)
- **Predictive Modeling**: Random Forest classifier for engagement level prediction
- **Clustering Analysis**: K-means clustering to identify post patterns
- **Network Analysis**: Hashtag-Platform engagement network visualization

## 📊 Dataset

The dataset contains 5,000 posts with the following attributes:
- **Post_ID**: Unique identifier for each post
- **Platform**: Social media platform (TikTok, Instagram, Twitter, YouTube)
- **Hashtag**: Primary hashtag used (#Challenge, #Education, #Dance, #Comedy, #Gaming, #Music, #Viral, #Fitness, #Tech, #Fashion)
- **Content_Type**: Type of content (Video, Shorts, Post, Tweet, Live Stream, Reel)
- **Region**: Geographic region (USA, Canada, UK, Brazil, India, Australia, Japan, Germany)
- **Views**: Number of views
- **Likes**: Number of likes
- **Shares**: Number of shares
- **Comments**: Number of comments
- **Engagement_Level**: Categorical rating (High, Medium, Low)

## 📈 Key Findings

### Platform Performance
- YouTube and Instagram dominate in terms of reach and engagement
- TikTok shows strong performance in viral content
- Twitter generates higher comment engagement relative to other metrics

### Content Type Analysis
- **Videos** and **Shorts** consistently outperform other content types
- **Live Streams** show high engagement-to-view ratios
- **Posts** and **Tweets** have lower overall engagement metrics

### Top Performing Hashtags
- #Fitness, #Education, and #Challenge show highest average engagement
- #Viral and #Music drive high share counts
- #Gaming generates strong comment engagement

### Regional Insights
- USA and Canada lead in overall engagement metrics
- India shows strong growth in video content consumption
- Brazil demonstrates high engagement in challenge and dance content

## 🛠️ Technologies Used

- **Python 3.10+**
- **Pandas** - Data manipulation and analysis
- **NumPy** - Numerical computing
- **Matplotlib & Seaborn** - Data visualization
- **Scikit-learn** - Machine learning (Random Forest, K-means, PCA)
- **NetworkX** - Network graph analysis

## 📊 Visualizations

The analysis includes the following visualizations:
1. Distribution of engagement metrics
2. Platform-wise engagement comparison
3. Regional post distribution (pie chart)
4. Engagement metrics distribution histograms
5. Top hashtag engagement analysis
6. Content type performance comparison
7. Engagement score distribution by platform
8. Hashtag-platform network graph
9. Engagement metrics over time
10. Feature importance for prediction model
11. Post clustering visualizations

## 🤖 Machine Learning Models

### Random Forest Classifier
- **Target Variable**: Engagement_Level (High/Medium/Low)
- **Features**: Platform, Hashtag, Content_Type, Region, Views, Likes, Shares, Comments
- **Performance**: Accuracy ~36% (baseline for multi-class engagement prediction)

### K-Means Clustering
- **Optimal clusters**: 3 (based on elbow method)
- **Features**: Standardized engagement metrics
- **Application**: Post segmentation based on engagement patterns

## 📁 Repository Structure

```
social-media-trends-analysis/
├── data/
│   └── Viral_Social_Media_Trends.csv
├── notebooks/
│   └── trends-on-social-media.ipynb
├── visualizations/
│   └── (generated plots)
├── requirements.txt
└── README.md
```

## 🚀 Getting Started

### Prerequisites
```bash
pip install -r requirements.txt
```

### Dependencies
```
pandas
numpy
matplotlib
seaborn
scikit-learn
networkx
```

### Run the Analysis
```bash
jupyter notebook trends-on-social-media.ipynb
```

## 📝 Key Code Examples

### Engagement Score Calculation
```python
df['Engagement_Score'] = (df['Likes'] * 0.4 + df['Shares'] * 0.3 + df['Comments'] * 0.3) / df['Views']
```

### Platform Analysis
```python
most_viewed = df.loc[df.groupby('Platform')['Views'].idxmax(), 
                      ['Platform', 'Post_ID', 'Region', 'Views', 'Hashtag']]
```

### Correlation Analysis
```python
correlation_matrix = df[['Views', 'Likes', 'Shares', 'Comments']].corr()
```

## 📈 Results Summary

| Platform | Best Performing Content | Top Hashtag |
|----------|------------------------|--------------|
| TikTok   | Dance Videos | #Dance |
| Instagram | Music Posts | #Music |
| Twitter | Challenge Videos | #Challenge |
| YouTube | Dance Shorts | #Dance |

## 🔮 Future Improvements

1. **Time-based analysis**: Incorporate temporal patterns for seasonal trends
2. **Sentiment analysis**: Add sentiment scoring for comments
3. **Deep learning models**: Implement neural networks for engagement prediction
4. **Real-time monitoring**: Develop streaming analytics pipeline
5. **A/B testing framework**: Test content strategies

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👥 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📧 Contact

For questions or feedback, please open an issue in the repository.


