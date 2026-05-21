# 🍽️ Restaurant Sentiment Analysis

Classifying customer sentiment from restaurant reviews using NLP and machine learning — helping food delivery platforms understand which restaurants are thriving and which need attention.

---

## 📌 Problem Statement

Food delivery apps host thousands of restaurants, but manually reading reviews at scale is impossible. This project answers:

> *How can we automatically classify customer sentiment and use it to improve restaurant recommendations and quality control?*

**Business impact:** Sentiment scores can be used to rank restaurants, flag low performers, and personalize recommendations for new users.

---

## 📊 Dataset

- **Source:** Kaggle
- **Size:** Reviews from ~10,000 restaurants across India
- **Features:** Restaurant name, reviewer name, review text, rating, metadata
- **Label distribution:** ~73% positive reviews (class imbalance noted)

---

## 🔧 Methodology

### 1. Data Preprocessing
- Removed stopwords, punctuation, and noise using NLTK
- Applied tokenization, stemming (PorterStemmer), and lemmatization (WordNetLemmatizer)
- Sentiment labels assigned using VADER (SentimentIntensityAnalyzer)

### 2. Feature Engineering
- Text vectorized using **TF-IDF** (Term Frequency–Inverse Document Frequency)

### 3. Models Trained

| Model | Accuracy |
|---|---|
| ✅ Logistic Regression | **88.86%** |
| Support Vector Machine (SVM) | 88.11% |
| Random Forest | 85.50% |
| Naive Bayes | 74.21% |

**Winner: Logistic Regression** with ~89% accuracy.

---

## 🛠️ Tech Stack

`Python` `NLTK` `scikit-learn` `Pandas` `NumPy` `Matplotlib` `Seaborn`

---

## 📁 Project Structure

```
SENTIMENT-ANALYSIS/
│
└── Sentiment Analysis.ipynb   # Full pipeline: EDA → preprocessing → modelling → evaluation
```

---

## 💡 Key Takeaways

- Logistic Regression outperformed ensemble and probabilistic models on this dataset
- Class imbalance (73% positive reviews) is a known limitation and a candidate for future improvement using oversampling (SMOTE) or class weighting
- VADER worked well for assigning sentiment labels without manual annotation

---

## 🚀 Future Improvements

- [ ] Handle class imbalance with SMOTE or class weights
- [ ] Try transformer-based models (BERT) for improved accuracy
- [ ] Deploy as a simple API endpoint for real-time review classification

---

## 👤 Author

**Navnee Sharma** — [LinkedIn](https://linkedin.com/in/navneesharma) | [navnee.sharma30@gmail.com](mailto:navnee.sharma30@gmail.com)
