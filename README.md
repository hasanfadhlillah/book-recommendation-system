# Sistem Rekomendasi Buku (Book Recommendation System) 📚

[![Python](https://img.shields.io/badge/Python-3.x-blue.svg)](https://www.python.org/)
[![Scikit-learn](https://img.shields.io/badge/scikit--learn-0.24.2-orange.svg)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/pandas-1.3.3-blue.svg)](https://pandas.pydata.org/)

Proyek ini bertujuan untuk membangun sistem rekomendasi buku untuk mengatasi masalah *choice overload* yang sering dihadapi pembaca. Dua pendekatan utama digunakan: Content-Based Filtering dan Collaborative Filtering, untuk memberikan rekomendasi yang personal dan relevan.

---

## 📖 Model yang Dikembangkan

Dua jenis model sistem rekomendasi telah dikembangkan dalam proyek ini:

1.  **Content-Based Filtering**
    * **Logika:** Merekomendasikan buku berdasarkan kemiripan atribut/metadata buku (penulis dan penerbit).
    * **Teknik:** Menggunakan `TfidfVectorizer` untuk mengubah teks metadata menjadi vektor dan `Cosine Similarity` untuk mengukur kemiripan antar buku.

2.  **Collaborative Filtering**
    * **Logika:** Merekomendasikan buku berdasarkan preferensi pengguna lain yang memiliki selera serupa (user-based).
    * **Teknik:** Menggunakan algoritma `K-Nearest Neighbors (KNN)` untuk menemukan "tetangga" terdekat dari seorang pengguna berdasarkan riwayat rating mereka.

---

## 📊 Dataset

Dataset yang digunakan adalah **"Book-Crossings"** yang tersedia di Kaggle.
* **Sumber:** [Book-Crossings Dataset on Kaggle](https://www.kaggle.com/datasets/arashnic/book-crossing-dataset)
* **Terdiri dari 3 file:** `Books.csv`, `Ratings.csv`, dan `Users.csv`.
* **Total Data:** 1.1M+ rating dari 278k+ pengguna untuk 271k+ buku.

---

## ⚙️ Teknologi yang Digunakan

* **Python**
* **Pandas & NumPy** untuk manipulasi data
* **Matplotlib & Seaborn** untuk visualisasi data
* **Scikit-learn** untuk pemodelan (`TfidfVectorizer`, `NearestNeighbors`)
* **Jupyter Notebook** sebagai environment kerja

---

## 🚀 Cara Menjalankan Proyek

1.  **Clone Repositori**
    ```bash
    git clone [https://github.com/NAMA_USER_ANDA/NAMA_REPO_ANDA.git](https://github.com/NAMA_USER_ANDA/NAMA_REPO_ANDA.git)
    cd NAMA_REPO_ANDA
    ```

2.  **Unduh Dataset**
    * Unduh dataset dari [link Kaggle](https://www.kaggle.com/datasets/arashnic/book-crossing-dataset).
    * Ekstrak dan letakkan file `Books.csv`, `Ratings.csv`, dan `Users.csv` di dalam folder utama proyek.

3.  **Jalankan Notebook**
    * Buka dan jalankan file `notebook.ipynb` menggunakan Jupyter Lab atau Google Colab.

---

## 📈 Hasil Evaluasi

Model Collaborative Filtering dievaluasi menggunakan metrik **Precision@10**, yang mengukur seberapa relevan 10 item teratas yang direkomendasikan.

* **Metric:** Precision@10
* **Hasil:** **12.5%**

**Interpretasi:** Dari 10 buku yang direkomendasikan, rata-rata lebih dari 1 buku (1.25 buku) relevan dan kemungkinan besar disukai oleh pengguna, yang merupakan hasil yang baik untuk dataset sebesar ini.
