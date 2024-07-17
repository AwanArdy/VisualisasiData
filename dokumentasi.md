### **Analisis Data Kanji: Frekuensi Penggunaan, Tingkat Kesulitan dan Jumlah Goresan**

Proyek ini menganalisis data kanji berdasarkan frekuensi penggunaan, tingkat kesulitan (grade), jumlah goresan, dan jumlah pembacaan. Tujuannya adalah untuk memahami hubungan antara variabel-variabel ini dan mengidentifikasi pola-pola menarik dalam penggunaan kanji.


#### **Dataset**
Dataset yang digunakan berisi informasi tentang sekitar 300 kanji, termasuk:
- **Kanji :** Karakter kanji itu sendiri
- **Strokes :** Jumlah goresan pada kanji
- **Grade :** Tingkat kesulitan kanji (1 - 6)
- **Freq :** Frekuensi penggunaan kanji
- **JLPT_new :** Level JLPT (Japanese Language Proficiency Test) yang menguji kanji tersebut
- **Readings_on :** Pembacaan onyomi dari kanji
- **Readings_kun :** Pembacaan kunyomi dari kanji


#### **Metodologi**
1. **Pemrosesan Data :**
    - Memuat data kanji dari file JSON
    - Mengubah data menjadi DataFrame Pandas
    - Menangani nilai yang hilang (NaN) dengan menggantinya dengan rata-rata kolom
    - Menghitung jumlah pembacaan onyomi dan kunyomi untuk setiap kanji

2. **Analisis Regresi :**
    - Membuat model regresi linear untuk memprediksi frekuensi penggunaan kanji berdasarkan tingkat kesulitan, jumlah goresan dan jumlah pembacaan
    - Membagi data menjadi data latih (80%) dan data uji (20%)
    - Melatih model regresi dengan data latih
    - Mengevaluasi model dengan menghitung Mean Squared Error (MSE) dan R-squared (R2) pada data uji

3. **Visualisasi Data :**
    - **Scatter Plot Interaktif (Plotly) :** Menampilkan hubungan antara frekuensi penggunaan dan tingkat kesulitan kanji untuk setiap level JLPT
    - **Histogram (Seaborn) :** Menampilkan distribusi frekuensi penggunaan kanji untuk setiap level JLPT
    - **Heatmap (Seaborn) :** Menampilkan jumlah kanji untuk setiap kombinasi jumlah goresan dan tingkat kesulitan
    - **Scatter Plot 3D (Plotly) :** Menampilkan hubungan antara frekuensi penggunaan, tingkat kesulitan dan jumlah goresan dalam bentuk 3D


#### **Hasil**
- **Analisis Regresi :** Model regresi linear menunjukkan bahwa tingkat kesulitan, jumlah goresan dan jumlah pembacaan memiliki pengaruh yang signifikan terhadap penggunaan kanji

- **Visualisasi :**
    - Scatter plot menunjukkan bahwa kanji dengan tingkat kesulitan yang lebih tinggi cenderung memiliki frekuensi penggunaan yang lebih rendah

    - Histogram menunjukkan bahwa sebagian besar kanji memiliki frekuensi penggunaan yang rendah dan hanya sedikit kanji yang memiliki frekuensi penggunaan yanng sangat tinggi

    - Heatmap menunjukkan bahwa kanji dengan jumlah goresan yang lebih banyak cenderung memiliki tingkat kesulitan yang lebih tinggi

    - Scatter plot 3D memberikan gambaran yang lebih lengkap tentang hubungan antara ketiga variabel


#### **Kesimpulan**
Proyek ini memberikan wawasan tentang pola penggunaan kanji dalam bahasa Jepang. Hasil analisis dapat digunakan untuk :
- **Pengembangan Materi Pembelajaran :** Membantu guru dan pembuat materi pembelajaran untuk menentukan urutan pengajaran kanji yang lebih efektif berdasarkan tingkat kesulitan dan frekuensi penggunaan

- **Penelitian Linguistik :** Memberikan informasi tentang bagaimana karakteristik kanji (seperti jumlah goresan dan jumlah pembacaan) mempengaruhi penggunaannya dalam bahasa Jepang

- **Pengembangan Aplikasi :** Membantu dalam pengembangan aplikasi pembelajaran bahasa Jepang atau aplikasi lain yang berhubungan dengan kanji


#### **Saran Pengembangan Lebih Lanjut**
- **Menggunaakn Dataset yang lebih besar :** Menggunakan dataset yang lebih besar dan lebih representatif meningkatkan akurasi dan generalisasi hasil analisis

- **Menambahkan variabel lain :** Menambahkan variabel lain seperti radikal kanji atau jenis kata (kata benda, kata kerja, dll) dapat memberikan wawasan yang lebih mendalam tentang penggunaan kanji

- **Membuat model prediksi yang lebih kompleks :** Mengembangkan model machine learning yang lebih kompleks (misalnya, model pohon keputusan atau jaringan saraf) dapat meningkatkan akurasi prediksi frekuensi penggunaan kanji