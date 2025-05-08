# 🎮 Movie Review Sentiment Analysis

This project performs sentiment analysis on movie reviews using a variety of natural language processing (NLP) techniques. It includes both traditional and modern methods for text representation and classification.

---

## 🔍 Project Overview

* **Goal:** Classify movie reviews as positive or negative
* **Dataset:** IMDb-style dataset with labeled reviews (`review`, `sentiment`)
* **Original Data Source:** [Stanford Large Movie Review Dataset (IMDB)](https://ai.stanford.edu/~amaas/data/sentiment/)
* **Approaches Used:**

  * VADER sentiment scoring (baseline)
  * TF-IDF vectorization
  * BERT embeddings
  * K-Nearest Neighbors (KNN) classification
  * EDA & feature analysis

---

## 🧪 Features & Techniques

### ✅ Sentiment Labeling

* Baseline sentiment scores generated using VADER (`compound_score`)
* Threshold: score ≥ 0 → positive; score < 0 → negative

### 📊 Exploratory Data Analysis (EDA)

* Review length distribution
* Top TF-IDF words
* VADER sentiment score distribution
* Word importance per class

### 🧠 Feature Engineering

* TF-IDF with n-grams (1,2)
* BERT embeddings using `sentence-transformers`

### 🧪 Modeling

* **TF-IDF + KNN**

  * Best `k`: 18
  * Accuracy: \~70.75%
* **BERT + KNN**

  * Best `k`: 13
  * Accuracy: \~80.30%
* **Baseline VADER**

  * Accuracy: \~69.34%

### 🎨 Visualization

* Confusion matrices
* Sentiment score histograms

---

## 🗂️ File Structure

```
📁 FinalProject-MovieReviews/
│
├── movies review.ipynb              # Main Jupyter notebook
├── train_reviews.csv                # Training data
├── test_reviews.csv                 # Test data
├── bert_embeddings/
│   ├── train_bert_embeddings.npy    # Cached BERT vectors
│   └── test_bert_embeddings.npy     # Cached BERT vectors
└── README.md                        # Project documentation
```

---

## ⚙️ Requirements

Install the following dependencies:

```bash
pip install -r requirements.txt
```

---

## 🚀 How to Run

1. Clone the repository
2. Open `movies review.ipynb` in Jupyter or PyCharm
3. Run cells in order for EDA, feature extraction, and model evaluation

---

## 📈 Sample Results

* **BERT KNN**: Best `k = 13`, Accuracy: **0.8030**
* **TF-IDF KNN**: Best `k = 18`, Accuracy: **0.7075**
* **VADER Baseline**: Accuracy: **0.6934**
* Top words in positive vs. negative reviews

---
