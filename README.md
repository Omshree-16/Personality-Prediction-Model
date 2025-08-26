# 🧠 Personality Prediction Model

Predicting MBTI (Myers-Briggs Type Indicator) personality types from textual data using Machine Learning and NLP techniques.

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/) 
[![Made with ❤️](https://img.shields.io/badge/Made%20with-%E2%9D%A4-red)](#)

---

## 📌 Project Overview

This project aims to classify users into **16 MBTI personality types** based on their written texts. We use real user-generated content from Kaggle forums and MBTI-labeled data to build and evaluate multiple classification models using NLP preprocessing and machine learning algorithms.

> 🧭 Personality Types include: ISTJ, INFP, ENTP, ESFP, etc.

---

## 🗂️ Dataset Used

1. [`mbti_1.csv`](https://www.kaggle.com/datasets/datasnaek/mbti-type): MBTI-labeled text data.
2. [`ForumMessages.csv`](https://www.kaggle.com/datasets/kaggle/meta-kaggle): Raw forum posts from Kaggle users.

We use `opendatasets` to programmatically download these datasets.

---

## ⚙️ Technologies & Tools

- **Languages**: Python
- **Libraries**:
  - NLP: `NLTK`, `BeautifulSoup`, `re`, `string`
  - ML: `Scikit-learn`, `ExtraTreesClassifier`, `LogisticRegression`, `MultinomialNB`
  - Visualization: `Seaborn`, `Matplotlib`, `Plotly`
- **Others**: `opendatasets`, `pandas`, `numpy`

---

## 🧹 Data Preprocessing Steps

- Cleaning HTML tags and URLs
- Removing punctuation, numbers
- Lowercasing and stemming using SnowballStemmer
- Handling missing values
- Aggregating forum user messages
- Token and vector transformation using `TfidfVectorizer` / `CountVectorizer`
- Optional: `TruncatedSVD` for dimensionality reduction

---

## 🤖 Machine Learning Models

We tested several models using **5-fold stratified cross-validation**:

| Model                | Accuracy | F1 Score | Log Loss |
|---------------------|----------|----------|----------|
| ExtraTrees + SVD    | ✅        | ✅        | ✅        |
| Naive Bayes          | ✅        | ✅        | ✅        |
| **Logistic Regression (Best)** | ✅✅✅ | ✅✅✅ | ✅✅✅ |

---

## 📊 Visualizations

- Barplot of personality type distribution in training set.
- Predicted distribution of personality types in Kaggle forums.
- Interactive pie chart of predicted personality percentages.


---

## 🚀 How to Run

1. Clone this repository:

```bash
git clone https://github.com/Omshree-16/personality-prediction-model.git
cd personality-prediction-model
