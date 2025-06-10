# Book Recommendation System 📚

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![Scikit-learn](https://img.shields.io/badge/scikit--learn-0.24.2-orange.svg)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/pandas-1.3.3-blue.svg)](https://pandas.pydata.org/)

A comprehensive book recommendation system developed as a machine learning project. This repository contains the implementation of two distinct recommendation models using the Book-Crossing dataset from Kaggle.

## Project Overview

In the vast world of literature, readers often face "choice overload," making it difficult to find books that match their tastes. This project addresses this challenge by building a recommendation engine to provide personalized book suggestions, enhancing user experience and engagement on digital platforms.

The primary goal is to develop and compare two popular recommendation techniques:
1.  **Content-Based Filtering:** Recommends books based on item metadata (e.g., author, publisher).
2.  **Collaborative Filtering:** Recommends books based on the preferences and rating history of like-minded users.

## Features

* **Dual-Model Approach**: Implements both Content-Based and Collaborative Filtering to provide robust recommendations.
* **Content-Based Filtering**:
    * Utilizes `Book-Author` and `Publisher` as content features.
    * Employs `TfidfVectorizer` to convert text features into a vector space.
    * Calculates `Cosine Similarity` to find and recommend similar books.
* **Collaborative Filtering**:
    * Uses explicit user ratings (scale 1-10) for training.
    * Implements the **Singular Value Decomposition (SVD)** algorithm from the `surprise` library to predict user ratings.
    * Generates top-N recommendations based on the highest predicted ratings.

## Dataset

This project uses the **Book-Crossing Dataset**, which can be found on Kaggle: [Book Recommendation Dataset](https://www.kaggle.com/datasets/arashnic/book-recommendation-dataset).

The dataset consists of three files:
* `Books.csv`: Contains book information such as ISBN, title, author, and publisher.
* `Users.csv`: Contains user demographic data like ID, location, and age.
* `Ratings.csv`: Contains user-book interactions, including explicit (1-10) and implicit (0) ratings.

## Evaluation

* **Collaborative Filtering (SVD)**: Evaluated using **Root Mean Squared Error (RMSE)** to measure the accuracy of rating predictions. The model achieved an `RMSE` of approximately **1.68**.
* **Content-Based Filtering**: Evaluated using **Precision@k**, which measures the relevance of the top recommendations. The model achieved a `Precision@5` of **1.0 (100%)** when recommending books by the same author.

## How to Run

1.  **Clone the repository:**
    ```bash
    git clone <repository-url>
    ```
2.  **Install dependencies:**
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn surprise
    ```
3.  **Download the dataset** from the Kaggle link above and place the `.csv` files in the project root.
4.  **Run the Jupyter Notebook or Python script:**
    * Open and run `proyek_rekomendasi.ipynb` in Jupyter.
    * Or run the script from your terminal: `python proyek_rekomendasi.py`
