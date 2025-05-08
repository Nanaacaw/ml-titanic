# 🛳️ Titanic Survival Prediction

Proyek ini dibuat sebagai bagian dari tugas interview posisi **Machine Learning Intern**. Tujuannya adalah membangun model prediksi sederhana yang bisa menebak apakah seorang penumpang Titanic selamat atau tidak, berdasarkan data yang tersedia dari Kaggle.

## 🎯 Tujuan Proyek
Membangun model machine learning untuk:
- Memprediksi keselamatan penumpang Titanic (`Survived`)
- Melakukan eksplorasi data dan preprocessing
- Melatih model klasifikasi sederhana
- Mengevaluasi performa model dengan metrik yang relevan

## 📂 Dataset
Dataset yang digunakan:  
📦 [`train.csv`](https://www.kaggle.com/c/titanic/data) dari  "Titanic - Machine Learning from Disaster" di Kaggle.

## 🛠️ Tools dan Library
- Python
- Pandas & NumPy
- Scikit-learn
- Matplotlib & Seaborn

## Langkah-langkah Proyek

### 1. Data Exploration (EDA)
- Cek isi dan struktur data (head, info, describe)
- Identifikasi missing values
- Visualisasi data dasar (opsional)

### 2. Preprocessing
- Menangani nilai hilang:
  - `Age`: Diisi dengan median
  - `Embarked`: Diisi dengan modus
  - `Cabin`: Dihapus karena terlalu banyak missing
- Encoding fitur kategorikal:
  - `Sex`: Label Encoding (0 = female, 1 = male)
  - `Embarked`: One-Hot Encoding (`Embarked_Q`, `Embarked_S`)
- Hapus kolom yang tidak relevan: `PassengerId`, `Name`, `Ticket`, `Cabin`

### 3. Persiapan Data untuk Model
- Pisahkan `X` (fitur) dan `y` (target `Survived`)
- Split data: 80% training, 20% testing

### 4. Model Training
- Menggunakan **Logistic Regression**
- Melatih model dengan `X_train`, `y_train`

### 5. Evaluasi Model
- Menggunakan:
  - Accuracy
  - Confusion Matrix
  - Precision
  - Recall
  - F1-Score

- **Evaluasi Tambahan:**
  - **K-Fold Cross Validation**: Validasi model dengan pembagian data ke dalam beberapa fold (5-fold), untuk melihat kestabilan performa model
  - **ROC-AUC Curve**:
    - Visualisasi kemampuan model membedakan kelas 0 dan 1
    - AUC (Area Under Curve) mendekati 1 berarti model makin bagus

## 📊 Hasil & Insight
- Fitur paling berpengaruh:
  - `Sex`: Penumpang wanita punya peluang selamat jauh lebih tinggi
  - `Pclass`: Penumpang kelas atas (1) lebih besar peluangnya selamat
  - `Fare`: Harga tiket juga berpengaruh, meskipun kecil
- Akurasi model sekitar 78-81%
- Model cukup bagus untuk baseline

## 🚀 Cara Menjalankan
1. Clone repo ini:
    ```bash
    git clone https://github.com/Nanaacaw/ml-titanic.git
    cd ml-titanic
    ```
2. Jalankan Notebook:
    - Buka `titanic_model.ipynb` di Jupyter Notebook / VS Code / Google Colab
    - Jalankan sel-sel secara berurutan

## 📝 Catatan
- Proyek ini menggunakan Logistic Regression sebagai baseline model
- Fokus utama adalah memahami proses end-to-end dari data hingga evaluasi model

## 👤 Author
Nana Casmana Ade Wikarta  
Final year Informatics Student, Universitas Singaperbangsa Karawang

---

