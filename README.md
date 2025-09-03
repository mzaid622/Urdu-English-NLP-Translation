# 🎭 Urdu to English Drama Translator (NLP Project)

This project implements a **Machine Translation (MT)** pipeline that translates **Urdu drama dialogues** into **English**.  
It uses the **Facebook M2M100 multilingual model** from Hugging Face Transformers, trained and fine-tuned on a custom dataset collected from Pakistani drama scripts.

---

## 📌 Project Overview
- **Dataset**: Custom parallel corpus with Urdu drama dialogue (`Urdu Transalation`) and English sentences (`Sentence`).
- **Model**: `facebook/m2m100_418M` (Multilingual Machine Translation Model).
- **Frameworks**: PyTorch + Hugging Face Transformers.
- **Metrics**: BLEU and chrF using SacreBLEU.

---

## ✨ Features
- 📂 **Data Collection** – Urdu-English parallel dataset from Pakistani dramas.
- 🧹 **Data Preprocessing** – Handles NaNs, empty strings, and Urdu-specific text cleaning.
- 🔄 **Machine Translation** – Trains M2M100 for Urdu → English.
- 📊 **Evaluation Metrics** – BLEU and chrF scores.
- 💾 **Chunk-Based Training** – Train large datasets in smaller chunks.
- 🔁 **Resume Training** – Continue training from saved checkpoints.

---

## 🛠️ Tech Stack
- **Python** 3.x
- **PyTorch**
- **Hugging Face Transformers**
- **Hugging Face Datasets**
- **SacreBLEU** (for BLEU/chrF)
- **Pandas**
- **Kaggle** (Training Environment)

---

## 📂 Dataset
Your dataset must be a **CSV file** with at least the following columns:
- `Urdu Transalation` → Urdu text (source language)
- `Sentence` → English text (target language)

Example:
| Urdu Transalation           | Sentence             |
|-----------------------------|----------------------|
| یہ ایک کہانی ہے              | This is a story.     |
| میں تم سے محبت کرتا ہوں     | I love you.          |

📌 **Dataset Available on Kaggle**: [Urdu-English Drama Translation Dataset](https://www.kaggle.com/code/mzaid990447)

---

## ⚙️ Installation

```bash
# Install dependencies
pip install torch transformers datasets sacrebleu pandas
