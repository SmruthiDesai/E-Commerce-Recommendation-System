# 🛍️ E-Commerce Recommendation System

This project implements a **hybrid recommendation system** for women’s clothing reviews. It combines **content-based filtering** (using TF-IDF and cosine similarity on review text) and **collaborative filtering** (user-based recommendations using rating similarities).

---

## 📌 Features

* **Content-Based Filtering**

  * Uses `TfidfVectorizer` to transform review text.
  * Computes cosine similarity between products.
  * Recommends items similar to a given product.

* **Collaborative Filtering**

  * Creates a user-item matrix (Age × Clothing ID).
  * Computes user similarity using cosine similarity.
  * Recommends items based on ratings of similar users.

---

## 🗂 Dataset

The project uses the **Women’s Clothing E-Commerce Reviews** dataset (~50K records).

Main columns:

* `Clothing ID` – unique identifier for each product
* `Age` – user’s age (used here as a proxy for user ID)
* `Review Text` – customer review
* `Rating` – rating given to the product
* `Recommended IND` – whether the reviewer recommended the product
* `Division Name`, `Department Name`, `Class Name` – product categories

---

## ⚙️ Installation

Clone the repo and install dependencies:

```bash
git clone <repo_url>
cd e-commerce-recommendation-system
pip install -r requirements.txt
```

### Requirements

* Python 3.12+
* pandas
* numpy
* scikit-learn

---

## 🚀 Usage

### 1. Content-Based Recommendation

```python
recommend_content(product_id=767, top_n=5)
```

Returns top 5 products most similar to the given `Clothing ID`.

---

### 2. Collaborative Filtering Recommendation

```python
recommend_collab(user_id=34, top_n=5)
```

Returns top 5 products recommended for the user with `Age = 34`.

⚠️ Note: Here, `Age` is used as the user identifier.

---

## 📊 Example Output

**Collaborative Filtering Example:**

```
Top recommendations (Collaborative):
   Clothing ID              Title               Review Text
160        1126     So sad not mine   Love everything about this coat...
164        1126        So pretty!   I bought this and like other reviews...
233        1030  Must have, right on trend, but still classic
...
```

---

## 🧩 Project Structure

```
├── Womens Clothing E-Commerce Reviews.csv   # Dataset
├── recommendation_system.ipynb              # Jupyter Notebook with code
├── README.md                                # Project documentation
└── requirements.txt                         # Dependencies
```

---

## 🔮 Future Improvements

* Evaluate model performance using **precision, recall, and RMSE metrics**.
* Develop a **Python demo application** to showcase personalized product suggestions.
* Build an **API-based deployment** for real-time recommendations.
* Use **Matrix Factorization (SVD/ALS)** for collaborative filtering.
* Integrate a **dashboard or web app** (Streamlit/Flask/Django) for interactive recommendations.

---

## 📌 Author

Smruthi Desai

---

