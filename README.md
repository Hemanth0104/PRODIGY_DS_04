# PRODIGY_DS_04


# 🐦 Twitter Sentiment Analysis

This project focuses on analyzing sentiment in Twitter data using natural language processing (NLP), VADER sentiment scoring, and interactive visualizations.

---

## 📁 Dataset Preparation

We started by uploading and merging two datasets: `twitter_training.csv` and `twitter_validation.csv`. These were loaded into pandas DataFrames, and the column names were standardized to `Id`, `Entity`, `Sentiment`, and `Text`. The combined dataset provided a unified base for processing and analysis.

---

## 🧹 Data Cleaning & Imputation

Initial inspection revealed missing text values primarily associated with certain entities and sentiments. A custom function `fill_missing_text` was implemented to impute missing `Text` entries using the most frequent text per Entity-Sentiment group. This ensured minimal loss of data while maintaining contextual relevance.

---

## 📝 Text Preprocessing

We applied a multi-step cleaning process:
- Lowercasing
- URL and emoji removal
- Special character filtering
- Tokenization using NLTK
- Stopword removal

Cleaned output was stored in a new column named `cleaned_review`. Though a simpler cleaning step later replaced this with a lighter version, the final data remained well-structured.

---

## 🔍 Sentiment Classification (VADER)

VADER (Valence Aware Dictionary and sEntiment Reasoner) was used to score sentiment:
- A `compound_score` was computed for each review.
- Sentiments were labeled as `positive`, `neutral`, or `negative` using a custom classifier based on compound score thresholds.

---

## 🧾 Tokenization & Frequency Analysis

Tokenization was applied to the `cleaned_review` column using `nltk.word_tokenize`. 
- Word frequencies were calculated using Python’s `Counter`.
- The top 20 tokens were visualized using Plotly bar charts, revealing common linguistic patterns across tweets.

---

## 📊 Visualizations

- **Sentiment Distribution**: Displayed via a Plotly bar chart showing counts for each sentiment class.
- **Word Clouds**: Generated for each sentiment class to visualize frequent terms.
- **Unique Tokens per Sentiment**: For each sentiment (`positive`, `negative`, `neutral`), we identified top unique tokens not found in other sentiment categories. These were visualized using Plotly for enhanced interactivity.

---

## 🧠 Observations

- Data was successfully merged and cleaned with minimal loss.
- Text preprocessing effectively normalized the tweet content.
- VADER provided interpretable sentiment scores and labels.
- Token analysis helped in identifying commonly and uniquely used words.
- Visualizations offered both statistical and intuitive understanding of the dataset.

---

## 🚀 Next Steps

Although not covered in this notebook, the presence of ML libraries such as `train_test_split`, `LabelEncoder`, `LogisticRegression`, and evaluation tools like ROC AUC and confusion matrix implies a future plan:
- **Model Training**: Train machine learning models on cleaned text data for supervised sentiment classification.
- **Model Evaluation**: Use evaluation metrics to benchmark model performance.

---

## 📦 Libraries Used

- `pandas`, `numpy`
- `nltk`
- `matplotlib`, `seaborn`, `plotly`
- `sklearn`
- `vaderSentiment`

---




![newplot (2)](https://github.com/user-attachments/assets/11c078a2-579e-4312-9051-4a50c4cbe062)
![newplot (3)](https://github.com/user-attachments/assets/cb655d88-a415-4808-91a3-120587b1708d)
![newplot (4)](https://github.com/user-attachments/assets/c6ac370e-b751-47be-84f3-97b195aa26ab)
![plot](https://github.com/user-attachments/assets/9e85e30e-903f-435f-9174-d37aeaefb462)
![newplot (5)](https://github.com/user-attachments/assets/b64c1895-d7e8-4eef-b924-5e8e2f23a0a7)
