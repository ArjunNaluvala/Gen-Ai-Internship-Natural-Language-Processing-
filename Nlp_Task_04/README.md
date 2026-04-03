## ⚠️ Note

## If the GitHub preview shows **"Invalid Notebook"** or does not display outputs, please open the notebook using the **Google Colab link below**.

👉 All outputs, results, and visualizations (including the confusion matrix) can be viewed in the notebook in Colab.

## https://colab.research.google.com/drive/1ac_5nTesyS1CJBD1R6mgkpI22bGgId8U

# 🚀 NLP Assignment 4: Fine-Tuning BERT on Kaggle Dataset

## 📌 Project Overview

This project demonstrates the implementation of **BERT (Bidirectional Encoder Representations from Transformers)** for sentiment analysis by fine-tuning a pre-trained model on the **IMDB Movie Reviews dataset**.

The goal is to understand how transformer models work for text classification and evaluate their performance using multiple metrics.


## 🎯 Objective

* Perform text preprocessing on real-world data
* Fine-tune a pre-trained BERT model
* Apply tokenization using Hugging Face Transformers
* Evaluate model performance using standard metrics
* Compare different fine-tuning strategies


## 🛠️ Technologies Used

* Python
* Hugging Face Transformers
* PyTorch
* Scikit-learn
* Pandas, NumPy
* Matplotlib, Seaborn
* Google Colab


## 🔄 Project Pipeline

Raw Data → Data Preprocessing → Data Splitting → Tokenization → Model Building → Fine-Tuning → Evaluation → Analysis


## ⚙️ Implementation Steps

### 🔹 1. Data Preprocessing

* Removed HTML tags, URLs, special characters
* Converted text to lowercase
* Handled missing values

### 🔹 2. Data Splitting

* Train, Validation, Test split
* Stratified sampling for class balance

### 🔹 3. Tokenization

* Used `bert-base-uncased` tokenizer
* Applied padding, truncation, attention masks

### 🔹 4. Model Building

* Loaded pre-trained BERT using `AutoModelForSequenceClassification`
* Configured for binary classification

### 🔹 5. Fine-Tuning

* Optimizer: AdamW
* Learning Rate: 2e-5
* Added Learning Rate Scheduler (Bonus)

### 🔹 6. Model Evaluation

* Accuracy
* Precision
* Recall
* F1 Score
* Confusion Matrix

## 🧪 Experiments Conducted

* Frozen BERT layers
* Fine-tuning last 2 layers
* Full BERT fine-tuning


## 📊 Key Results & Insights

* Full fine-tuning achieved the highest performance
* Transformer models capture contextual meaning effectively
* Learning rate scheduling improved convergence
* Frozen models trained faster but had slightly lower accuracy


## 🧠 Conclusion

The project successfully demonstrates the effectiveness of BERT for sentiment analysis. Fine-tuning pre-trained transformer models significantly improves performance compared to traditional approaches. The experiments highlight the importance of model adaptation strategies in NLP tasks.


## 📌 Future Improvements

* Implement DistilBERT / RoBERTa
* Add early stopping
* Use advanced hyperparameter tuning


## ⭐ Acknowledgment

This project was completed as part of an NLP assignment to gain hands-on experience with transformer models and real-world datasets.
