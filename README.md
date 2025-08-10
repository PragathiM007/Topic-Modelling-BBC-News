# Topic Modelling on BBC News Articles

## 📌 Project Overview
This project focuses on **unsupervised machine learning** techniques to uncover latent themes and topics in BBC News articles. The dataset contains **2225 articles** published by the BBC between 2004 and 2005, categorized into five sections: **Business, Entertainment, Politics, Sport, and Tech**.

Using **Latent Dirichlet Allocation (LDA)** and **Latent Semantic Analysis (LSA)**, the project identifies hidden patterns in the text, compares vectorization techniques (**CountVectorizer** vs **TF-IDF Vectorizer**), and evaluates the effectiveness of each model.

---

## 🎯 Objectives
- Consolidate BBC News articles from multiple text files into a single dataset.
- Preprocess the text to remove noise and standardize words.
- Apply **LDA** and **LSA** to uncover latent topics.
- Compare model performance between:
  - LDA + CountVectorizer
  - LDA + TF-IDF Vectorizer
  - LSA + CountVectorizer
  - LSA + TF-IDF Vectorizer
- Evaluate model accuracy and topic relevance.
- Visualize topics using **word clouds**.

---

## 📂 Dataset Description

### Source
BBC News dataset (2004–2005), containing:
- **Title** – Headline of the article
- **Description** – Full text content of the article
- **Category** – Predefined BBC section (Business, Entertainment, Politics, Sport, Tech)

### Data Summary
- **Rows:** 2225 articles
- **Columns:** Title, Description, Category
- **Duplicates:** 100 duplicate rows (handled during data wrangling)
- **Missing Values:** None

---

## 🛠️ Methodology

### 1️⃣ Data Wrangling
- Remove duplicates
- Normalize text (lowercasing, expanding contractions, removing punctuation/digits/stopwords)
- Lemmatization using **WordNetLemmatizer**

### 2️⃣ Feature Extraction
- **CountVectorizer** – Token frequency representation
- **TF-IDF Vectorizer** – Adjusted for term importance

### 3️⃣ Topic Modelling
- **LDA** – Probabilistic topic modelling
- **LSA** – Dimensionality reduction via **Truncated SVD**

### 4️⃣ Model Evaluation
- Accuracy, Precision, Recall, and F1-Score per topic
- Comparison between vectorization approaches
- Visual inspection of topics using **word clouds**

---

## 📊 Results Summary

| Model                          | Vectorizer       | Accuracy | Observations |
|--------------------------------|------------------|----------|--------------|
| LDA                            | CountVectorizer  | ~93%     | Best overall performance |
| LDA                            | TF-IDF           | ~85%     | Over-determined entertainment topic |
| LSA                            | CountVectorizer  | Lower    | Less topic clarity |
| LSA                            | TF-IDF           | Lower    | Similar performance drop |

- **Best Performing Model:** LDA with CountVectorizer  
- **Highest F1-Score:** 97% for Sports category  
- **Lowest F1-Score:** ~90% for Politics  

---

## 📷 Visualizations
- **Word Clouds** for each topic
- **Topic-Term Distributions**
- **Model Performance Charts** (Precision, Recall, F1)

---

## 📦 Technologies Used
- Python 3.x
- **Libraries:**
  - `pandas`, `numpy`
  - `scikit-learn`
  - `nltk`
  - `gensim`
  - `matplotlib`, `seaborn`, `wordcloud`

---

## 📈 Business Use Case
Automated topic classification helps:
- Organize large volumes of news content efficiently.
- Enable targeted content delivery to readers.
- Summarize trends and themes across multiple articles.
- Support editorial planning with topic coverage insights.

---

## 🚀 Future Work
- Incorporate more topic modelling algorithms (e.g., BERTopic, NMF).
- Perform time-series topic trend analysis.
- Integrate sentiment analysis for deeper insight.
- Fine-tune hyperparameters for better accuracy.

---

## 🖇️ Repository Structure
├── data/
│ ├── bbc/ # Original BBC news text files
│ ├── processed_data.csv # Consolidated dataset
├── notebooks/
│ ├── topic_modelling.ipynb
├── visuals/
│ ├── wordclouds/
│ ├── performance_charts/
├── README.md


---

## 📜 License
This project is licensed under the MIT License.

---

## 🙋 Author
*Pragath 
📧 Contact: [Your Email Here]  
🔗 GitHub: [Your GitHub Link Here]  


