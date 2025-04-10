# Quora-Question-Pairs
Developed a duplicate question detection model using a dataset of 404,290 question pairs, achieving a log loss of 0.344 with XGBoost. The project involved feature engineering with 32 extracted features and evaluation of multiple machine learning models.


This project aims to predict whether two questions are duplicates or not using a dataset of question pairs from Quora. The goal is to develop a robust model that can accurately identify duplicate questions, which is crucial for maintaining data quality and reducing redundancy in question-answering platforms.

Dataset

Total Data Points: 404,290 question pairs.

Class Distribution: The dataset is slightly imbalanced, with 63.08% non-duplicate pairs and 36.92% duplicate pairs.

Feature Engineering

The project involves extensive feature engineering to capture both syntactic and semantic similarities between question pairs. Key features include:

Basic Features:

Question frequency (freq_qid1, freq_qid2)

Length metrics (q1len, q2len, q1_n_words, q2_n_words)

Word overlap features (word_Common, word_share)

Advanced Features:

Token overlaps (cwc_min, ctc_max)

Fuzzy string matching (token_set_ratio, fuzz_ratio)

Longest common substring (longest_substr_ratio)

Weighted Word Vectors:

Integrated spaCy word embeddings with TF-IDF weights to capture semantic meaning.

Modeling and Evaluation

Multiple machine learning models were tested to evaluate their performance on this task:

Random Baseline: A random model was used as a baseline for comparison.

XGBoost: Achieved the best performance with a log loss of 0.344 on the test set.

LightGBM: Also performed well, with a log loss of 0.338 on the test set.

Evaluation metrics included log loss and confusion matrices to assess model performance.

Key Insights

Feature Importance: Word overlap and semantic features significantly improved model performance.

Class Imbalance: Addressed imbalance using stratified sampling during train-test split.

Future Directions
Hyperparameter Tuning: Further optimization of model parameters to enhance performance.

Advanced Embeddings: Exploring BERT or RoBERTa for improved semantic understanding.

DATASET LINK: https://www.kaggle.com/code/akshat4112/quora-question-pair-similarity-part-1-basic-eda/input?select=train.csv.zip
