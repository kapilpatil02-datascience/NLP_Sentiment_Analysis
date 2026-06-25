# NLP_Sentiment_Analysis_Project

this is work on kernel base(python 3.13.5)

This repository contains an NLP sentiment analysis project with code, data, and model files.

## Contents
- `nlp.ipynb`: notebook for exploration and modeling
- `api.py`, `app.py`: application code
- `requirements.txt`: Python dependencies
- `sentiment_model.pkl`, `tfidf_vectorizer.pkl`: trained model artifacts
- `cleaned_reviews1.csv`, `NLP Material/cleaned_reviews.csv`: dataset files


# 📝 NLP Sentiment Analysis on Customer Product Reviews

## 📌 Project Overview

This project focuses on **Sentiment Analysis** using **Natural Language Processing (NLP)** and **Machine Learning** to automatically classify customer product reviews into **Positive, Neutral, and Negative** sentiments.

The objective is to help businesses analyze customer feedback at scale, understand customer satisfaction, identify product issues, and support data-driven decision-making.

---

# 🎯 Business Problem

Organizations receive thousands of customer reviews every day. Manually reading and categorizing these reviews is time-consuming and inefficient.

This project automates the sentiment classification process using NLP techniques, allowing businesses to:

* Monitor customer satisfaction
* Identify recurring complaints
* Understand customer opinions
* Improve products based on customer feedback

---

# 📊 Dataset

The dataset contains customer product reviews with the following columns:

* Title
* Rating
* Review Body

The **Title** and **Review Body** were combined into a single review text for sentiment analysis.

Target Classes:

* Positive
* Neutral
* Negative

---

# 🔍 Exploratory Data Analysis (EDA)

Performed comprehensive exploratory data analysis including:

* Missing value analysis
* Duplicate record detection
* Review length distribution
* Rating distribution
* Word frequency analysis
* Positive vs Negative review comparison
* Correlation analysis
* Word Cloud visualization
* Review statistics

---

# 🧹 Text Preprocessing

To improve model performance, the following preprocessing steps were applied:

* Convert text to lowercase
* Remove URLs
* Remove emojis
* Remove punctuation
* Remove numbers
* Remove extra spaces
* Remove stopwords
* Lemmatization
* Handle multilingual reviews by translating non-English text into English
* Preserve important negation words such as:

  * not
  * no
  * never

---

# ⚙️ Feature Engineering

Created additional text-based features:

* Text Length
* Word Count
* Average Word Length
* Negation Count
* Sentence Count

Text was converted into numerical features using:

* TF-IDF Vectorization

---

# 🤖 Machine Learning Models

The following classification models were trained and evaluated:

* Logistic Regression
* Naive Bayes
* Support Vector Machine (SVM)
* LinearSVC
* Random Forest
* Gradient Boosting

---

# ⚡ Hyperparameter Tuning

Hyperparameter tuning was performed using **GridSearchCV** for LinearSVC.

Best Parameters:

* C = 1
* class_weight = balanced
* loss = hinge
* max_iter = 3000

---

# 📈 Model Evaluation

Evaluation metrics used:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix
* Classification Report

Final model comparison showed that SVM achieved the highest overall accuracy, while Logistic Regression with balanced class weights provided the most balanced performance across all sentiment classes.

---

# 🌐 Deployment

The selected model was deployed using **Streamlit**, allowing users to:

* Enter customer reviews
* Perform real-time sentiment prediction
* Display predicted sentiment
* Analyze customer feedback instantly

---

# 🛠️ Technologies Used

### Programming Language

* Python

### Libraries

* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* NLTK
* WordCloud
* Streamlit
* Pickle

---

# 📁 Project Structure

```
NLP-Sentiment-Analysis/
│
├── data/
│   └── reviews.csv
│
├── notebooks/
│   └── NLP_Sentiment_Analysis.ipynb
│
├── models/
│   ├── sentiment_model.pkl
│   └── tfidf_vectorizer.pkl
│
├── app.py
├── requirements.txt
├── README.md
└── assets/
```

---

# 🚀 How to Run the Project

### Clone Repository

```bash
git clone https://github.com/yourusername/NLP-Sentiment-Analysis.git
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Launch Streamlit

```bash
streamlit run app.py
```

---

# 📊 Results

Model Comparison:

| Model                    | Accuracy |
| ------------------------ | -------- |
| Logistic Regression      | ~79%     |
| Naive Bayes              | ~70%     |
| SVM                      | ~81%     |
| LinearSVC + GridSearchCV | ~80%     |
| Random Forest            | ~78%     |
| Gradient Boosting        | ~77%     |

---

# 🚧 Challenges Faced

During the project several real-world NLP challenges were encountered:

* Cleaning noisy customer reviews
* Handling punctuation without merging words
* Processing multilingual reviews
* Managing class imbalance
* Detecting neutral sentiment
* Understanding negation phrases
* Handling mixed-sentiment reviews
* Evaluating multiple machine learning models

These challenges highlighted the importance of effective preprocessing and model evaluation.

---

# 🔮 Future Improvements

Potential improvements include:

* Fine-tuning transformer models (BERT / DistilBERT)
* Better handling of sarcasm and contextual language
* Expanding the dataset
* Aspect-based sentiment analysis
* Explainable AI techniques for prediction interpretation

---

# 📌 Key Learnings

* Text preprocessing significantly impacts model performance.
* TF-IDF is an effective baseline for traditional NLP tasks.
* Model evaluation should consider Precision, Recall, F1-score, and Confusion Matrix—not just Accuracy.
* Class imbalance affects minority class prediction.
* Deploying models with Streamlit transforms machine learning projects into interactive applications.

---

# 👨‍💻 Author

**Kapil Patil**

Aspiring Data Scientist | Machine Learning | Natural Language Processing

If you found this project interesting, feel free to ⭐ the repository and connect with me on LinkedIn.
