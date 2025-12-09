# Prediksi Nilai Akhir Mahasiswa Menggunakan Machine Learning dan Deployment Berbasis Gradio


## 🚀 Gambaran Umum Proyek

Proyek ini mengimplementasikan studi kasus Data Science di bidang pendidikan/pelatihan menggunakan metodologi **CRISP-DM**.

Tujuan utama proyek adalah **memprediksi probabilitas kelulusan (Lulus/Gagal)** peserta pelatihan. Model ini dikembangkan untuk mengidentifikasi dini peserta yang berisiko gagal, sehingga intervensi belajar dapat diberikan tepat waktu.
## 📌 Fitur Utama

- Data preprocessing lengkap
Meliputi cleaning, imputasi, encoding, dan scaling menggunakan pipeline.

- Model Machine Learning
Menggunakan Logistic Regression untuk prediksi kelulusan serta model regresi untuk prediksi nilai akhir.

- Evaluasi Model
Menghasilkan metrik seperti akurasi, confusion matrix, dan classification report.

- Model Deployment
Menggunakan Gradio sebagai antarmuka interaktif untuk melakukan prediksi secara real-time.
## 🛠 Teknologi yang Digunakan

- Python 3.x

- Pandas

- NumPy

- Scikit-Learn

- Joblib

- Gradio

- Jupyter Notebook

## 📂 Struktur Repository
├── Dataset Pelatihan.csv       # Dataset yang digunakan
├── reg_pipeline_nilai.joblib   # Model pipeline untuk prediksi nilai akhir
├── model_logreg_kelulusan.pkl  # Model prediksi kelulusan
├── preprocessor_deployment.pkl # Preprocessor (encoding + scaling)
├── notebook.ipynb              # Notebook CRISP-DM (pemodelan lengkap)
├── app_gradio.py               # Aplikasi Gradio untuk prediksi
└── README.md                   # Dokumentasi proyek

## ⚙️ Metodologi CRISP-DM

Proyek diimplementasikan secara sistematis melalui enam tahapan:

#### 1. Business Understanding
* **Fokus:** Menetapkan tujuan prediksi kelulusan sebagai masalah **Klasifikasi Biner**.

#### 2. Data Understanding
* **Fokus:** Eksplorasi data, identifikasi nilai non-standar pada kolom `Nilai`.

#### 3. Data Preparation
* **Teknik:** Menggunakan **Scikit-learn Pipeline** dan **ColumnTransformer** untuk pemrosesan yang konsisten.
* **Langkah Kunci:** Pembersihan `Nilai`, **Iterative Imputation** untuk nilai numerik, **Standardisasi (Scaling)**, dan **One-Hot Encoding** untuk data kategorikal.

#### 4. Modeling
* **Algoritma:** **Logistic Regression**.
* **Alasan:** Sederhana, mudah diinterpretasi, dan baik untuk *baseline* masalah klasifikasi biner.

#### 5. Evaluation
* **Metode:** Mengukur kinerja model menggunakan **Akurasi**, **Confusion Matrix**, dan **Classification Report**.
* **Hasil:** Akurasi $\approx 96\%$ (menunjukkan kemampuan prediksi yang baik, namun dengan catatan perlu mencermati ketidakseimbangan data).

#### 6. Deployment
* **Implementasi:** Menyimpan model (`model_logreg_kelulusan.pkl`) dan *preprocessor* (`preprocessor_deployment.pkl`) menggunakan `joblib` untuk skenario prediksi *real-time*.
