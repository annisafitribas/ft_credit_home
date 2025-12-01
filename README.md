# HOME CREDIT INDONESIA
Proyek ini bertujuan untuk membangun model machine learning yang dapat memprediksi apakah sebuah pengajuan kredit rumah (home credit) akan **disetujui** atau **ditolak** berdasarkan fitur-fitur calon peminjam. Model ini membantu perusahaan meningkatkan efisiensi proses underwriting dan menargetkan segmen nasabah yang paling potensial.
            
## 1. Problem yang Ingin Diselesaikan
Perusahaan ingin mengetahui **probabilitas persetujuan kredit** sejak awal proses pengajuan.  
Dengan model prediksi ini, perusahaan dapat:

- Menurunkan risiko kredit macet  
- Mempercepat proses penilaian pengajuan  
- Mengoptimalkan strategi pemasaran  
- Mendeteksi calon nasabah yang berpotensi memenuhi kriteria bank  

## 2. Dataset yang Digunakan
Dataset terdiri dari berbagai informasi terkait nasabah dan pengajuan kredit:

### **Kategori Data**
- **Data Demografis**: usia, status pernikahan, jumlah tanggungan  
- **Data Finansial**: pendapatan, total hutang, kewajiban bulanan  
- **Riwayat Kredit**: keterlambatan pembayaran, active loan  
- **Data Pengajuan**: tujuan kredit, besar pinjaman, lama tenor  
- **Target**: `Approved` atau `Rejected`

Dataset telah melalui proses pembersihan (handling NaN, encoding, scaling).

## 3. Insights Utama dari Data
### **Insight 1 — Nasabah PNS (Pegawai Negeri Sipil) memiliki approval rate tertinggi: 75%**
Namun jumlah pengajuan dari PNS hanya **12%** dari total aplikasi.
**Rekomendasi Aksi:**  
Buat campaign khusus untuk PNS karena mereka adalah segmen yang:
- Risiko gagal bayar rendah  
- Approval rate tinggi  
- Potensi meningkatkan profit perusahaan  

### **Insight 2 — Pendapatan Bulanan > 8 Juta memiliki probabilitas persetujuan 2x lebih tinggi**
Namun hanya 28% nasabah berada dalam kategori ini.
**Rekomendasi Aksi:**  
- Buat produk “Premium Fast Approval” untuk nasabah dengan pendapatan tinggi  
- Optimalkan channel digital targeting high-income users  

## 4. Model & Machine Learning Pipeline
Bagian ini menjelaskan **model final** tanpa masuk ke detail eksperimen.
### **Features yang Digunakan**
Model menggunakan kombinasi:
- **Numerical features**: Income, Loan Amount, Debt Ratio, Age, etc  
- **Categorical features**: Employment Type, Marital Status, Purpose  
- **Derived features**:  
  - Debt-to-Income Ratio  
  - Payment Reliability Score  
  - Age Group Encoding  

### **Preprocessing yang Dilakukan**
- Handling missing values (median & mode)  
- Encoding kategori (One-Hot Encoding)  
- Scaling numerik (StandardScaler)  
- Train-test split (80:20)  
- SMOTE untuk menangani imbalance data  
- Feature selection dengan Random Forest Importance  

### **Algoritma Machine Learning**
Model final: **XGBoost Classifier**
Dipilih karena:
- Akurat  
- Tahan terhadap data imbalance  
- Cepat  
- Mendukung interpretasi feature importance  

### **Performance Model**
| Metric | Score |
|--------|-------|
| Accuracy | **0.87** |
| Precision | **0.85** |
| Recall | **0.82** |
| F1-score | **0.83** |
| ROC-AUC | **0.91** |

## 5. Cara Menjalankan Proyek
### **1. Clone Repository**
bash
git clone https://github.com/annisafitribas/ft_credit_home
cd ft_credit_home

## Struktur Folder
ft_credit_home/
│── notebook.ipynb
│── README.md

## 6. Referensi
- Home Credit Default Risk Dataset  
- XGBoost Documentation  
- SMOTE Oversampling Techniques  
- scikit-learn preprocessing & pipeline  

## GitHub Repo
https://github.com/annisafitribas/ft_credit_home

## Link Google Drive
https://drive.google.com/drive/folders/12DLaKNhiffq7fKSwScaaVLs6lQqh32h4?usp=sharing

## Author
An Nisa Fitri — Data Science Project  
