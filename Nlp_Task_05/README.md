⚠️ Note

If the GitHub preview shows "Invalid Notebook" or does not display outputs, please open the notebook using the Google Colab link below.

👉 All outputs, results, and predictions can be viewed in the notebook in Colab.

🔗 https://colab.research.google.com/drive/1Fq5zouoIYjfqGAG-lsH1WaokMcOccA-J

🚀 NLP Assignment 5: Fine-Tuning BERT for POS Tagging & Chunking

📌 Project Overview

This project demonstrates the implementation of BERT (Bidirectional Encoder Representations from Transformers) for Token Classification, specifically for Part-of-Speech (POS) Tagging.

The goal is to understand how transformer models perform sequence labeling tasks, where each word in a sentence is assigned a grammatical label.

Additionally, the project provides a conceptual understanding of Chunking (Phrase Detection).

🎯 Objective

Perform token classification using transformer models
Fine-tune a pre-trained BERT model for POS tagging
Handle tokenization and label alignment challenges
Evaluate sequence labeling performance using appropriate metrics
Perform inference on custom sentences

🛠️ Technologies Used

Python

Hugging Face Transformers

PyTorch

SeqEval (Evaluation Metric)

📂 Dataset Used

Universal Dependencies

Task: POS Tagging

🏷️ Sample Labels:

NOUN, VERB, ADJ, ADV, PRON, DET, ADP, PROPN, PUNCT

🔄 Project Pipeline

Raw Data → Tokenization → Label Alignment → Model Setup → Training → Evaluation → Inference

⚙️ Implementation Steps

🔹 1. Data Loading
Loaded dataset in .conllu format
Extracted tokens and corresponding POS tags

🔹 2. Data Preprocessing
Structured tokens and labels
Limited dataset size for faster training
Created label mappings (label2id, id2label)

🔹 3. Tokenization
Used bert-base-uncased tokenizer
Applied:
Padding
Truncation
Attention masks

🔹 4. Label Alignment (Important Step)
Handled subword tokenization
Assigned -100 to special tokens
Ensured correct mapping between tokens and labels

🔹 5. Model Setup
Loaded BERT using AutoModelForTokenClassification
Configured with correct number of labels

🔹 6. Training
Trainer API used
Learning Rate: 2e-5
Epochs: 3
Batch Size: 16
Weight Decay applied

🔹 7. Model Evaluation
Precision
Recall
F1 Score
Accuracy
(using SeqEval metric)

🔹 8. Inference
Tested model on custom sentences
Generated POS tags for each token

🔍 Inference Example
Input:

John works at Google in California

Output:

John → PROPN
works → VERB
at → ADP
Google → PROPN
in → ADP
California → PROPN

🔄 POS Tagging vs Chunking

Feature	POS Tagging	Chunking
Level	Word-level	Phrase-level
Output	Grammar tags	Phrase groups
Example	NOUN, VERB	NP, VP
Difficulty	Easy	Medium

🧪 Observations

BERT effectively captures contextual relationships between words

Label alignment plays a crucial role in model performance

Even with limited data, the model produces good results

Transformer models outperform traditional NLP techniques

⚠️ Challenges Faced

Handling subword tokenization

Aligning labels correctly with tokens

Managing special tokens (-100)

Understanding sequence evaluation metrics

Training time and resource constraints

📊 Key Results & Insights

Fine-tuned BERT achieved strong performance on POS tagging

Context-aware embeddings improved prediction quality

Proper preprocessing significantly impacts accuracy

SeqEval provided reliable evaluation for sequence tasks

🧠 Conclusion

This project demonstrates the effectiveness of BERT for token classification tasks such as POS tagging. The model successfully learns contextual dependencies between words and produces accurate grammatical labels.

The assignment also highlights the importance of preprocessing, especially label alignment, in achieving good performance in sequence labeling tasks.

📌 Future Improvements

Implement Chunking using CoNLL dataset

Try DistilBERT for faster performance

Apply hyperparameter tuning

Increase dataset size for better accuracy
