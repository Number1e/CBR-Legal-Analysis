# Analisis Putusan Pengadilan Menggunakan Case-Based Reasoning (CBR)

Proyek ini adalah implementasi sistem *Case-Based Reasoning* (CBR) untuk menganalisis dan menemukan preseden dari dokumen putusan pengadilan pidana. Sistem ini dibangun menggunakan teknik *Natural Language Processing* (NLP) dengan representasi TF-IDF dan membandingkan dua pendekatan retrieval: **Cosine Similarity** dan **Support Vector Machine (SVM)**.

## Struktur Proyek

```
/
|-- README.md
|-- requirements.txt
|-- main
|
|-- Putusan/              # Tempat menyimpan file PDF putusan mentah
|
|-- data/                 # Folder untuk data
|   |-- raw_pdf/          # Tempat menyimpan file PDF putusan mentah
|   |-- raw_text/         # Output teks dari proses cleaning
|   |-- processed/        # Data terstruktur (CSV)
|   |-- results/          # Hasil prediksi
|   |-- eval/             # Hasil evaluasi model
|
|-- models/               # Model dan vectorizer yang telah dilatih
|
```

## Instalasi

Untuk menjalankan proyek ini, pastikan Anda memiliki Python 3.8+ terinstal.

1.  **Clone repositori ini:**
    ```bash
    git clone [https://github.com/URL_REPOSITORY_ANDA/CBR-Legal-Analysis.git](https://github.com/URL_REPOSITORY_ANDA/CBR-Legal-Analysis.git)
    cd CBR-Legal-Analysis
    ```

2.  **Buat dan aktifkan virtual environment (dianjurkan):**
    ```bash
    python -m venv env
    # Windows
    env\Scripts\activate
    # macOS/Linux
    source env/bin/activate
    ```

3.  **Instal semua pustaka yang dibutuhkan:**
    ```bash
    pip install -r requirements.txt
    ```

## Cara Menjalankan Pipeline

Pipeline proyek ini dirancang untuk dijalankan secara bertahap menggunakan Jupyter Notebook.

1.  **Siapkan Data:**
    Letakkan semua file `.pdf` putusan pengadilan yang ingin Anda proses ke dalam folder `/data/raw_pdf/`.

2.  **Jalankan Notebook secara Berurutan:**
    Buka dan jalankan sel-sel di dalam setiap notebook pada folder `/notebooks/` sesuai urutan nomornya:
    -   `main.ipynb`

3.  **Lihat Hasil:**
    -   Data yang telah diproses akan tersedia di `/data/processed/`.
    -   Model yang telah dilatih akan disimpan di `/models/`.
    -   Hasil evaluasi, termasuk metrik dan grafik perbandingan, akan disimpan di `/data/eval/`.

## Hasil
Proyek ini menghasilkan perbandingan kuantitatif antara dua metode retrieval. Berdasarkan hasil evaluasi, pendekatan berbasis kemiripan (Cosine Similarity) seringkali memberikan performa yang lebih stabil untuk menemukan kasus yang relevan dibandingkan dengan pendekatan klasifikasi (SVM) ketika data tidak seimbang.
