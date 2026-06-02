# 📧 Anti-Spam Filter for University

> End-to-end NLP pipeline combining email classification, topic modeling, semantic analysis, and named entity recognition.

---

## 📌 Overview

This project goes beyond simple spam detection: it builds a **complete NLP pipeline** that classifies emails as SPAM or NOT SPAM, then performs **deep analysis** on the corpus — extracting topics, measuring semantic distances, and identifying organizations mentioned in legitimate emails.

---

## 🎯 Objectives

1. **Classify** emails as SPAM / NOT SPAM (binary classification)
2. **Analyze** SPAM emails to extract:
   - Main topics (LDA Topic Modeling)
   - Semantic distance between topics (word vectors)
3. **Extract** organizations mentioned in NOT SPAM emails (NER)

---

## 🏗️ Pipeline

```
Raw Emails
     │
     ▼
Text Preprocessing (cleaning, tokenization, lemmatization)
     │
     ├──────────────────────────────────┐
     ▼                                  ▼
Classification                    Topic Modeling (SPAM)
(TF-IDF + Naive Bayes)            (LDA via gensim)
     │                                  │
     ▼                                  ▼
SPAM / NOT SPAM              Topics + Semantic Distance
                                   (pyLDAvis)
                             Named Entity Recognition
                             (NOT SPAM → Organizations)
                                   (spaCy NER)
```

---

## 📁 Dataset

🔗 [Dataset (ProfessionAI NLP)](https://raw.githubusercontent.com/ProfAI/natural-language-processing/refs/heads/main/datasets/Verifica%20Finale%20-%20Spam%20Detection/)

Collection of university emails, labeled as spam or legitimate.

---

## 🛠️ Tech Stack

| Area | Tools |
|---|---|
| Text Classification | `scikit-learn` (TF-IDF + Naive Bayes) |
| Topic Modeling | `gensim` (LDA), `pyLDAvis` |
| NER | `spaCy` |
| Semantic Analysis | `scipy` (distance metrics) |
| Text Preprocessing | `nltk` |
| Deep Learning | `tensorflow` |
| Visualization | `matplotlib`, `seaborn`, `wordcloud` |
| Data | `numpy`, `pandas` |

---

## 📊 Approach

### 1. Text Preprocessing
- Lowercasing, punctuation & stopword removal
- Tokenization and lemmatization (NLTK)
- TF-IDF vectorization

### 2. Classification
- **Naive Bayes** classifier on TF-IDF features
- Metrics: Accuracy, Precision, Recall, F1-score

### 3. Topic Modeling on SPAM (LDA)
- Latent Dirichlet Allocation via gensim
- Interactive visualization with **pyLDAvis**
- Semantic distance between topics (cosine similarity)

### 4. Named Entity Recognition on NOT SPAM
- spaCy NER pipeline
- Extraction and ranking of **ORG** entities
- Analysis of most mentioned organizations

---

## 📝 Notes

Developed as part of the **Master in Data Science @ ProfessionAI** (2025–2026).  
This project showcases a multi-technique NLP approach — combining classical ML, probabilistic topic modeling, and neural NER in a single coherent pipeline.

---

## 📫 Author

**Nicolò Discotto** · [LinkedIn](https://www.linkedin.com/in/nicolo-discotto/) · [GitHub](https://github.com/NicoloDiscotto)
