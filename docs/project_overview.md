# Project Overview

## More Cleaning or More Data?

### Rethinking the Value of Text Preprocessing Across Training Data Scales

---

## 1. Overview

This project investigates the relationship between **text preprocessing**, **training-data scale**, and **sentiment classification performance**.

In Natural Language Processing, preprocessing is often treated as an important step before model training. Operations such as stopword removal and lemmatization are commonly assumed to improve the quality of textual data.

However, the benefit of additional preprocessing may depend on factors such as:

- Dataset characteristics
- Amount of training data
- Machine-learning model
- Type of preprocessing applied

This research explores these factors experimentally rather than assuming that more preprocessing always leads to better performance.

---

## 2. Research Problem

A common NLP workflow applies several preprocessing techniques before converting text into numerical features.

While this can reduce noise and vocabulary size, preprocessing can also remove information that may be useful for classification.

At the same time, increasing the amount of training data can provide models with more examples from which to learn.

This leads to the central question:

> **As the amount of training data increases, does additional text preprocessing continue to provide a meaningful performance advantage?**

---

## 3. Research Objectives

The main objectives of the project are:

1. Compare different text preprocessing strategies for sentiment classification.
2. Study model performance at different training-data scales.
3. Compare multiple traditional machine-learning classifiers.
4. Examine whether preprocessing effectiveness depends on the dataset.
5. Analyze the interaction between preprocessing, model selection, and training-data scale.
6. Identify situations where additional preprocessing may or may not be beneficial.

---

## 4. Datasets

The research uses publicly available sentiment-analysis datasets.

### IMDb Movie Reviews

The IMDb dataset contains movie-review text associated with positive and negative sentiment labels.

### Twitter Sentiment Data

The Twitter dataset contains short text samples associated with sentiment labels.

The datasets provide different textual characteristics, allowing preprocessing strategies to be examined across more than one type of sentiment data.

> Exact sampling procedures and experimental configurations are intentionally omitted from this public repository while the manuscript is under preparation.

---

## 5. Preprocessing Strategies

The study considers multiple levels of text preprocessing.

### Baseline Normalization

Text is minimally normalized while retaining most of the original information.

### Stopword Removal

Common stopwords are removed before feature extraction.

### Lemmatization

Words are transformed toward their base or dictionary form.

### Combined Preprocessing

Stopword removal and lemmatization are applied together.

The purpose is not to assume that one strategy is universally better, but to empirically compare their behavior under different training conditions.

---

## 6. Feature Representation

The project uses **Term Frequency–Inverse Document Frequency (TF-IDF)** to transform textual documents into numerical representations.

The representation considers:

- Unigrams
- Bigrams

TF-IDF provides a sparse numerical representation suitable for traditional machine-learning classifiers.

---

## 7. Machine-Learning Models

The study evaluates three traditional classifiers.

### Logistic Regression

A linear classification model used for binary sentiment classification.

### Multinomial Naive Bayes

A probabilistic model commonly applied to text classification problems.

### Linear Support Vector Machine

A linear maximum-margin classifier that is well suited to high-dimensional sparse text representations.

---

## 8. Training-Data Scale

A major part of the research is the comparison of model performance across different amounts of available training data.

Instead of evaluating preprocessing at only one dataset size, the study examines multiple training-data scales.

This allows the research to investigate whether the relative usefulness of preprocessing changes as more training examples become available.

---

## 9. Evaluation

The primary evaluation metrics are:

### Accuracy

Measures the proportion of correctly classified samples.

### F1-score

Provides a balance between precision and recall and is useful for evaluating classification performance beyond raw accuracy.

The results are compared across:

```text
Dataset
    ×
Preprocessing Strategy
    ×
Machine-Learning Model
    ×
Training-Data Scale