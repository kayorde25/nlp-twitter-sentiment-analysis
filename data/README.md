# Dataset Instructions

This folder is intended to store the dataset files required to run the project.

---

## Dataset Source

The dataset used in this project is:

**Twitter Airline Sentiment Dataset**  
https://www.kaggle.com/datasets/crowdflower/twitter-airline-sentiment

---

## Required Files

After downloading and extracting the dataset, this folder should contain:

- `Tweets.csv`
- `database.sqlite` (optional)

Only `Tweets.csv` is required to run the notebook.

---

## How to Download

### Option 1 — Kaggle (Recommended)

Run the following command in your notebook:

```python
!kaggle datasets download -d crowdflower/twitter-airline-sentiment -p data
