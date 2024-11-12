<h1 align="center">🔍 Simple Search Engine</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-blue.svg" alt="Python Version">
  <img src="https://img.shields.io/badge/Flask-2.2.3-green.svg" alt="Flask Version">
</p>

<p align="center">
  An intelligent document search engine that leverages natural language processing techniques to provide relevant and personalized search results. Powered by Flask, TF-IDF, and cosine similarity.
</p>

Table of Contents
-----------------

- [Features](#-features)
- [Prerequisites](#-prerequisites)
- [Installation](#-installation)
- [Project Structure](-#project-structure)
- [Usage](#-usage)
- [Key Components](#-key-components)
  - [Text Preprocessing](#text-preprocessing)
  - [Inverted Index](#inverted-index)
  - [TF-IDF Calculation](#tf-idf-calculation)
  - [Cosine Similarity](#cosine-similarity)
  - [Spell Checking](#spell-checking)

  
## 📋 Features

- **Text Preprocessing**: Tokenization, stop word removal, and lemmatization
- **Inverted Index Construction**: Allows efficient term-based lookups
- **TF-IDF Calculation**: Measures the importance of terms in each document
- **Cosine Similarity**: Computes similarity between the query and documents for ranking
- **Spell Checking**: Automatically corrects misspelled terms in user queries
- **Web Interface**: Search through documents using a simple HTML form


## 🚀 Installation

1. **Install Required Packages** Install the necessary Python packages listed in `requirements.txt`:
   ```bash
   pip install -r requirements.txt
2. **Download spaCy Model**
   ```bash
   python -m spacy download en_core_web_sm
3. **Download NLTK Data** Download the stopwords dataset from NLTK
4. **Run the Application** Start the Flask app by running:
   ```bash
   python app.py
   
 The app will be available at `http://127.0.0.1:5000`.

## 🗂️ Project Structure

-----

  1. `app.py`: Main application file with text processing, TF-IDF calculation, and Flask routes.

 2. `templates/index.html`: HTML template for the search interface.

 3. `static/style.css`: CSS file for styling the web interface.

 4. `requirements.txt`: List of required Python packages.

## 🔍 Usage
-----

1.  Open the app in your browser (`http://127.0.0.1:5000`).
2.  Enter a search query in the input box and click "Search."
3.  The application will display documents ranked by relevance to the query, showing their cosine similarity scores. Misspelled terms in the query will be automatically corrected.

## 🔑 Key Components
------

### Text Preprocessing

The text is converted to lowercase, punctuation is removed, stop words are removed, and remaining words are stemmed.

### Inverted Index

An inverted index is created to store document IDs for each unique term, facilitating fast lookup of terms in documents.

### TF-IDF Calculation

The TF-IDF score is calculated for each term in each document. TF (Term Frequency) and IDF (Inverse Document Frequency) scores are used to measure term importance.

### Cosine Similarity

The similarity between the query and each document is calculated using cosine similarity, which helps rank documents based on relevance.

### Spell Checking

The application uses a custom spell checker to automatically correct misspelled terms in user queries, improving the search experience.

