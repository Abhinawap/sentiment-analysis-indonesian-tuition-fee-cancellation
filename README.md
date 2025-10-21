# Sentiment Analysis of Indonesian Tuition Fee Cancellation (UKT)

This repository contains a Google Colab project that analyses public sentiment surrounding **the cancellation of Indonesia's university tuition fee increase**, officially known as **"Uang Kuliah Tunggal" (UKT)**.  

### 🎨 Related Media
This project was originally showcased on Instagram:  
[View the post](https://www.instagram.com/p/C9eJcqHvXuq/)

### 🎓 Organizational Context
This project was developed as part of my work as a **Data Analyst in the University Student Government (BEM KM UGM)**, specifically within the **Ministry of Data Analysis and Digital Product**, Universitas Gadjah Mada (UGM).

The project classifies social media comments into **positive**, **negative**, and **neutral** categories using a **Support Vector Machine (SVM)** model with **TF‑IDF vectorization**, supported by visualisations such as pie charts and word clouds.

## 📘 Project Overview

This work explores how Indonesian students and citizens reacted to the decision to cancel an increase in tuition fees (*UKT*). The dataset is derived from Twitter posts and processed through the following pipeline:

1. **Preprocessing**
   - Removing numbers, links, mentions, emojis, punctuation.
   - Lowercasing text and applying stemming with *Sastrawi* (Indonesian stemmer).
   - Removing Indonesian stopwords from NLTK and custom-defined lists.

2. **Model Training**
   - Utilises preprocessed IndoNLU dataset (`train_preprocess.tsv` and `valid_preprocess.tsv`).
   - Features extracted with `TfidfVectorizer`.
   - Model: SVM with RBF kernel trained using scikit‑learn.

3. **Prediction & Visualisation**
   - Applies the trained model to a dataset of tweets discussing UKT.
   - Displays results as a **pie chart**, **bar chart**, and **word clouds** for each sentiment type.

## 📄 Context for UK Readers

In Indonesia, *Uang Kuliah Tunggal (UKT)* refers to a single-tuition-fee policy issued by the Ministry of Education. In 2024–2025, an increase to these fees caused wide public criticism.  
This project analyses thousands of public reactions to the **government's decision to revoke that increase**, similar to how UK media might debate changes to student loan repayments or tuition caps.

## ⚙️ Installation and Setup

You can reproduce this project locally or in Google Colab.

```bash
git clone https://github.com/abhinawap/sentiment-analysis-indonesian-tuition-fee-cancellation.git
cd sentiment-analysis-indonesian-tuition-fee-cancellation
pip install -r requirements.txt
```

If using Colab, simply upload the notebook `SentimenPembatalanKenaikanUKT.ipynb` and run all cells.

## 🚀 Usage

Run the notebook step-by-step to:
- Preprocess data.
- Train and evaluate the sentiment model.
- Generate visualisations of the sentiment distribution.

Output includes:
- A pie chart showing sentiment share.
- Word clouds for *positive*, *neutral*, and *negative* classes.

## 📊 Example Output

Example visualisations include:
- **Pie chart:** showing the percentage of sentiment categories.
- **WordClouds:** revealing the most frequent words per sentiment.

These highlight recurring expressions used by Indonesian Twitter users when reacting to the UKT issue.

## 🧩 Technologies Used

| Category | Library/Tool |
|-----------|---------------|
| Data Handling | pandas, numpy |
| Preprocessing | NLTK, Sastrawi, regex |
| Feature Extraction | TfidfVectorizer |
| Modelling | scikit-learn (SVM) |
| Visualisation | matplotlib, seaborn, wordcloud |
| Utility | emoji, joblib |

## 📁 Repository Contents

```
SentimenPembatalanKenaikanUKT.ipynb    # Main notebook file
requirements.txt                        # Environment dependencies
LICENSE                                 # MIT License
runtime.txt                             # (Optional) Python runtime spec
.gitignore                              # Git ignore patterns
```

## 🪪 License

This project is distributed under the MIT License — see the `LICENSE` file for details.

## 📷 Acknowledgements

- IndoNLU project for training datasets  
- NLTK and Sastrawi for Indonesian NLP processing  
- Matplotlib/WordCloud for visualisation  
- Original Colab project: *Sentimen Pembatalan Kenaikan UKT (PieChart)*  

*Last updated:* July 2024
