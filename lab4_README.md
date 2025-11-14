# 📘 Lab 4 – Text Feature Engineering on Azure

This lab focused on extracting, transforming, and combining different **text-based features** from the Goodreads reviews dataset to prepare a rich and clean feature table for modeling.  
All work was done on **Azure Databricks** using **PySpark**, and results were stored in the **Gold layer** of Azure Data Lake.

---

## 🧩 Data Preparation
The curated Goodreads review data (in Delta format) was used as the base for feature extraction.  
This dataset already contained review text, book details, and metadata like `review_id`, `book_id`, and `rating`.

---

## 🧠 Step 6.5 – Sentiment & Length Feature Extraction
We built sentiment and text-length features for every review.

- Used **VADER Sentiment Analyzer (`nltk.sentiment.vader`)**
- Calculated:
  - `sentiment_pos`
  - `sentiment_neg`
  - `sentiment_neu`
  - `sentiment_compound`
- Added:
  - `review_length_chars` (character count)
  - `review_length_words` (word count)

All features were saved in:
/gold/sentiment_length_features/


---

## 🔢 Step 7 – Combine All Features and Save Final Gold Dataset
We merged:
1. **Sentiment & length features**  
2. **TF-IDF features** (`tf`, `df`, `idf`, `tfidf`)  
3. **Metadata** (`review_id`, `book_id`, `rating`, `title`)

Merges were done on `review_id`.  
Columns were renamed for clarity (`tfidf_score`, `idf_weight`, `term_frequency`, `document_frequency`).

---

## 🏆 Bonus Features
To earn the bonus and enrich modeling quality, we added:
- **`sentiment_label`** → categorical label (positive / neutral / negative)  
- **`review_density`** → ratio of characters to words  
- **`exclamation_count`** → number of “!” to show emotional intensity  

---

## 💾 Final Output
All combined features were stored successfully in:


/gold/features_v2/


Final printout confirmed:


✅ Final combined feature dataset saved successfully to Gold layer under 'features_v2/'
🎉 Bonus features included: sentiment_label, review_density, and exclamation_count.


---

## ✅ Summary
This lab covered:
- Sentiment and text length feature engineering  
- TF-IDF creation and validation  
- Schema checks and data quality validation  
- Feature merging into a single Gold dataset  



