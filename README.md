## 📌 Project Overview

This project aims to help a fictional app development company decide what kind of free app to build for both the Google Play Store and Apple App Store. Since the company only builds free-to-download apps and revenue is driven mainly by in-app ads, the goal is to create an app that attracts as many users as possible.

To achieve this, I analyzed two datasets: one for Android apps (Google Play) and one for iOS apps (App Store), to identify the most successful app genres based on user engagement.

------

## 🗂️ Datasets Used

- Google Play Store dataset: Includes app names, categories, genres, reviews, installs, ratings, and more.

- Apple App Store dataset: Contains app names, primary genres, ratings, rating counts, and other relevant info.

Both datasets are from open data sources and reflect the state of the stores as of around 2018.

------

## 🧹 Data Cleaning & Preparation

✅ Android Dataset

- Removed duplicate entries: Found 1,181 duplicate apps. Kept only the row with the highest number of reviews (i.e. the most recent data point).

- Removed entries with missing or corrupted data: For example, row 10472 had '3.0M' in the reviews column, which is invalid.

- Filtered out non-English apps

- Kept only free apps


✅ iOS Dataset

- Dataset was mostly clean

- Checked for duplicates and found none

- Filtered to keep only English-language and free apps

------

## 📊 Exploratory Data Analysis

🎯 Objective

Identify app genres that are:

- Popular across both platforms

- Have high user engagement, as shown by:

   - Number of installs (Android)

   - Total rating counts (iOS)

------

## 📈 Frequency Analysis

🔹 Most Common Genres (Android):

Used the Genres and Category columns to determine distribution.

Top genres by count:

- Family

- Game

- Tools

- Productivity


🔹 Most Common Genres (iOS):

Based on prime_genre column.

Top genres by count:

- Games

- Entertainment

- Education

- Photo & Video

However, frequency does not necessarily correlate with popularity or profitability... Some genres are overcrowded.

------

## ⭐ Popularity by Genre

Instead of just frequency, I calculated the average number of installs or rating counts per genre:

🔸 iOS (Average User Ratings per Genre)

Calculated average total user ratings (proxy for popularity):

| Genre             | Avg. User Ratings |
| ----------------- | ----------------- |
| Navigation        | \~860,000+        |
| Reference         | \~740,000+        |
| Social Networking | \~530,000+        |
| Music             | \~400,000+        |
| Weather           | \~330,000+        |

Insight: High-rated genres are often utility or niche-focused apps like GPS, dictionaries, or social platforms.


🔸 Android (Average Installs per Genre)

Cleaned the Installs column and removed non-numeric characters, then calculated:

| Genre         | Avg. Installs |
| ------------- | ------------- |
| Communication | \~38M         |
| Video Players | \~25M         |
| Social        | \~23M         |
| Productivity  | \~15M         |
| Photography   | \~12M         |

Insight: Communication, social media, and media apps dominate in install counts, but are highly competitive.

------

## 💡 Key Findings

- While Games dominate in count, communication, productivity, and reference tools have higher average installs and ratings.

- Navigation, Reference, and Social Networking genres tend to attract massive user bases, especially if they serve a unique need.

- The most successful genres combine utility with engagement, like apps that help people solve real-world problems and have a fun or social element (e.g. gamified to-do lists, fitness trackers with social features).

------

## ✅ Conclusion

To maximize reach and engagement for a new app, I recommend developing a free utility app with added engagement mechanisms, such as:

- A productivity app with gamification

- A habit tracker with social features

- A reference or learning app with interactive tools

These genres are proven to attract users and provide long-term value, increasing the chance of retention and ad revenue.

------

## 🛠️ Technologies Used

- Python (Jupyter Notebook)

- Data cleaning with lists, for loops, and conditionals

- Custom functions for frequency analysis

- Git & GitHub for version control

------

## 📁 Project Structure

├── app-profile-analysis.ipynb   # Main notebook
├── apple-store.csv              # iOS dataset
├── google-play-store.csv        # Android dataset
├── README.md                    # Project overview and insights

------

## 🙋‍♀️ About Me

I'm a beginner data analyst learning through hands-on projects like this. This analysis helped me practice real-world data cleaning, exploration, and storytelling techniques. I’m currently expanding my skills in Python, data visualization, and statistical modeling.
