# Persian Sentiment Analysis — Snappfood Reviews

Binary sentiment classification (happy / sad) of ~70k Persian food-delivery reviews.

**Data:** [Snappfood Persian Sentiment Analysis](https://www.kaggle.com/datasets/soheiltehranipour/snappfood-persian-sentiment-analysis) on Kaggle (downloaded with `kagglehub`; not included in this repo).

## Method
1. Persian text normalization, tokenization, stop-word removal and lemmatization with [hazm](https://github.com/roshan-research/hazm)
2. Two feature types: Bag-of-Words and TF-IDF
3. Three classifiers: Logistic Regression, Linear SVM, Multinomial Naive Bayes
4. Hyperparameter `C` tuned on a validation set, final score on a held-out test set

## Results

| Features | Model | Accuracy | Macro-F1 |
| :-- | :-- | :-: | :-: |
| TF-IDF | Logistic Regression | 0.818 | 0.818 |
| Bag-of-Words | Logistic Regression | 0.811 | 0.811 |
| Bag-of-Words | Naive Bayes | 0.807 | 0.807 |
| TF-IDF | Linear SVM | 0.807 | 0.807 |

Best model (TF-IDF + Logistic Regression, `C=1`) on the **test set: 81.95% accuracy, macro-F1 0.819**.

Notebook: [`snappfood_sentiment.ipynb`](snappfood_sentiment.ipynb)
