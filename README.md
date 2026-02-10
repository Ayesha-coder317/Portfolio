# NLP_portfolio_project

Project Overview

This project implements an end-to-end Natural Language Processing (NLP) pipeline to classify SMS messages as spam or ham (legitimate).

The goal is to help telecom operators automatically identify spam messages in order to reduce fraud risk and improve customer experience. The project explores and compares different text preprocessing techniques, feature representations, and machine learning models, with a focus on understanding trade-offs between:

Generative vs. discriminative classifiers
Sparse vs. dense text representations

Dataset Description

Dataset: SMS Spam Collection

Source: UCI Machine Learning Repository

Total messages: ~5,500 SMS messages

Classes:

Ham (legitimate messages)

Spam (unsolicited or promotional messages)

The dataset reflects real-world class imbalance, with legitimate messages occurring more frequently than spam, making it suitable for practical spam detection scenarios.

Run the Notebook

Open the provided (.ipynb) in Google Colab.

Run all cells sequentially from top to bottom.

The notebook will:

Load and explore the dataset

Preprocess raw text

Generate sparse and dense feature representations

Train multiple classification models

Evaluate and compare model performance

3. Reproducibility

All random operations are seeded.

The preprocessing pipeline and feature extraction steps are modular and reusable.

Results Summary

Several models were evaluated using Accuracy, Precision, Recall, and F1-score on a held-out test set.

Best Performing Model

TF-IDF (uni-grams + bi-grams) with Linear Support Vector Machine (SVM)

Key Observations

Discriminative models (Linear SVM, Logistic Regression) outperformed the generative Naive Bayes classifier when combined with TF-IDF features.

Sparse TF-IDF representations were more effective than averaged Word2Vec embeddings for short SMS text.

Including bi-grams improved performance by capturing common spam phrases such as “call now” and “free entry”.

The final model demonstrated strong performance and is well-suited for real-world SMS spam filtering applications.

Technologies Used

Python

pandas, NumPy

scikit-learn

NLTK

Gensim

Matplotlib, Seaborn
