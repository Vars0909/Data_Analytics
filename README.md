# 🎬 Netflix Titles — Data Analytics Project

An end-to-end data analytics project built on the **Netflix Titles dataset** (`netflix_titles.csv`, 8,807 rows × 12 columns). The project covers exploratory data analysis, sentiment analysis on show descriptions, a machine learning classifier, and an interactive Power BI dashboard.

---

## 📌 Project Overview

This project explores Netflix's content catalog from multiple angles:

1. **Exploratory Data Analysis (EDA)** — understanding the shape and trends in the catalog using pandas, matplotlib, and seaborn.
2. **Machine Learning Model** — predicting whether a title is a Movie or TV Show using a Random Forest Classifier.
3. **Interactive Dashboard** — a Power BI dashboard for visual, business-style exploration of the dataset.
4. **Sentiment Analysis (NLP)** — classifying show/movie descriptions as Positive or Negative using TF-IDF and Logistic Regression.

---

## 📂 Repository Structure

```
├── Data_Analysis_Using_Pandas.ipynb   # Exploratory Data Analysis
├── Machine_Learning_Model.ipynb       # Movie vs TV Show classification
├── DashBoard.ipynb                    # Dashboard-related notebook
├── Sentiment_Analysis.ipynb           # NLP-based sentiment classification
├── netflix_titles.csv                 # Dataset (place in root directory)
└── README.md
```

---

## 📊 1. Data Analysis Using Pandas

Exploratory analysis of the Netflix catalog, including:

- Dataset overview (shape, missing values, cleaning)
- Missing value handling (numerical columns filled with median, categorical filled with `"Unknown"`)
- Movies vs TV Shows distribution
- Top 10 countries producing content
- Most common genres
- Titles released per year (Movies & TV Shows)
- Content rating distribution
- Content duration analysis
- Top directors and actors on Netflix
- Country-wise content breakdown

**Libraries used:** `pandas`, `numpy`, `matplotlib`, `seaborn`

---

## 🤖 2. Machine Learning Model

Predicts whether a title is a **Movie** or **TV Show** based on its metadata (release year, rating, duration, country, and genre):

- Missing value imputation
- Categorical encoding with `LabelEncoder`
- Train/test split (80/20)
- Classification using a **Random Forest Classifier** (100 estimators)

**Results:**
- **Accuracy:** ~99.7%
- Near-perfect precision and recall for both classes, showing that content metadata alone is highly predictive of title type.

**Libraries used:** `scikit-learn` (`RandomForestClassifier`, `LabelEncoder`, `train_test_split`)

---

## 📈 3. Interactive Dashboard (Power BI)

An interactive **Netflix Content Analysis Dashboard** built in Power BI to visually explore the dataset through business-style, click-through filtering (by Content Type and Release Year).

**Key metrics & visuals:**
- **9K** total titles — **6K** Movies (69.6%) vs **3K** TV Shows (30.4%)
- **Netflix Content Growth Over Years** — line chart showing a sharp rise in titles added, especially post-2015
- **Top Countries by Content** — United States leads, followed by India, United Kingdom, Japan, South Korea, and Canada
- **Content Rating Distribution** — donut chart breaking down ratings (TV-MA ~36%, TV-14 ~24.5%, TV-PG ~9.8%, R ~9%, PG-13 ~5.6%, TV-Y7 ~3.8%, and others)
- Interactive slicers for **Content Type** (multi-select) and **Release Year**


---

## 💬 4. Sentiment Analysis

Applies NLP techniques to the `description` field of each title to classify it as **Positive** or **Negative**:

- Text preprocessing: lowercasing, punctuation removal, stopword removal, and lemmatization (`nltk`)
- Rule-based sentiment labeling using curated positive/negative keyword lists
- Feature extraction with **TF-IDF** (top 5,000 features)
- Classification using **Logistic Regression**

**Results:**
- **Accuracy:** ~91.5%
- Strong performance on the Positive class (precision 0.91, recall 1.00); the Negative class is harder to catch (recall 0.37) due to class imbalance in the dataset.

**Libraries used:** `nltk`, `wordcloud`, `scikit-learn` (`TfidfVectorizer`, `LogisticRegression`)


**Illapani Varshini**



## 📄 License

This project is for educational and portfolio purposes.
