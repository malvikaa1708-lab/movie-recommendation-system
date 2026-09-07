# 🎬 Movie Recommendation System

### Content-Based Movie Recommendation using Python & Machine Learning

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-blue?logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Data%20Processing-blue?logo=numpy)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-Machine%20Learning-orange?logo=scikit-learn)
![NLTK](https://img.shields.io/badge/NLTK-NLP-green)

---

## 📌 Overview

This project implements a **content-based movie recommendation system** using Python and Jupyter Notebook.

The system analyzes movie metadata such as **overview, genres, keywords, cast, and director** to identify movies with similar content.

The movie information is combined into a text-based feature called **tags**, which is then preprocessed, vectorized using `CountVectorizer`, and compared using **Cosine Similarity**.

When a user enters a movie title, the system recommends movies that are most similar to it.

---

## ✨ Features

- 📊 Movie dataset analysis
- 🧹 Data cleaning and preprocessing
- 🎭 Genre extraction
- 🔑 Keyword extraction
- 🎭 Cast information processing
- 🎬 Director extraction
- 📝 Feature engineering using movie tags
- 🌱 Text preprocessing and stemming
- 🔢 Text vectorization using CountVectorizer
- 📐 Cosine similarity calculation
- 🎯 Similar movie recommendations

---

## 🔄 Project Workflow

```text
Movie Dataset
      ↓
Data Loading
      ↓
Merge Movie & Credits Data
      ↓
Data Cleaning
      ↓
Feature Extraction
      ↓
Create Movie Tags
      ↓
Text Preprocessing
      ↓
CountVectorizer
      ↓
Feature Vectors
      ↓
Cosine Similarity
      ↓
Movie Recommendations
```

---

## 🧠 How It Works

### 1. Data Loading

The project uses two datasets containing movie and credits information:

- `movies.csv`
- `credits.csv`

The datasets are loaded using **Pandas**.

---

### 2. Data Merging

The movie and credits datasets are merged using the movie `title`.

This brings together information about the movie along with its cast and crew.

---

### 3. Feature Selection

The following movie attributes are used for recommendation:

- Movie ID
- Title
- Overview
- Genres
- Keywords
- Cast
- Director

These features provide information about the content and characteristics of each movie.

---

### 4. Data Preprocessing

The data is cleaned and missing values are handled.

JSON-like columns such as genres, keywords, cast, and crew are converted into usable lists.

For the cast, the most relevant cast members are extracted, while the director is identified from the crew information.

---

### 5. Feature Engineering

Important movie information is combined into a single **tags** feature.

```text
Overview
   +
Genres
   +
Keywords
   +
Cast
   +
Director
   ↓
Movie Tags
```

This creates a text representation of each movie that can be used for similarity calculation.

---

### 6. Text Preprocessing

The movie tags are converted to lowercase and processed using **Porter Stemmer**.

Stemming reduces words to their root form so that similar words can be treated more consistently.

Example:

```text
loving → love
loved  → love
```

---

### 7. Text Vectorization

The processed movie tags are converted into numerical vectors using **CountVectorizer**.

The implementation uses:

```python
CountVectorizer(
    max_features=5000,
    stop_words="english"
)
```

This converts the textual movie information into a numerical representation that can be compared mathematically.

---

### 8. Cosine Similarity

**Cosine Similarity** is used to measure how similar two movie vectors are.

The similarity scores are calculated between all movies and stored in a similarity matrix.

A higher similarity score indicates that two movies have more similar content.

---

### 9. Recommendation

The recommendation function takes a movie title as input.

```python
recommend("Avatar")
```

The system:

1. Finds the selected movie.
2. Retrieves its similarity scores.
3. Sorts movies based on similarity.
4. Removes the selected movie itself.
5. Returns the most similar movies.

---

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming |
| Jupyter Notebook | Development & experimentation |
| Pandas | Data manipulation |
| NumPy | Numerical operations |
| Scikit-learn | Vectorization & similarity |
| NLTK | Text preprocessing |
| CountVectorizer | Text feature representation |
| Cosine Similarity | Similarity calculation |

---

## 📂 Project Structure

```text
movie-recommendation-system/
│
├── Movie_Recommendation_System.ipynb
├── movies.csv
├── credits.csv
├── README.md
├── requirements.txt
│
└── images/
    └── recommendation-demo.png
```

> If the datasets are not included in the repository, add instructions for obtaining them instead of uploading large dataset files.

---

## 🚀 How to Run

### 1. Clone the repository

```bash
git clone https://github.com/malvikaa1708-lab/movie-recommendation-system.git
```

### 2. Navigate to the project

```bash
cd movie-recommendation-system
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

### 5. Open the notebook

```text
Movie_Recommendation_System.ipynb
```

Run the cells sequentially.

---

## 📊 Example

### Input

```text
Avatar
```

### Output

The system returns a list of movies with the highest similarity scores to the selected movie.

---

## 🎯 Skills Demonstrated

- Machine Learning
- Recommendation Systems
- Data Preprocessing
- Feature Engineering
- Natural Language Processing
- Text Vectorization
- Similarity Algorithms
- Python
- Data Analysis
- Jupyter Notebook

---

## 🔮 Future Improvements

- 🌐 Build a web interface using Streamlit
- 🚀 Deploy the recommendation system
- 🔤 Experiment with TF-IDF vectorization
- ⚖️ Improve feature weighting
- 👤 Add user-based recommendations
- 🤝 Combine content-based and collaborative filtering

---

## 👩‍💻 Author

**Malvika**

AI/ML & AI Automation Enthusiast

[GitHub](https://github.com/malvikaa1708-lab)
