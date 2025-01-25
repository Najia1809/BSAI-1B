# Top Ranked Social Media Platforms Analysis

## Overview

This project analyzes the top-ranked social media platforms using Python and the Pandas library. The dataset contains information about various social media platforms, including their launch year, category, primary feature, active users, and target audience.

## Dataset

The dataset includes the following columns:

- `Platform Name`: Name of the social media platform
- `Launch Year`: Year the platform was launched
- `Category`: Type of platform (e.g., Social Networking, Messaging, Video Sharing)
- `Primary Feature`: Main functionality of the platform
- `Active Users (Million)`: Number of active users (in millions)
- `Target Audience`: The primary audience for the platform

## Requirements

Ensure you have the following dependencies installed:

```bash
pip install pandas
```

## Code Example

```python
import pandas as pd

# Load dataset
data = pd.read_csv('topranks.csv')

# Display basic information
data.info()

# Display top 5 platforms by active users
top_platforms = data.sort_values(by='Active Users (Million)', ascending=False)
print("Top 5 Social Media Platforms:")
print(top_platforms[['Platform Name', 'Active Users (Million)']].head())

# Calculate how many times data have come in each coloumn
df['Platform'].value_counts()  
```

## Output Example

```Top 5 Social Media Platforms:
    Platform Name  Active Users (Million)
0      Facebook                   2900
1       YouTube                   2200
2      WhatsApp                   2000
3     Instagram                   1500
4        TikTok                   1200

Number of platforms by category:
Social Networking    3
Messaging            1
Video Sharing        1

Average number of active users (in millions): 234.96
```

## Conclusion

- Facebook leads with the highest number of active users.
- Social Networking is the most common category among the platforms.
- The average number of active users across platforms is approximately 234.96 million.
