# Customer Sentiment Analysis on Social Media Posts using Machine Learning Models

A machine learning project to classify customer opinions from social media posts (tweets) into **positive, negative, or neutral** sentiments. The project demonstrates a full data analysis and modeling pipeline with multiple machine learning algorithms, structured using the **PDCA (Plan–Do–Check–Act)** Lean continuous improvement cycle.

## Table of Contents
1. [Introduction](#introduction)
2. [Methodology & Quality Framework](#methodology--quality-framework)
3. [Dataset](#dataset)
4. [Models Used](#models-used)
5. [Evaluation Metrics](#evaluation-metrics)
6. [Results](#results)
7. [Tools & Technologies](#tools--technologies)
8. [Conclusion](#conclusion)

---

## Introduction

This project focuses on analyzing customer sentiment from social media posts. The goal is to classify **U.S. airline customer tweets** into positive, negative, or neutral sentiments using machine learning models. The project covers the entire workflow — from data exploration to model evaluation and business insights generation — following a **PDCA Lean cycle** to ensure methodical development and quality assurance at every phase.

---

## Methodology & Quality Framework

This project is structured using the **PDCA (Plan–Do–Check–Act)** Lean continuous improvement cycle, with **5S principles** applied to the model evaluation process to ensure a clean, standardized, and reproducible workflow.

### Plan
- Defined the classification objective: 3-class sentiment prediction (positive / negative / neutral).
- Selected target evaluation metrics: Accuracy, Precision, Recall, and F1-Score.
- Designed the end-to-end pipeline:
  - Text cleaning → Tokenization → Normalization → Feature extraction (TF-IDF / Bag of Words) → Class imbalance handling → Model training → Evaluation
- Selected 5 candidate classifiers covering a range of algorithmic approaches: SVM, KNN, Naive Bayes, Decision Tree, Random Forest.

### Do
- Loaded the `tweets.csv` dataset and performed EDA: basic statistics, missing value identification, and class distribution analysis.
- Executed the full NLP preprocessing pipeline:
  - Removed punctuation, stop words, and special characters
  - Applied tokenization and normalization
  - Extracted numerical features using **TF-IDF / Bag of Words**
  - Applied class imbalance handling strategies to prepare balanced training data
- Trained all 5 classifiers on the processed dataset with a standardized train/test split for fair comparison.

### Check
- Applied **5S principles** to the model evaluation process:

| 5S Step | Application |
|---------|-------------|
| **Sort** | Ranked all 5 models by F1-Score to identify top performers and eliminate underperformers |
| **Set in Order** | Organized results into a structured metrics matrix (Accuracy · Precision · Recall · F1-Score) |
| **Shine** | Cleaned and standardized the evaluation pipeline for reproducibility across all models |
| **Standardize** | Established a unified scoring rubric applied consistently to every classifier |
| **Sustain** | Documented the full workflow in a reproducible Jupyter Notebook for future replication |

- **Random Forest achieved the highest accuracy: 96%**, confirming ensemble learning superiority for text-based sentiment classification.
- Identified that SVM also performed competitively, while KNN and Naive Bayes showed lower recall on minority sentiment classes.

### Act
- Performed **root cause analysis** on lower-performing models to identify preprocessing and feature extraction gaps contributing to misclassifications.
- Determined that class imbalance in the dataset was a primary driver of weaker recall on minority sentiment classes.
- Standardized the Jupyter Notebook pipeline as the reproducible baseline for future extensions.
- Scoped next-cycle improvements: deep learning techniques (LSTM, BERT) and real-time data processing for live sentiment monitoring.

---

## Dataset

| Property | Detail |
|----------|--------|
| **File** | `tweets.csv` |
| **Domain** | U.S. airline customer reviews on social media |
| **Task** | 3-class sentiment classification (Positive / Negative / Neutral) |
| **Key features** | Text content of tweets, sentiment labels |
| **Purpose** | Real-world data to train and evaluate multiple ML classifiers |

---

## Models Used

| Model | Type |
|-------|------|
| Support Vector Machine (SVM) | Margin-based classifier |
| K-Nearest Neighbors (KNN) | Instance-based classifier |
| Naive Bayes | Probabilistic classifier |
| Decision Tree | Rule-based classifier |
| Random Forest ⭐ | Ensemble classifier — best performer (96% accuracy) |

---

## Evaluation Metrics

All models evaluated using a standardized metrics matrix (5S — Standardize phase):

| Metric | Purpose |
|--------|---------|
| **Accuracy** | Overall correct classification rate |
| **Precision** | Reliability of positive predictions |
| **Recall** | Coverage of actual positive cases |
| **F1-Score** | Harmonic mean of Precision and Recall — primary ranking metric |

---

## Results

- Classified U.S. airline customer tweets into 3 sentiment categories using 5 ML models.
- Applied a full NLP preprocessing pipeline: text cleaning, tokenization, TF-IDF/Bag-of-Words feature extraction, and class imbalance handling.
- Evaluated all models using a **5S-standardized metrics matrix** (Accuracy, Precision, Recall, F1-Score).
- **Random Forest achieved the highest accuracy: 96%**, demonstrating the superiority of ensemble learning for text-based classification.
- **Root cause analysis** on lower-performing models identified class imbalance and feature extraction limitations as primary drivers of weaker recall on minority classes.
- Findings confirm the effectiveness of ensemble methods for extracting actionable sentiment insights from social media data.

---

## Tools & Technologies

| Category | Tools |
|----------|-------|
| Programming | Python |
| ML Library | Scikit-learn |
| Data Processing | Pandas, NumPy |
| NLP | NLP preprocessing libraries (tokenization, stop-word removal, TF-IDF) |
| Development | Jupyter Notebook |
| Quality Framework | PDCA (Lean), 5S, Root Cause Analysis |

---

## Conclusion

This project demonstrates a complete, **PDCA-structured workflow** for sentiment analysis on social media posts. Applying Lean quality principles — particularly **5S to the model evaluation process** — ensured a clean, standardized, and reproducible comparison across all classifiers.

- **Random Forest (96% accuracy)** emerged as the optimal model, validated through a rigorous, standardized evaluation pipeline.
- **Root cause analysis** on misclassifications provided actionable guidance for future preprocessing improvements.
- Businesses can leverage this approach to monitor customer satisfaction trends, address operational inefficiencies, and optimize strategies in real time.

**Future work** (Act phase next cycle):
- Explore deep learning models (LSTM, BERT) for improved contextual understanding
- Implement real-time sentiment monitoring on live social media streams
- Extend to multi-domain sentiment datasets beyond airline reviews
