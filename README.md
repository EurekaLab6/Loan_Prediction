# Loan Prediction Based on Customer Behavior

- Build a model to help the creditor team to filter potential customers and prevent defaults.
- Extraction feature to optimizing the learning process of model
- Train model with 5 different algorithms, and choose 1 for next hyperparameter tuning
- Handle imbalanced class with Combining oversampling and undersampling (hybrid techniques)

# Problems
- In this case, **the acceptable default threshold is 5% based on Bank Indonesia Circular Letter No 6/23/DPNP 2004**, but in reality, **the default rate recorded reached 12.3%**.

# Purpose
reduce the default rate to 5% based on the threshold that has been set

# Exploratory Data Analysis
   1. Distributin City of Risk Flag
    ![1](https://github.com/user-attachments/assets/f3ff4bb1-cdaf-41a3-97b3-d9f63e83ad33)

   2. Distribution income of Risk Flag
    ![2](https://github.com/user-attachments/assets/dc5ea1b6-e37d-49b0-bfdb-9f5eba8c287b)

   3. Distribution Age of Risk Flag
    ![3](https://github.com/user-attachments/assets/722c51aa-788f-43e9-9ed8-cc4a24680764)

   4. Distribution Profession of Risk FLag
    ![4](https://github.com/user-attachments/assets/fafbc925-8e25-43ea-89eb-f6a7f6555707)

   5. Distribution Experience of Risk Flag
    ![5](https://github.com/user-attachments/assets/7a0882be-ffaf-44ed-9eb2-ae2489949589)

## Dataset
- **Id:** Identitas user (object)
- **Income:** Penghasilan tiap bulan Mata uang Rupee (float)
- **Age:** Umur Customer
- **Experience:** Pengalaman Kerja Customer secara keseluruhan
- **Married/Single:**
    - **Single:** Belum Menikah
    - **Married:** Sudah Menikah
- **House_Ownership:**
    - **Rented:** Menyewa
    - **Owned:** Rumah pribadi
    - **Norent_noown:** Homeless
- **Car_Ownership:**
    - **Yes:** Punya Mobil
    - **No:** Tidak Punya Mobil
- **Profession:** Profesi user (obj)
- **City:** Kota user (obj)
- **State:** Negara Bagian (obj)
- **Current_Job_Yrs:** Masa kerja saat ini (int)
- **Current_House_Yrs:** Status kepemilikan rumah dalam tahun (int)
- **Risk_Flag (Target):**
    - **0:** Potensial gagal bayar rendah
    - **1:** Potensial gagal bayar tinggi
 
## Summary of EDA
Dataset Loan Prediction digunakan untuk mengidentifikasi pola gagal bayar. Hasil analisis menunjukkan bahwa kreditur dengan status single, tanpa aset, berpenghasilan rendah, atau memiliki pengalaman kerja terbatas memiliki risiko gagal bayar tertinggi. Profesi tertentu, seperti polisi, dan lokasi domisili, seperti Kota Bhubaneswar dan negara bagian Manipur, juga menjadi faktor signifikan. Berdasarkan temuan ini, kami merekomendasikan pengembangan kategori pinjaman fleksibel berdasarkan kelas ekonomi kreditur, pelatihan literasi keuangan, dan kerja sama dengan institusi lokal untuk meminimalkan risiko gagal bayar. Selain itu, penyesuaian batas kredit, suku bunga, serta dukungan berbasis komunitas diusulkan untuk meningkatkan keberhasilan program pinjaman.


## Instalasi

Ikuti langkah-langkah berikut untuk menjalankan proyek ini:
- **Clone Repository:**
git clone https://github.com/EurekaLab6/Loan_Prediction.git
- **Streamlit App:**
[Streamlit](https://final-riskmodelapp-eurekalab.streamlit.app/)
