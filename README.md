# 🔍 Quora Question Pairs - Duplicate Detection

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-orange.svg)](https://pandas.pydata.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

An end-to-end Machine Learning and Natural Language Processing (NLP) project aimed at identifying whether a pair of questions asked on Quora are semantic duplicates.

---

## 📌 Table of Contents
- [About the Project](#-about-the-project)
- [Dataset Details](#-dataset-details)
- [Feature Engineering](#-feature-engineering)
- [Exploratory Data Analysis (EDA)](#-exploratory-data-analysis-eda)
- [Tech Stack](#-tech-stack)

---

## 🎯 About the Project
Quora is a popular platform where people ask questions and share answers. Often, users ask questions that mean the exact same thing but are phrased differently. This creates redundancy. 

The goal of this project is to build an intelligent NLP model that predicts whether two given questions (`question1` and `question2`) are duplicates (`1`) or not (`0`).

---

## 📊 Dataset Details
- **Source:** Kaggle (Quora Question Pairs Competition)
- **Total Rows:** 404,290 question pairs
- **Features:**
  - `id`: Row identifier
  - `qid1`, `qid2`: Unique IDs for each question
  - `question1`, `question2`: The actual text strings
  - `is_duplicate`: Target label (`1` if duplicate, `0` otherwise)

---

## 🛠️ Feature Engineering
To extract maximum signal from text data before feeding it to ML models, various advanced and basic features were engineered:
- **Basic Features:** Length of questions (`q1_len`, `q2_len`), word counts (`q1_num_words`, `q2_num_words`).
- **Token-based Features:** Number of common words (`word_common`), word share ratio (`word_share`).
- **Advanced NLP Features:** Stopwords overlap, length differences, and token ratios.

---

## 📈 Exploratory Data Analysis (EDA)
- Analyzed class distribution: Found that roughly **36.6%** of pairs are duplicates and **63.4%** are non-duplicates.
- Studied distribution of character and word lengths using `Seaborn` and `Matplotlib`.
- Checked for missing values and performed necessary text cleaning (lowercasing, punctuation removal).

---

## 💻 Tech Stack
- **Programming Language:** Python 3.x
- **Data Manipulation & Processing:** Pandas, NumPy
- **Data Visualization:** Matplotlib, Seaborn
- **Environment:** Jupyter Notebook / Google Colab

---
