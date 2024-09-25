

---

# Music Recommendation System

## Overview

This repository contains code for a basic music recommendation system using Python. The recommendation system suggests similar songs based on the textual content of song lyrics.

## How it Works

The recommendation system utilizes two main concepts: TF-IDF (Term Frequency-Inverse Document Frequency) and cosine similarity.

### TF-IDF (Term Frequency-Inverse Document Frequency)

TF-IDF is a numerical statistic that reflects the importance of a word in a document relative to a collection of documents. It consists of two parts:

1. **Term Frequency (TF)**: Measures how frequently a term occurs in a document. It is calculated as the number of times a term appears in a document divided by the total number of terms in the document.

    ```
    TF = (Number of times term appears in a document) / (Total number of terms in the document)
    ```

2. **Inverse Document Frequency (IDF)**: Measures the rarity of a term across all documents. It is calculated as the logarithm of the total number of documents divided by the number of documents containing the term.

    ```
    IDF = log_e(Total number of documents / Number of documents containing the term)
    ```

The TF-IDF score for a term in a document is obtained by multiplying its TF and IDF scores.

### Cosine Similarity

Cosine similarity is a measure of similarity between two non-zero vectors of an inner product space. In the context of the recommendation system, cosine similarity is used to quantify the similarity between the TF-IDF vectors of different songs' lyrics.

It calculates the cosine of the angle between two vectors, represented as documents in a multi-dimensional space. The cosine of the angle ranges from -1 to 1, where:

- 1 indicates perfect similarity.
- 0 indicates no similarity.
- -1 indicates perfect dissimilarity.

## Usage

To use the recommendation system:

1. Ensure you have Python installed on your system.
2. Clone this repository to your local machine.
3. Install the required dependencies using pip:

    ```
    pip install -r requirements.txt
    ```

4. Run the provided Python script to load the dataset, preprocess the lyrics, and generate recommendations.

    ```
    python recommend_songs.py
    ```

5. Follow the prompts to enter a song name for which you want recommendations.

## Dataset

The dataset used in this recommendation system contains song information including song titles and lyrics. It is stored in CSV format.

## Author

This recommendation system was developed by Fawad Saqlain.

---