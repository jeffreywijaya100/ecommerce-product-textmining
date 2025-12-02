# **Product Text Classification for E-Commerce**

Pada proyek ini, saya membangun sistem klasifikasi otomatis untuk mengelompokkan deskripsi produk e-commerce ke dalam empat kategori, yaitu Household, Books, Electronics, dan Clothing & Accessories. Sistem ini bertujuan membantu perusahaan dalam proses penyaringan dan pengelompokan produk secara efisien berdasarkan teks deskripsi.

## Tahapan Pengerjaan

### 1. Text Pre-processing

- Case folding & cleaning (menghapus angka, simbol, dan karakter non-alpha)
    
- Tokenization untuk mengubah teks menjadi unit-unit yang lebih kecil dan mudah dikelola yang disebut token
    
- Stopword removal untuk menghapus kata-kata umum seperti "yang", "dan", dan "di" dari teks
    
- Lemmatization untuk mengubah kata ke base form sesuai tata bahasa, misal dari berlari jadi lari
    
- Hasil akhir berupa token yang telah dinormalisasi dan siap untuk vectorization

### 2. Text Representation (Vectorization)

Dua metode representasi teks digunakan untuk membandingkan kinerja model:

- CountVectorizer/ Bag of Words (BoW)
    
- TF-IDF

### 3. Machine Learning Modeling
   
Saya menggunakan dua algoritma untuk membangun model klasifikasi:

- Support Vector Machine (SVM)
    
- Random Forest

Setiap algoritma dilakukan tuning minimal 2 hyperparameter, antara lain:

- SVM → C, kernel
    
- Random Forest → n_estimators, max_depth

### 5. Model Evaluation

Evaluasi performa dilakukan menggunakan data test dengan metrik:

- Accuracy
    
- Precision
    
- Recall
    
- F1-Score

Semua hasil evaluasi disajikan dalam bentuk summary tabel untuk membandingkan performa setiap kombinasi metode text representation dan algoritma machine learning.

<img width="1313" height="354" alt="image" src="https://github.com/user-attachments/assets/406f6c39-508c-4b11-a3b5-700bd7efc1fd" />


## Hasil dan Insight

Berdasarkan hasil eksperimen:

- Model dengan TF-IDF + SVM menghasilkan performa terbaik dengan skor akurasi dan F1-Score paling tinggi dibanding kombinasi lain.

- Random Forest bekerja baik pada BoW, namun kurang optimal pada TF-IDF dibanding SVM.

- Penggunaan teknik TF-IDF memberikan representasi kata yang lebih informatif dibanding BoW sehingga meningkatkan akurasi model berbasis SVM. Hal ini menunjukkan bahwa TF-IDF mampu mengekstrak dan merepresentasikan data teks lebih baik dibandingkan dengan BoW.

## Impact / Business Value

Penerapan model klasifikasi otomatis ini memberikan dampak signifikan terhadap operasional perusahaan e-commerce, antara lain:

✔ Meningkatkan efisiensi proses kurasi produk
Produk dapat dikategorikan otomatis tanpa inspeksi manual sehingga menghemat waktu tim operasional.

✔ Mengurangi human error dalam kategorisasi
Sistem berbasis machine learning memberikan standar konsisten dalam pengelompokan deskripsi produk.

✔ Mempercepat proses onboarding seller & listing katalog
Seller baru dapat mem-posting produk dengan cepat karena kategori dapat terisi otomatis.

✔ Meningkatkan pengalaman customer
Produk tersusun lebih rapi sehingga pencarian kategori lebih akurat → berdampak pada peningkatan conversion rate.

✔ Dapat diskalakan untuk kategori tambahan
Model dapat dikembangkan untuk mendukung lebih banyak kategori seiring pertumbuhan katalog e-commerce.
