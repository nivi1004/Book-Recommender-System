# **Book Recommender System**

The **Book Recommender System** is a data-driven application that provides **personalized book recommendations** based on user preferences and historical ratings.  
It leverages **collaborative filtering** and **cosine similarity** to suggest books that align with a user’s reading interests.  
The system features a **Flask-based web interface** where users can explore popular books and receive tailored recommendations.

---

## 📖 Overview
With millions of books available today, discovering titles that truly resonate with an individual’s taste can be challenging.  
This system addresses the issue by:
- Analyzing historical user ratings
- Identifying patterns in similar user behavior
- Recommending books with high similarity scores to those the user already enjoys

---

## 📂 Dataset
Three datasets were used:

1. **Books Dataset (`books.csv`)**
   - ISBN, Book Title, Author, Publisher, Year of Publication, Cover Image URLs

2. **Ratings Dataset (`ratings.csv`)**
   - User-ID, ISBN, Book Rating (1–10)

3. **Users Dataset (`users.csv`)**
   - User-ID, Location, Age

---

## 🛠 Data Preprocessing
- Removed rows with missing critical values (`Book-Author`, `Publisher`, `Image-URL-L`)
- Added a lowercase title column for easier matching
- Merged datasets to form a user-book rating matrix
- Filtered:
  - Users with more than 200 ratings
  - Books with at least 50 ratings

---

## 🤖 Recommendation Engine
**Technique:** Collaborative Filtering + Cosine Similarity

**Process:**
1. Create a pivot table of books vs. users with ratings filled (missing = 0)
2. Calculate cosine similarity between books
3. When a user inputs a book:
   - Find similarity scores
   - Sort and return **top N** similar books

---

## 🌐 Web Interface
Built with **Flask**:
- **Homepage**: Displays 50 popular books with cover images, authors, ratings, and vote counts
- **Recommendation Page**: User enters a book title → system shows similar books with images and details

---

## 📊 Summary of Achievements
- Accurate, personalized recommendations
- Efficient handling of large datasets
- Intuitive, responsive web interface

---

## ⚠ Challenges & Solutions
- **Sparse rating matrix** → filtered low-activity users/books to improve density
- **Similarity accuracy** → optimized cosine similarity implementation

---

## 🚀 Future Improvements
- Incorporate hybrid recommendation (content-based + collaborative)
- Include NLP for book description similarity
- Support for multilingual book titles

---

## 🏗 Tech Stack
- **Python** (Pandas, NumPy, Scikit-learn)
- **Flask** (Web framework)
- **HTML/CSS** (Frontend)
- **Jupyter Notebook** (Development & testing)

---

## 📜 References
- [Machine Learning Specialization – Coursera](https://www.coursera.org/specializations/machine-learning-introduction)  
- [Flask Documentation](https://flask.palletsprojects.com/en/2.1.x/)  
- [Scikit-learn Documentation](https://scikit-learn.org/)  

---
