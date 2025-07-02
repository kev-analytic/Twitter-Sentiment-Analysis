# Tweet Sentiment Classification

## 1. Business Problem

Social media platforms, especially Twitter, serve as real-time indicators of public opinion. Organizations, marketers, and policymakers can gain valuable insights by analyzing sentiment in tweets. The goal of this project is to classify tweets into four sentiment categories:

- **Positive**
- **Negative**
- **Neutral**
- **Irrelevant**

Accurate classification enables better decision-making in areas such as customer feedback analysis, brand monitoring, and public sentiment tracking.

---

## 2. Dataset Description

The dataset consists of raw tweets, each labeled as one of the four sentiment classes.
Preprocessing is essential due to the noisy and informal nature of tweet content (e.g., slang, emojis, hashtags, links).

---

## 3. Steps Taken

### Text Preprocessing:
- Joined tokenized lemmas into clean strings
- Removed unwanted characters and applied lowercasing
- Removed stopwords using `TfidfVectorizer` with built-in English stopword removal

### Feature Engineering:
- Converted processed text into TF-IDF features


### Modeling:
- Split the data into training and validation sets
- Fit the `TfidfVectorizer` only on the training data to prevent data leakage
- Trained a **Random Forest Classifier** on the final feature matrix
- Evaluated performance using accuracy and AUC score

---

## 4. Results

The model achieved the following performance on the validation set:

- ✅ **Accuracy:** 95%
- ✅ **AUC (macro average):** 0.99

These results indicate that the model is both accurate and generalizes well across all four sentiment classes.

---

## 5. Conclusion

This tweet classification pipeline demonstrates that combining effective preprocessing with a robust ensemble model like Random Forest yields high-performance sentiment prediction. The current approach is efficient, scalable, and avoids common pitfalls like data leakage or memory errors by using sparse matrix operations.

This solution is well-suited for production environments where sentiment analysis from real-time social media streams is essential.

---

## Dependencies

- Python 3.7+
- `pandas`
- `scikit-learn`
- `nltk`





