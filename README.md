🧠 Credit Risk Prediction — Predicting Loan Default Using Machine Learning
📋 Project Overview

Proyek ini bertujuan untuk memprediksi risiko gagal bayar nasabah kredit dengan memanfaatkan data historis pinjaman, demografi, dan status keuangan nasabah.
Dengan model prediksi yang akurat, lembaga keuangan dapat:

- Mengidentifikasi calon nasabah berisiko tinggi
- Mengurangi potensi kerugian finansial
- Mengoptimalkan proses penilaian kredit secara data-driven
  
Dataset yang digunakan berasal dari Kaggle (Credit Risk Dataset) dengan total 32.581 baris dan 12 kolom.

🧾 Problem Statement

Salah satu tantangan utama dalam industri keuangan adalah meningkatnya risiko gagal bayar (default). Berdasarkan data historis:
- Sekitar 21.9% nasabah mengalami gagal bayar, dengan kerugian total mencapai $76,933,675.

Tujuan proyek ini adalah untuk memprediksi secara dini potensi gagal bayar, sehingga perusahaan dapat mengambil langkah preventif seperti:
- Penolakan atau penyesuaian bunga
- Permintaan jaminan tambahan
- Penerapan kebijakan kredit berbasis risiko

🎯 Objectives

1. Mengidentifikasi faktor-faktor yang memengaruhi risiko gagal bayar.
2. Membangun model prediksi berbasis machine learning yang akurat dan dapat diinterpretasikan.
3. Memberikan insight yang membantu tim analis kredit dalam pengambilan keputusan berbasis data.

🧹 Data Preprocessing

Langkah-langkah yang dilakukan pada tahap data preparation:
- Handling missing values dengan imputasi median
- Drop duplicate records (99.49%)
- Outlier handling menggunakan metode IQR
- Encoding untuk variabel kategorikal
- Scaling fitur numerik
- Split dataset menjadi train dan test (80:20)

📊 Exploratory Data Analysis (EDA)

Beberapa temuan utama:
- Loan Grade G memiliki tingkat gagal bayar tertinggi (98.4%)
- Loan Grade D menyumbang kerugian terbesar ($22.7 juta)
- Nasabah usia muda (18–35 tahun) dan pendapatan menengah ($25K–75K) memiliki risiko gagal bayar signifikan
- Pinjaman kecil (< $10K) tetap membawa risiko tinggi karena volumenya besar

🤖 Model Development

Model yang diuji:
- Logistic Regression
- Random Forest
- XGBoost
- KNN
- Decision Tree
- LightGBM

Hasil menunjukkan bahwa XGBoost memberikan performa terbaik:

Metric	Value
F1-Score	0.8412
ROC-AUC	0.9472

Upaya hyperparameter tuning dan SMOTE balancing tidak meningkatkan performa, sehingga digunakan model dasar terbaik.

📈 Feature Importance

Fitur paling berpengaruh terhadap prediksi gagal bayar:
1. loan_grade
2. person_income
3. loan_percent_income

✅ Conclusion
- 78.1% nasabah melunasi pinjaman, namun 21.9% gagal bayar tetap menimbulkan kerugian besar.
- Loan Grade D = kerugian tertinggi; Grade G = risiko gagal bayar tertinggi.
- Risiko tinggi juga terlihat pada segmen usia muda & pendapatan menengah.

💡 Recommendations
- Tingkatkan monitoring untuk Loan Grade D.
- Gunakan risk-based pricing berdasarkan total pinjaman dan risiko.
- Implementasi early warning system untuk deteksi dini potensi gagal bayar.

🛠️ Tech Stack
- Python
- Pandas, NumPy, Scikit-learn, XGBoost, Matplotlib, Seaborn
- Visual Studio Code
