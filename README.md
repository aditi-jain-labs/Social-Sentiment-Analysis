# Social-Sentiment-Analysis: NLP-Based Tweet Sentiment Analysis

TweetSense is a Natural Language Processing (NLP) project that explores multiple machine learning, deep learning, and lexicon-based approaches for classifying tweets as **Positive, Neutral, or Negative**.

The project compares several sentiment classification techniques and develops an ensemble model combining **Support Vector Classification (SVC), Logistic Regression, and VADER** to achieve more balanced sentiment predictions.

---

## Overview

Social media platforms generate enormous volumes of unstructured text containing opinions, reactions, and emotions.

Automatically identifying sentiment within this data can help uncover patterns in public opinion and understand how people respond to topics, products, events, and services.

This project builds an end-to-end NLP pipeline for tweet sentiment classification, covering:

- Data exploration
- Text preprocessing
- Feature extraction
- Machine learning
- Deep learning
- Lexicon-based sentiment analysis
- Hyperparameter tuning
- Model evaluation
- Ensemble learning

---

## Objective

The goal is to classify tweets into three sentiment categories:

| Sentiment | Description |
|-----------|-------------|
| Positive | Expresses positive sentiment |
| Neutral | Does not strongly express positive or negative sentiment |
| Negative | Expresses negative sentiment |

In addition to achieving good overall accuracy, the project focuses on obtaining balanced performance across the three sentiment classes.

---

## Project Workflow

The project follows an end-to-end NLP and machine learning workflow:

1. **Data Exploration**
   - Inspect the dataset
   - Analyse sentiment distribution
   - Identify characteristics of the textual data

2. **Text Preprocessing**
   - Clean and prepare tweet text
   - Transform unstructured text into a form suitable for modelling

3. **Feature Engineering**
   - Convert textual data into numerical representations
   - Use TF-IDF-based features for traditional machine learning models

4. **Model Development**
   - Train and compare multiple classification approaches

5. **Hyperparameter Tuning**
   - Optimise selected machine learning models

6. **Model Evaluation**
   - Compare accuracy, precision, recall and F1-score
   - Examine performance across individual sentiment classes

7. **Ensemble Learning**
   - Combine selected models using majority voting

---

## Models Explored

The project investigates multiple approaches to sentiment classification.

### Machine Learning

- Support Vector Classifier (SVC)
- Logistic Regression
- Random Forest
- Naive Bayes

### Deep Learning

A **Convolutional Neural Network (CNN)** was explored as a deep-learning approach to text classification.

### Lexicon-Based NLP

**VADER (Valence Aware Dictionary and sEntiment Reasoner)** was used as a rule and lexicon-based sentiment analysis approach.

### Ensemble Model

The final approach combines:

**SVC + Logistic Regression + VADER**

Each model independently predicts the sentiment of a tweet. The final sentiment is determined using **majority voting (mode)** across their predictions.

---

## Model Evaluation

Models were evaluated using multiple metrics rather than relying only on overall accuracy.

Evaluation included:

- Accuracy
- Precision
- Recall
- F1-score
- Classification reports
- Precision-Recall curves
- Area Under the Precision-Recall Curve (AUPRC)

This makes it possible to examine not only overall predictive performance but also how well each model handles individual sentiment classes.

---

## Results

The final ensemble model achieved approximately:

### **81% Test Accuracy**

The ensemble combined predictions from:

- Support Vector Classifier
- Logistic Regression
- VADER

The experiments also highlighted an important machine-learning consideration:

> **Overall accuracy alone does not provide a complete picture of model performance.**

Performance across individual sentiment classes should also be considered, particularly when the class distribution or classification difficulty varies between categories.

The ensemble approach provided a more balanced result across **positive, neutral, and negative sentiment** compared with several of the individual approaches explored during the project.

---

## Tech Stack

### Programming & Data

- Python
- Pandas
- NumPy

### Machine Learning

- Scikit-learn
- TF-IDF
- Support Vector Machines
- Logistic Regression
- Random Forest
- Naive Bayes
- Ensemble Learning

### Deep Learning

- TensorFlow
- Keras
- Convolutional Neural Networks

### NLP

- NLTK
- VADER Sentiment Analysis

### Visualisation

- Matplotlib
- Seaborn

### Development Environment

- Jupyter Notebook
- Google Colab

---

## Repository Structure

```text
TweetSense/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── notebooks/
│   └── tweet_sentiment_analysis.ipynb
│
└── data/
    └── README.md


Getting Started
1. Clone the repository
git clone <your-repository-url>
cd TweetSense
2. Create a virtual environment
python -m venv venv

Activate it on macOS/Linux:

source venv/bin/activate

On Windows:

venv\Scripts\activate
3. Install dependencies
pip install -r requirements.txt
4. Launch Jupyter Notebook
jupyter notebook

Open:

notebooks/tweet_sentiment_analysis.ipynb

The notebook can also be run using Google Colab.

Key Skills Demonstrated

This project demonstrates practical experience in:

Natural Language Processing
Exploratory Data Analysis
Text preprocessing
Feature engineering
TF-IDF vectorisation
Machine learning classification
Hyperparameter optimisation
Deep learning
Sentiment analysis
Model evaluation
Precision/Recall analysis
Ensemble learning
Python-based data analysis
Key Takeaways

A major takeaway from the project was that selecting a model based purely on accuracy can hide weaknesses in individual classes.

Comparing precision, recall and F1-score alongside overall accuracy provided a better understanding of model behaviour.

The project also demonstrates how different NLP approaches can complement one another. Rather than relying entirely on a single model, the final solution combines traditional machine learning with lexicon-based sentiment analysis through ensemble learning.

Future Improvements

Several extensions could further develop TweetSense:

Experiment with transformer-based models such as BERT
Explore alternative text representations and embeddings
Improve handling of class imbalance
Perform more extensive cross-validation
Automate hyperparameter optimisation
Develop a reusable prediction pipeline
Expose the trained model through a REST API
Build an interactive sentiment analysis dashboard
Extend the system to analyse new social-media text
# Author

## Aditi Jain

Interested in building at the intersection of data, artificial intelligence, machine learning, analytics, research, and software engineering.
