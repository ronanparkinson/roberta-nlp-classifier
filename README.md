# 🤖 RoBERTa NLP Text Classification (Human vs AI)

## 🧠 Overview

This project fine-tunes a pre-trained RoBERTa model to classify whether text is human-written or machine-generated.

The model is trained on the SemEval 2024 Task 8 dataset using transfer learning via Hugging Face.

---

## 🎯 Problem

Detect whether a piece of text is:
- Human-written (0)
- Machine-generated (1)

---

## ⚙️ Approach

- Used **RoBERTa-base** with Hugging Face
- Tokenized text with max length of 128
- Applied batch size of 32 for efficient training
- Used AdamW optimizer with learning rate 2e-5
- Loss: Sparse categorical crossentropy

---

## 📊 Results

- Training Accuracy: **97.5%**
- Validation Accuracy: **~70%**
- F1 Score: **0.33**

Model outperformed baseline (~64%) but showed signs of **overfitting and class bias**

---

## ⚠️ Limitations

- Overfitting due to lack of early stopping
- Class imbalance affecting F1 score
- Bias toward dominant class

---

## 🔮 Improvements

- Add early stopping
- Apply class weighting
- Improve dataset balance

---

## 🛠️ Tech Stack

- Python
- TensorFlow
- Hugging Face Transformers
- NumPy / Pandas

---

## ▶️ How to Run

```bash
pip install -r requirements.txt
