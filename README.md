# 🎙️ NLP Analysis — Australian Radio Talkback Transcripts

A natural language processing project that analyses 29 Australian radio talkback transcripts to uncover recurring themes and compare content differences between public (ABC) and commercial radio stations.

---

## 📌 Project Overview

This project applies text analysis and topic modelling techniques to a corpus of Australian English radio transcripts sourced from the **Australian National Corpus (AusNC)**. The goal is to identify what topics dominate public vs. commercial radio and understand regional audience engagement patterns.

**Dataset:** 29 plain text transcript files from the Australian National Corpus (managed by Griffith University, 2012–2023)  
**Radio stations covered:** ABC National, ABC Eastern, ABC Southern/Western, Commercial Eastern, Commercial Southern/Western  
**Key techniques:** TF-IDF Vectorization, LDA Topic Modelling, N-gram Analysis, Word Clouds

---

## 🗂️ Station Categories

| Code | Description |
|---|---|
| NAT | ABC National Radio |
| ABCE | ABC Radio — Eastern Australia |
| ABCNE | ABC Radio — Southern & Western Australia |
| COME | Commercial Radio — Eastern Australia |
| COMNE | Commercial Radio — Southern & Western Australia |

---

## 🔧 Pipeline Steps

### 1. Data Loading & Exploration
- Loaded 29 transcript files, categorised by filename prefix (ABC vs. Commercial)
- Checked for missing values and validated category distribution
- Visualised category frequency using bar charts

### 2. Text Preprocessing
- Generated **word clouds** across all transcripts and per category
- Tokenised text into individual words using NLTK
- Extracted **bigrams and trigrams** to surface common conversational phrases (e.g. *"a little bit"*, *"I think"*)

### 3. Data Cleaning
- Converted text to lowercase and removed punctuation
- Removed standard English stopwords plus domain-specific filler words (*"um"*, *"uh"*)
- Applied **lemmatization** to reduce words to their base forms
- Validated cleaning effectiveness by reviewing most frequent remaining terms

### 4. Topic Modelling — LDA
- Vectorised cleaned text using **TF-IDF** (Term Frequency–Inverse Document Frequency)
- Fitted a **Latent Dirichlet Allocation (LDA)** model with 5 topics
- Identified key terms per topic to label recurring themes

---

## 🔍 Key Findings — 5 Topics Identified

| Topic | Key Terms | Theme |
|---|---|---|
| Topic 1 | plant, garden, tree, bird, house | 🌿 Gardening & Nature (Queensland focus) |
| Topic 2 | doctor, blood, golf, salt | 🏥 Health, Medicine & Sports |
| Topic 3 & 4 | person, remember, wanted, case | 💬 Personal Anecdotes & Talkback Exchanges |
| Topic 5 | flower, paint, book, green | 🎨 Art, Literature & Nature |

### Public vs. Commercial Radio Differences
- **ABC (Public) stations** focused more on topics like **health, gardening, and community issues**
- **Commercial stations** leaned toward more **entertainment-driven and regionally specific** content
- Bigram/trigram analysis revealed conversational phrases unique to each station group

---

## 📁 Repository Structure

```
├── notebooks/
│   └── nlp_radio_analysis.ipynb   # Full analysis notebook
├── data/
│   └── transcripts/               # 29 .txt transcript files
└── README.md
```

---

## 🚀 How to Run

```bash
# Install dependencies
pip install nltk scikit-learn matplotlib seaborn wordcloud pandas

# Launch notebook
jupyter notebook notebooks/nlp_radio_analysis.ipynb
```

---

## 🛠️ Tech Stack

| Tool | Purpose |
|---|---|
| Python | Core language |
| NLTK | Tokenization, stopwords, lemmatization |
| scikit-learn | TF-IDF Vectorization, LDA model |
| Matplotlib / Seaborn | Visualisations and charts |
| WordCloud | Word frequency visualisation |
| Pandas | Data handling |

---

## 👤 Author

**Shivansh Pandey**  
Master of Data Science and Innovation — University of Technology Sydney  
[LinkedIn](https://linkedin.com/in/your-link) | [GitHub](https://github.com/shivanshweb)
