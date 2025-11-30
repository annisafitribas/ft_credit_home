# Credit Scoring Optimization -- Final Project

Proyek ini bertujuan untuk membangun dan mengevaluasi model credit
scoring menggunakan data dari Home Credit. Fokus utamanya adalah
meningkatkan kemampuan model dalam memprediksi pelanggan yang berpotensi
gagal bayar sehingga keputusan pemberian pinjaman dapat lebih akurat dan
adil.

## Tujuan Proyek
1.  Memprediksi apakah seorang peminjam akan melakukan default atau
    tidak.
2.  Menggunakan kombinasi metode statistik dan Machine Learning.
3.  Meningkatkan akurasi dan AUC dibanding baseline.
4.  Memastikan peminjam yang layak tidak ditolak, serta mengurangi
    risiko finansial perusahaan.

## Struktur Folder
    ├── data/
    │   ├── application_train.csv
    │   ├── application_test.csv
    │   └── descriptions.csv
    ├── notebook/
    │   └── credit_scoring.ipynb
    ├── models/
    │   ├── model_xgboost.pkl
    │   ├── model_lightgbm.txt
    │   └── scaler.pkl
    ├── submissions/
    │   └── submission.csv
    └── README.md

## Teknologi & Tools
-   Python
-   Pandas, NumPy
-   Scikit-learn
-   XGBoost
-   LightGBM
-   Matplotlib & Seaborn
-   Jupyter Notebook


## Tahapan Proyek

### 1. Exploratory Data Analysis (EDA)
-   Memeriksa distribusi fitur numerik & kategorik
-   Missing values
-   Korelasi terhadap target
-   Visualisasi

### 2. Data Cleaning & Preprocessing
-   Missing value handling
-   Encoding
-   Normalisasi
-   SMOTE / class_weight

### 3. Feature Engineering
-   Debt Ratio
-   Income per Family Member
-   Credit/Income ratio
-   Days employed ratio
-   Age bucket

### 4. Model Training
Model diuji: - Logistic Regression - Random Forest - XGBoost - LightGBM

## Hasil Evaluasi
  Model                 AUC Score      Accuracy
  --------------------- -------------- ----------
  Logistic Regression   0.69           0.72
  Random Forest         0.74           0.79
  XGBoost               0.78           0.82
  LightGBM              0.79 -- 0.81   0.83

## Submission
    SK_ID_CURR,PREDICTED_PROB
    100001,0.03921
    100005,0.19283
    100013,0.00823

## Kesimpulan
-   LightGBM terbaik berdasarkan AUC.
-   Feature engineering sangat berpengaruh.
-   Model membantu mengurangi risiko dan meningkatkan akurasi credit
    scoring.

## Penulis
An Nisa Fitri
