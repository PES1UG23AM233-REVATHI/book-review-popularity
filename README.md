# 📚 Text-Based Prediction of Book Review Popularity

### 🧠 Machine Learning | Natural Language Processing | Logistic Regression

---

## 🔍 Overview
This project predicts whether a **book review** will be **popular** (highly rated) or **not popular**, based solely on its **text content**.  
Using **Natural Language Processing (NLP)** and **Machine Learning**, we analyze linguistic patterns — tone, structure, and vocabulary — to estimate engagement levels.  

The project is inspired by the paper:  
**_“Text-Based Prediction of Book Review Popularity”_** by *Bridget Daly, Stanford University.*



---

## 💡 Motivation
Book review platforms like **Goodreads** and **Amazon** host millions of reviews — but only a few gain significant attention.  
By identifying what makes a review **popular**, this project aims to:
- Improve book recommendation systems  
- Help users write more engaging reviews  
- Demonstrate how **text alone** can predict audience engagement  

---

## 🧰 Tech Stack

| Category | Tools Used |
|-----------|-------------|
| Programming | Python 3 |
| Libraries | Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn |
| NLP | TF–IDF Vectorization |
| Model | Logistic Regression |
| Environment | Google Colab / Jupyter Notebook |

---

## ⚙️ Methodology

### 1️⃣ **Data Loading**
Dataset used: Goodreads *Comics & Graphic Novels* dataset (20,000 samples for performance).  
Loaded using Python’s `gzip` library since the data is in compressed `.json.gz` format.

### 2️⃣ **Preprocessing**
- Removed missing or empty reviews  
- Cleaned text (lowercasing, punctuation & noise removal)  
- Created a new field `clean_review`  
- Defined target label:  
  - Rating ≥ 4 → **Popular (1)**  
  - Rating < 4 → **Not Popular (0)**  

### 3️⃣ **Feature Extraction**
Used **TF–IDF Vectorization** (`max_features=5000`) to convert textual data into numerical form.

### 4️⃣ **Model Development**
- **Model:** Logistic Regression  
- **Train-Test Split:** 80% training / 20% testing  
- **Evaluation Metrics:** Accuracy, Precision, Recall, F1-score  

### 5️⃣ **Visualization**
Created a **confusion matrix heatmap** using Seaborn to visually represent model predictions.

---

## 📊 Results

| Metric | Score |
|--------|--------|
| **Accuracy** | ~82% |
| **Precision** | 0.81 |
| **Recall** | 0.79 |
| **F1-Score** | 0.80 |

📈 **Key Insights:**
- Reviews with emotional or expressive wording are more likely to be popular.  
- Short, generic reviews typically receive lower ratings.  


---

## 🧩 User Interface (Colab Demo)
A simple **Colab interface** was built to allow users to type their own book reviews and get a predicted popularity score.

📸 *Screenshot example:*
![UI Screenshot](https://github.com/PES1UG23AM233-REVATHI/book-review-popularity/blob/main/ui_screenshot.png)
> “Enter a review → Model outputs: Popular / Not Popular.”

---

## 🗃️ Dataset

**File Name:** `goodreads_reviews_comics_graphic.json.gz`  
**Format:** Compressed JSON (`.gz`)  
**Source:** Goodreads Dataset (subset)

Due to large size, the dataset is hosted externally.  
📂 [Download Dataset from Google Drive](https://drive.google.com/drive/folders/1yrnYvXRqzp5PgdA704vDL7QUTT_E2eVA)

> You don’t need to unzip it — the notebook reads the `.gz` file directly using `gzip.open()`.

---

## 💻 How to Run Locally

### 🪜 Setup Steps

```bash
# 1️⃣ Clone the repository
git clone https://github.com/yourusername/book-review-popularity.git
cd book-review-popularity

# 2️⃣ Install dependencies
pip install pandas numpy scikit-learn seaborn matplotlib

# 3️⃣ Run the notebook
jupyter notebook miniML.ipynb

```
---
⚙️ Requirements

Python 3.8+

Jupyter Notebook or Google Colab

Internet access (for downloading dataset if needed)

🎯 Conclusion

✅ The project successfully predicts book review popularity based solely on textual content.
✅ Logistic Regression provided strong baseline performance and interpretability.
✅ The model reveals meaningful relationships between emotional language and user engagement.
Future Enhancements:

Incorporate sentiment polarity and reviewer metadata

Experiment with advanced models (LSTM, BERT)

Develop a web dashboard for live predictions
👨‍💻 Author

REVATHI A N,NIDHI SHETTY

Department of Artificial Intelligence and Machine Learning

PES UNIVERSITY

📧 Email: revrevathi1103@gmail.com
           nidhi.shetty1408@gmail.com

⭐ GitHub Repository

👉 https://github.com/PES1UG23AM233-REVATHI/book-review-popularity




