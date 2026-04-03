# Twitter Airline Sentiment Analysis with TF-IDF and Baseline Machine Learning Models

A complete Natural Language Processing (NLP) pipeline for sentiment classification of airline tweets using TF-IDF feature engineering and classical machine learning models.

---

## Overview

This project builds a multi-class sentiment classification model to analyze customer feedback from airline-related tweets.

The workflow includes:

- Data loading from Kaggle
- Exploratory Data Analysis (EDA)
- Text preprocessing and cleaning
- Feature engineering using TF-IDF
- Training multiple baseline machine learning models
- Model evaluation and comparison

---

## Why This Matters

Airline companies receive large volumes of customer feedback on social media platforms such as Twitter.

Understanding sentiment in real time enables:

- Improved customer experience
- Faster response to negative feedback
- Identification of operational issues
- Data-driven decision-making

This project demonstrates how NLP can transform raw text into actionable insights.

---

## Dataset

- **Source:** Kaggle  
- **Dataset:** Twitter Airline Sentiment  
- **Link:** https://www.kaggle.com/datasets/crowdflower/twitter-airline-sentiment  

### Dataset Description

The dataset contains tweets about U.S. airlines labeled with sentiment:

- Positive  
- Neutral  
- Negative  

### Files Used

- `Tweets.csv` — main dataset used for analysis  
- `database.sqlite` — optional (not used in this project)  

---

## Methodology

### 1. Data Preparation

- Loaded dataset from Kaggle
- Selected relevant columns:
  - `text`
  - `airline_sentiment`
- Handled missing values
- Encoded labels using `LabelEncoder`

---

### 2. Exploratory Data Analysis

- Analyzed class distribution
- Checked for missing values
- Explored tweet length distribution

---

### 3. Text Preprocessing

- Converted text to lowercase
- Removed URLs, mentions, and special characters
- Removed extra whitespace
- Generated cleaned text column

---

### 4. Feature Engineering

- Used **TF-IDF Vectorization**
- Included unigrams and bigrams
- Limited feature size to 5000 for efficiency

---

### 5. Model Training

Three baseline models were trained:

- Logistic Regression  
- Multinomial Naive Bayes  
- Linear Support Vector Machine (SVM)  

---

### 6. Evaluation

Models were evaluated using:

- Accuracy  
- Precision, Recall, F1-score  
- Confusion matrix  
- Model comparison plots  

---

## Exploratory Data Analysis

Key findings:

- The dataset is **imbalanced**, with more negative tweets  
- Tweets are generally short (<150 characters)  
- Some noise exists due to informal language and abbreviations  

---

## Text Preprocessing

Text cleaning significantly improved model input quality by:

- Removing noise (URLs, mentions)
- Standardizing text
- Reducing irrelevant tokens

---

## Baseline Models

The following models were evaluated:

| Model                | Description |
|---------------------|------------|
| Logistic Regression | Strong linear baseline for text classification |
| Naive Bayes         | Fast probabilistic model |
| Linear SVM          | Effective for high-dimensional sparse data |

---

## Results

- Logistic Regression and Linear SVM achieved the best performance  
- Naive Bayes provided a fast but slightly weaker baseline  

### Key Observations

- Linear models perform well on TF-IDF features  
- Class imbalance affects performance on minority classes  
- Most misclassifications occur between neutral and negative sentiments  

---

## Key Insights

- TF-IDF is highly effective for traditional NLP tasks  
- Linear models are strong baselines for text classification  
- Data cleaning plays a critical role in performance  
- Model evaluation should go beyond accuracy  

---

## Limitations

- Dataset imbalance affects model fairness  
- No deep learning models were used  
- Limited feature engineering beyond TF-IDF  
- Contextual meaning (sarcasm, tone) not fully captured  

---

## Future Improvements

- Implement deep learning models (LSTM, BERT)  
- Use advanced embeddings (Word2Vec, GloVe)  
- Apply class balancing techniques  
- Deploy model using Streamlit or FastAPI  
- Add real-time inference capability  

---

## Reproducibility

To reproduce this project:

### Step 1 — Get Kaggle API Key

1. Go to https://www.kaggle.com/account  
2. Click **Create New API Token**
   
Alternatively, you may run the following command:
!kaggle datasets download -d crowdflower/twitter-airline-sentiment -p data
 

---

### Step 2 — Run in Colab or Local

```bash
pip install -r requirements.txt
