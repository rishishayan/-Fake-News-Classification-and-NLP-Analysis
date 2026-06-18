# -Fake-News-Classification-and-NLP-Analysis
## Overview

This project focuses on analysing and classifying news articles as **Fake News** or **Factual News** using various Natural Language Processing (NLP) techniques and Machine Learning models.

The notebook explores the complete NLP pipeline, including:

- Text preprocessing
- Part-of-Speech (POS) tagging
- Named Entity Recognition (NER)
- Sentiment Analysis
- Topic Modelling (LDA & LSA)
- Feature Engineering using TF-IDF and Bag-of-Words
- Fake News Classification using Machine Learning

---

## Dataset

The dataset contains news articles labelled as:

- **Fake News**
- **Factual News**

Main columns:

| Column | Description |
|----------|------------|
| text | Original news article |
| fake_or_factual | Target label |

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SpaCy
- NLTK
- Gensim
- Scikit-Learn

---

## Project Workflow

### 1. Exploratory Data Analysis (EDA)

- Loaded and inspected the dataset
- Checked data structure and missing values
- Visualised distribution of fake vs factual articles

---

### 2. POS Tagging

Used **SpaCy** to extract:

- Nouns
- Verbs
- Adjectives
- Adverbs
- Other grammatical structures

Purpose:

- Understand language patterns
- Compare linguistic characteristics between fake and factual news

---

### 3. Named Entity Recognition (NER)

Identified entities such as:

- People
- Organizations
- Countries
- Locations
- Political figures

Purpose:

- Analyse how entities are used across different news categories

---

### 4. Text Preprocessing

Performed:

- Lowercasing
- Tokenization
- Stopword removal
- Lemmatization
- Text cleaning

Purpose:

- Reduce noise
- Improve model performance

---

### 5. Sentiment Analysis

Applied **VADER Sentiment Analyzer** to calculate sentiment scores.

Generated sentiment categories:

- Positive
- Neutral
- Negative

Analysed sentiment distribution across:

- Fake News
- Factual News

---

### 6. Topic Modeling

#### Latent Dirichlet Allocation (LDA)

Used Gensim LDA to discover hidden topics within fake news articles.

Steps:

- Dictionary creation
- Document-Term Matrix generation
- Topic coherence evaluation
- Topic extraction

---

#### Latent Semantic Analysis (LSA)

Applied:

- TF-IDF Vectorisation
- LSI (Latent Semantic Indexing)

Purpose:

- Identify latent semantic structures
- Compare topic quality with LDA

---

### 7. Feature Engineering

Created numerical representations using:

#### Bag of Words (BoW)

Implemented using:

```python
CountVectorizer()
```

#### TF-IDF

Implemented using:

```python
TfidfModel()
```

Purpose:

- Convert text into machine-readable features

---

### 8. Machine Learning Models

#### Logistic Regression

Used for binary classification of news articles.

Evaluation:

- Accuracy Score
- Precision
- Recall
- F1-Score

---

#### Support Vector Machine (SGDClassifier)

Implemented linear SVM using:

```python
SGDClassifier()
```

Evaluation:

- Accuracy Score
- Classification Report

---

## Model Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Classification Report

---
## Results & Visualizations

### Most Common Entities in Fake News

![Most Common Entities in Fake News](images/Most_common_Entities_in _fake_news.png)

Key Observation:
- Political entities such as Trump, Clinton, Obama, and McCain appear frequently.
- Fake news articles are heavily centred around political topics.

---

### Most Common Entities in Factual News

![Most Common Entities in Factual News](images/Most_common_Entities_in_factual_news.png)

Key Observation:
- Factual news contains more references to organizations and geographical entities.
- Reuters and U.S. are among the most frequently mentioned entities.

---

### Most Common Unigrams After Preprocessing

![Most Common Unigrams](images/Most_common_unigrams.png)

Key Observation:
- Words such as "said", "trump", "state", and "president" dominate the corpus.
- Political content is strongly represented in the dataset.

---

### Overall Sentiment Distribution

![News Sentiment](images/news_sentiment.png)

Key Observation:
- Positive and negative sentiments occur at similar frequencies.
- Neutral sentiment appears less frequently.

---

### Sentiment by News Type

![Sentiment by News Type](images/sentiment_by_news_type.png)

Key Observation:
- Both fake and factual news exhibit similar sentiment patterns.
- Sentiment alone is not sufficient to distinguish fake news.

---

### Topic Coherence Analysis

![Topic Coherence](images/coherence_score.png)

Key Observation:
- Topic coherence was evaluated across different numbers of topics.
- The optimal topic count was selected based on the highest coherence score.

## Key NLP Techniques Demonstrated

- Tokenization
- Lemmatization

  ## Learning Outcomes

Through this project, the following NLP concepts were explored:

- Text preprocessing techniques
- Linguistic feature extraction
- Sentiment analysis
- Topic modelling
- Feature engineering
- Supervised machine learning for text classification

This project serves as an NLP workflow for understanding and detecting fake news using Python.

- POS Tagging
- Named Entity Recognition
- Sentiment Analysis
- Topic Modelling
- TF-IDF Vectorisation
- Bag-of-Words Representation
- Text Classification
