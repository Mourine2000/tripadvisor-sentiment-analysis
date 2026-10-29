# Comparative NLP Sentiment Analysis: TF-IDF vs. Fine-Tuned DistilBERT

> **Author:** Mourine Lagat  
> **Date:** October 2026  

---

## 📌 Project Overview
This repository contains the code, documentation, and presentation assets for a comparative Natural Language Processing (NLP) study evaluating sentiment classification performance on TripAdvisor travel reviews. 

The project investigates whether transitioning from a traditional bag-of-words baseline (**TF-IDF + Logistic Regression**) to a modern deep learning architecture (**Fine-Tuned DistilBERT Transformer**) yields significant performance gains, particularly when handling complex linguistic nuances such as neutral/ambiguous sentiment.

---

## 🚀 Key Results & Performance
Both models were rigorously evaluated on an independent, unseen validation/holdout dataset containing 1,600 reviews across three sentiment classes (Negative, Neutral, Positive):

| Model Architecture | Negative (0) F1 | Neutral (1) F1 | Positive (2) F1 | Overall Accuracy |
| :--- | :---: | :---: | :---: | :---: |
| **TF-IDF + Logistic Regression (Baseline)** | 0.82 | 0.55 | 0.84 | **81%** |
| **Fine-Tuned DistilBERT (Transformer)** | **0.88** | **0.63** | **0.91** | **84%** |

* **Key Takeaway:** Fine-tuned DistilBERT demonstrated superior generalization, achieving an 84% overall accuracy and showing dramatic improvements in resolving ambiguous neutral (3-star) feedback through self-attention mechanisms.

---

## 🛠️ Tech Stack & Tooling
* **Deep Learning Framework:** Hugging Face Transformers (`AutoModelForSequenceClassification`), Datasets, and Trainer
* **Hardware Acceleration:** PyTorch with Google Colab T4 GPU
* **Baseline Modeling:** Scikit-Learn (`TfidfVectorizer`, `LogisticRegression`)
* **Evaluation Metrics:** Scikit-learn classification reports and confusion matrices
* **Visualization:** Matplotlib & Seaborn

---

## 📂 Repository Structure
```text
├── nlp_sentiment_analysis_presentation.pptx   # Branded editable slide deck
├── notebook.ipynb                             # Google Colab source code & pipeline
└── README.md                                  # Project documentation
