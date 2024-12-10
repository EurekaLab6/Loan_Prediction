# Loan Prediction Based on Customer Behavior

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
