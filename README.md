# 🎬 Movie Recommendation System using NLP

### 📌 Overview

This project is an end-to-end **Content-Based Movie Recommendation System** that recommends similar movies using **Natural Language Processing (NLP)** and **Machine Learning** techniques.

Unlike popularity-based recommendation systems, this application analyzes a movie's **overview, genres, and tagline** to understand its content and recommends movies with similar semantic meaning.

The recommendation engine is built using **TF-IDF Vectorization** and **Cosine Similarity**, enabling intelligent recommendations based on textual similarity rather than user ratings.

The project demonstrates the complete machine learning workflow including data cleaning, feature engineering, NLP preprocessing, vectorization, similarity computation, and model serialization.

---

## 🚀 Features

🎬 Search movies by title

🤖 Content-Based Movie Recommendations

🧠 NLP Text Preprocessing

📚 TF-IDF Vectorization

📐 Cosine Similarity Recommendation Engine

🧹 Data Cleaning & Feature Engineering

📦 Model Serialization using Pickle

⚡ Instant Movie Recommendations

---

## 🧠 End-to-End Recommendation Workflow

### 📥 Data Collection

Movie metadata is loaded from the dataset containing information such as:

- Movie Title
- Overview
- Genres
- Tagline
- Vote Average
- Popularity

---

### 🧹 Data Cleaning

Performed extensive preprocessing including:

- Removing duplicate records
- Selecting relevant features
- Handling missing titles
- Filling missing overview and tagline values
- Resetting dataframe index

This ensures a clean dataset before feature engineering.

---

### 🧠 Feature Engineering

Generated a new feature named **Tags** by combining:

- Movie Overview
- Genres
- Tagline

The combined text provides richer contextual information for the recommendation engine.

Example:

```
Overview
   +
 Genres
   +
Tagline
   ↓
  Tags
```

---

### ✂️ NLP Text Preprocessing

Applied Natural Language Processing techniques using **NLTK**.

Processing includes:

- Lowercase conversion
- Regex-based punctuation removal
- Stopword removal
- Word Lemmatization

Lemmatization converts words into their root forms, improving recommendation quality.

Example:

```
running
runs
ran

↓

run
```

---

### 📊 TF-IDF Vectorization

Converted textual movie information into numerical vectors using:

**TF-IDF (Term Frequency-Inverse Document Frequency)**

Configuration:

- Maximum Features: **50,000**
- N-Gram Range: **(1,2)**

TF-IDF gives higher importance to informative words while reducing the weight of frequently occurring words.

---

### 📐 Similarity Computation

Calculated similarity using:

**Cosine Similarity**

Cosine Similarity measures the angle between two TF-IDF vectors instead of comparing word frequencies directly.

Similarity Score:

- **1 → Highly Similar**
- **0 → No Similarity**

---

### 🎯 Recommendation Engine

When a movie title is entered:

1. Locate the movie index
2. Retrieve its TF-IDF vector
3. Compute cosine similarity with all movies
4. Rank similarity scores
5. Return the Top N most similar movies

If the movie is unavailable, the system returns:

```
Movie not found
```

---

### 💾 Model Serialization

The trained artifacts are stored using Pickle for efficient reuse.

Saved files include:

- **df.pkl**
- **tfidf.pkl**
- **tfidf_matrix.pkl**

This avoids rebuilding the recommendation model every time the application is executed.

---

## 🛠️ Tech Stack

### Programming

- Python

### Data Processing

- Pandas
- NumPy

### Data Visualization

- Matplotlib
- Seaborn

### Natural Language Processing

- NLTK
- Regular Expressions

### Machine Learning

- Scikit-learn

### Vectorization

- TF-IDF Vectorizer

### Similarity Metric

- Cosine Similarity

### Model Serialization

- Pickle

---

## ⚙️ Project Architecture

```
  Movie Dataset
        │
        ▼
  Data Cleaning
        │
        ▼
Feature Engineering
        │
        ▼
NLP Text Preprocessing
        │
        ▼
TF-IDF Vectorization
        │
        ▼
  TF-IDF Matrix
        │
        ▼
 Cosine Similarity
        │
        ▼
Recommendation Engine
        │
        ▼
Top Similar Movies
        │
        ▼
Pickle Serialization
```

---

## 🔥 Key Features

✅ Content-Based Recommendation System

✅ Natural Language Processing

✅ Feature Engineering

✅ TF-IDF Vectorization

✅ Cosine Similarity

✅ Text Preprocessing

✅ Stopword Removal

✅ Lemmatization

✅ Pickle Model Serialization

---

## 📈 Machine Learning & NLP Concepts Covered

- Natural Language Processing (NLP)
- Text Preprocessing
- Regular Expressions
- Stopword Removal
- Lemmatization
- Feature Engineering
- TF-IDF Vectorization
- Cosine Similarity
- Content-Based Recommendation Systems
- Information Retrieval
- Text Similarity
- Machine Learning Pipeline
- Model Serialization

---

## 💡 Business Applications

This project can be used for:

- Movie Streaming Platforms
- OTT Platforms
- Personalized Movie Recommendations
- Entertainment Applications
- Digital Content Discovery
- AI-Based Recommendation Systems
- Online Media Libraries
- Content Personalization Engines

---

## 📚 Learning Outcomes

Through this project, I learned:

- End-to-end Recommendation System Development
- Data Cleaning & Feature Engineering
- Natural Language Processing (NLP)
- Regular Expressions
- Text Preprocessing
- Stopword Removal
- Word Lemmatization
- TF-IDF Vectorization
- Cosine Similarity
- Content-Based Recommendation Systems
- Information Retrieval
- Model Serialization using Pickle
- Building Machine Learning Pipelines

---

## 🔮 Future Improvements

🎭 Integrate TMDB API for movie posters and details

🔍 Add fuzzy title search for better user experience

⭐ User rating-based recommendations

🤝 Hybrid Recommendation System (Content + Collaborative Filtering)

🧠 Transformer-based embeddings using Sentence Transformers

☁️ Deploy as a web application

📱 Mobile-friendly interface

⚡ Recommendation caching for faster responses

---

# 👨‍💻 Author

**Kunal Shelukar**

---

# 📜 License

This project is licensed under the **MIT License**.
