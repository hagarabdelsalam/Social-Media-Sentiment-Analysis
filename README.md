# Social Media Sentiment Analysis using Sentiment140 🐦💬

## 📌 Project Overview

This project performs sentiment analysis on social media data, specifically Twitter data from the **Sentiment140** dataset. Using natural language processing (NLP) and machine learning techniques, we classify tweets as **Positive** or **Negative**, visualize word trends, and analyze sentiment patterns over time.

---

## 🧾 Dataset

- **Source**: [Sentiment140](https://www.kaggle.com/datasets/kazanova/sentiment140)
- **Size**: 1.6 million labeled tweets
- **Columns Used**: 
  - `sentiment`: 0 = Negative, 4 = Positive
  - `text`: Raw tweet content

---

## 🧪 Project Workflow

### 1. Data Loading & Preprocessing
- Loaded the CSV with `latin-1` encoding
- Selected relevant columns (`sentiment`, `text`)
- Mapped sentiment labels:  
  - `0 → Negative`  
  - `4 → Positive`

### 2. Text Cleaning (NLP)
- Removed:
  - URLs, mentions, hashtags
  - Special characters
- Converted text to lowercase
- Removed stopwords (NLTK)
- Applied stemming (Porter Stemmer)
- Created `clean_text` column

### 3. Visualizations

#### ✅ Sentiment Distribution
- Countplot of Positive vs Negative tweets  
**Insight**: Balanced dataset

#### ☁️ Word Clouds
- Visualized common words in:
  - Positive tweets (e.g., *love*, *good*)
  - Negative tweets (e.g., *bad*, *hate*)

#### 📈 Sentiment Trend Over Time
- Simulated tweet timestamps
- Resampled by day using `pandas`
- Smoothed using 7-day rolling average  
**Insight**: Periodic spikes may indicate public response to events

---

## 🤖 Sentiment Classification

- **Vectorization**: `CountVectorizer`
- **Model**: `Multinomial Naive Bayes`
- **Split**: 80% Train / 20% Test
- **Evaluation**: `classification_report`

### 🔍 Model Results:
- **Accuracy**: ~77%
- **Precision & Recall**: Balanced between classes  
**Insight**: Even simple models can be effective with proper preprocessing.

---

## 🛠️ Tech Stack

- Python (Pandas, Numpy, Seaborn, Matplotlib)
- NLTK (NLP Preprocessing)
- Scikit-learn (ML Modeling)
- WordCloud (Text Visualization)

---

---

## ✨ Future Improvements

- Incorporate Neutral sentiment (score 2)
- Use advanced models (e.g., Logistic Regression, BERT)
- Analyze real-time Twitter data using Twitter API

---

## 📬 Contact

For questions or collaboration:  
**Hagar Abdelsalam** - [hagarabdelsalam64@gmail.com]  
**www.linkedin.com/in/hagar-abd-el-salam-863a98259** 



