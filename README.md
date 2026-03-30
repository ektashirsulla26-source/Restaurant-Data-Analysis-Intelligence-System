<div align="center">

# 🍽️ Restaurant Data Analysis & Intelligence System

### A multi-level data science project analyzing global restaurant trends, ratings, pricing, and customer behavior

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org)
[![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org)
[![Folium](https://img.shields.io/badge/Folium-Geospatial-77B829?style=for-the-badge)](https://python-visualization.github.io/folium/)
[![Status](https://img.shields.io/badge/Status-Completed-22C55E?style=for-the-badge)]()

<br/>

| 🍴 Restaurants Analyzed | 📊 Analysis Levels | 🤖 ML Models | 🌍 Geospatial |
|:---:|:---:|:---:|:---:|
| **Global Dataset** | **3 Levels · 9 Tasks** | **Random Forest + KMeans + DBSCAN** | **Folium Map Clustering** |

</div>

---

## 📌 Project Overview

This project performs an **end-to-end restaurant intelligence analysis** on a global Zomato-style dataset. It covers everything from basic data cleaning and exploratory analysis to machine learning classification, geospatial restaurant clustering, restaurant chain analysis, and sentiment scoring — structured across **3 progressive levels** of increasing complexity.

> 💡 Core Question: *What factors — cuisine, location, price, delivery, and reviews — most influence restaurant ratings and customer engagement?*

---

## 🎯 Objective

- Identify the top cuisines, cities, and price segments driving restaurant success
- Understand how **online delivery** and **table booking** affect aggregate ratings
- Segment restaurants into behavioral clusters using **KMeans and DBSCAN**
- Build a **classification model** to predict a restaurant's rating category
- Detect **restaurant chains** and analyze their popularity vs. independent outlets
- Perform **votes analysis** and **sentiment analysis** on rating text

---

## 📦 Dataset Information

| Field | Details |
|:------|:--------|
| **Source** | Zomato-style global restaurant dataset |
| **File** | `Dataset.csv` |
| **Key Columns** | Restaurant ID, Name, City, Cuisines, Average Cost for Two, Price Range, Has Table Booking, Has Online Delivery, Aggregate Rating, Rating Text, Votes, Latitude, Longitude |
| **Target Variable** | `Aggregate Rating` (regression) / `Rating Text` (classification) |

---

## 🔧 Tech Stack

| Category | Tools |
|:---------|:------|
| **Language** | Python 3.x |
| **Data Handling** | Pandas, NumPy |
| **Visualization** | Matplotlib, Seaborn |
| **Machine Learning** | Scikit-learn (Random Forest, KMeans, DBSCAN) |
| **Geospatial** | Folium, MarkerCluster |
| **NLP / Sentiment** | NLTK (VADER SentimentIntensityAnalyzer) |
| **Statistics** | SciPy (t-test, ANOVA, chi-square) |
| **Environment** | Jupyter Notebook / Google Colab |

---

## ⚙️ Project Pipeline
```
01 → Data Loading & Inspection      Shape, dtypes, nulls, duplicates, unique counts
02 → Data Cleaning                  Handle missing values, standardize columns
03 → Univariate Analysis            Ratings distribution, price range, top cuisines & cities
04 → Bivariate Analysis             Rating vs votes, cost vs rating, delivery vs rating
05 → Multivariate Analysis          Correlation heatmap across numeric features
06 → Statistical Testing            t-test (table booking), ANOVA (city costs), chi-square
07 → ML Classification              Predict rating category using Random Forest
08 → ML Clustering                  Segment restaurants via KMeans (k=4) + DBSCAN
09 → Geospatial Mapping             Plot restaurant locations using Folium + MarkerCluster
```

---

## 📋 Analysis Levels & Tasks

### 🔵 Level 1 — Foundational Analysis

| Task | Description |
|:-----|:------------|
| **Task 1 — Top Cuisines** | Identify top 3 cuisines; calculate % of restaurants serving each |
| **Task 2 — City Analysis** | City with most restaurants; average rating per city; top-rated city |
| **Task 3 — Price Range** | Distribution of price ranges; % of restaurants per price tier |
| **Task 4 — Online Delivery** | % offering delivery; compare avg ratings with vs. without delivery |

### 🟡 Level 2 — Intermediate Analysis

| Task | Description |
|:-----|:------------|
| **Task 1 — Rating Distribution** | Histogram of ratings; most common range; avg votes analysis |
| **Task 2 — Cuisine Combinations** | Top 10 cuisine combos; highest-rated combinations (min 5 restaurants) |
| **Task 3 — Geospatial Analysis** | Map restaurants via Folium; DBSCAN clustering by location |
| **Task 4 — Restaurant Chains** | Identify chains; compare chain vs. independent ratings and popularity |

### 🔴 Level 3 — Advanced Analysis

| Task | Description |
|:-----|:------------|
| **Task 1 — Sentiment Analysis** | VADER sentiment on Rating Text; score vs. aggregate rating |
| **Task 2 — Votes Analysis** | Top/bottom restaurants by votes; correlation between votes and rating |

---

## 📈 Key Insights

- 🍛 **North Indian** and **Chinese** cuisines are the most common across restaurants
- 🏙️ **New Delhi** has the highest number of restaurants in the dataset
- 🚚 Restaurants **with online delivery** have a measurably higher average rating than those without
- 📋 Restaurants **with table booking** consistently outperform those without across rating categories
- 📊 **Higher votes strongly correlate** with higher aggregate ratings (positive correlation)
- 🔵 KMeans clustering reveals **4 distinct restaurant segments** by cost, votes, and rating
- 🔗 Restaurant **chains show higher vote counts** but mixed ratings vs. independent outlets
- 💬 VADER sentiment scores on rating text align closely with the numeric aggregate rating

---

## 📊 ML Model Summary

| Model | Type | Purpose |
|:------|:-----|:--------|
| **Random Forest Classifier** | Supervised | Predict rating category (Poor / Average / Good / Excellent) |
| **KMeans Clustering (k=4)** | Unsupervised | Segment restaurants by cost, votes, and rating |
| **DBSCAN** | Unsupervised | Detect geospatial clusters and outlier restaurant locations |

---

## 📂 Project Structure
```
restaurant-analysis/
│
├── notebooks/
│   └── notebook_1.ipynb          # Full analysis notebook (all 3 levels)
│
├── data/
│   └── Dataset.csv               # Raw restaurant dataset
│
├── outputs/
│   ├── rating_distribution.png
│   ├── top_cuisines.png
│   ├── price_range_dist.png
│   ├── delivery_vs_rating.png
│   ├── cuisine_combinations.png
│   ├── restaurant_map.html       # Interactive Folium map
│   └── chain_popularity.png
│
└── README.md
```

---

## 🚀 How to Run
```bash
# 1. Clone the repository
git clone https://github.com/ektashirsulla26-source/data-science-assignment.git
cd data-science-assignment

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn folium nltk scipy

# 3. Launch the notebook
jupyter notebook notebooks/notebook_1.ipynb
```

---

## ✅ Conclusion

- This project demonstrates a complete data science workflow applied to restaurant analytics.
- The analysis confirms that **service features** (online delivery, table booking) have a statistically significant impact on ratings.
- **Geospatial clustering** reveals concentrated hotspots of restaurant activity.
- While **machine learning models** successfully classify and segment restaurants with strong accuracy.
- The multi-level task structure showcases progressive analytical depth — from basic EDA to NLP and geospatial intelligence.

---

## 👤 Author

**Ekta Shirsulla** — Data Scientist · Restaurant Analytics · ML & EDA

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/ekta-shirsulla/)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ektashirsulla26-source)

---

<div align="center">
<sub>Built with 🐍 Python · 📓 Jupyter · 🤖 Scikit-learn · 🌍 Folium · 💬 NLTK</sub>
</div>
