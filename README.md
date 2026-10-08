<div align="center">

<img src="assets/project-logo.png" alt="More Cleaning or More Data?" width="420"/>

# More Cleaning or More Data?

### Rethinking the Value of Text Preprocessing Across Training Data Scales

**Punith Dewangan¹ · Mir Shaad Ali¹**

¹ Department of Artificial Intelligence and Data Science  
**Global Academy of Technology, Bengaluru, India**

<br>

**Research Project · Manuscript in Preparation**

<br>

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![NLP](https://img.shields.io/badge/NLP-Text%20Processing-8E44AD?style=for-the-badge)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![TF-IDF](https://img.shields.io/badge/TF--IDF-Feature%20Extraction-16A085?style=for-the-badge)
![Research](https://img.shields.io/badge/Research-Manuscript%20in%20Preparation-3498DB?style=for-the-badge)

</div>

---

## 🧠 About

Text preprocessing is a common step in Natural Language Processing (NLP).

Techniques such as stopword removal and lemmatization are often applied before training a machine-learning model. However, additional preprocessing does not necessarily provide the same benefit across every dataset, model, or training-data size.

This research investigates the relationship between:

- 🧹 **Text preprocessing**
- 📊 **Training-data scale**
- 🤖 **Machine-learning models**
- 📝 **Sentiment classification**
- 📈 **Model performance**

The central idea is:

> **When more training data is available, does additional text cleaning still provide a meaningful advantage?**

---

## 🔬 Research Questions

The study investigates:

1. Does text preprocessing consistently improve sentiment classification?
2. Does the usefulness of preprocessing change as training data increases?
3. Do different machine-learning models respond differently to preprocessing?
4. Are preprocessing effects consistent across different datasets?
5. When is additional cleaning useful compared with simply providing more training data?

---

## 📚 Datasets

The research uses publicly available sentiment-analysis datasets.

### 🎬 IMDb Movie Reviews

A movie-review sentiment dataset containing text samples associated with positive and negative sentiment labels.

### 🐦 Twitter Sentiment Data

A sentiment-analysis dataset containing text samples labelled according to sentiment.

> Detailed sampling procedures and unpublished experimental configurations are intentionally not included in this public repository at the current research stage.

---

## 🧹 Text Preprocessing

The research compares multiple levels of text preprocessing.

| Strategy | Description |
|---|---|
| **Baseline Normalization** | Minimal text normalization |
| **Stopword Removal** | Removal of common stopwords |
| **Lemmatization** | Conversion of words toward their base forms |
| **Combined Preprocessing** | Stopword removal + lemmatization |

The objective is to experimentally compare preprocessing strategies rather than assume that more cleaning is always better.

---

## 🔢 Feature Extraction

The project uses **TF-IDF (Term Frequency–Inverse Document Frequency)** to convert textual documents into numerical feature representations.

The research considers:

- Unigrams
- Bigrams

The resulting sparse representations are used as input to traditional machine-learning classifiers.

---

## 🤖 Machine Learning Models

The study evaluates three traditional machine-learning classifiers.

### Logistic Regression

A linear classification model used for sentiment classification.

### Multinomial Naive Bayes

A probabilistic classifier commonly used for text classification.

### Linear Support Vector Machine

A linear maximum-margin classifier suitable for high-dimensional sparse text representations.

---

## 📊 Training-Data Scale

A key part of the research is studying model performance across different amounts of available training data.

Rather than evaluating preprocessing at only one dataset size, multiple training-data scales are considered.

This allows the study to examine whether the relative usefulness of preprocessing changes as more training examples become available.

---

## 📈 Evaluation

The primary evaluation metrics are:

- **Accuracy**
- **F1-score**

Performance is compared across combinations of:

```text
Dataset
    ×
Preprocessing Strategy
    ×
Machine Learning Model
    ×
Training-Data Scale