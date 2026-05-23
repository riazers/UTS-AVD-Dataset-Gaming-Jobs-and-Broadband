# Laporan UTS-AVD-Dataset-Gaming-Jobs-and-Broadban

*Overview:*

Repositori ini berisi proyek analisis data berbasis Python yang mengeksplorasi korelasi dan pola antara akses broadband, kebiasaan bermain game (gaming), dan dinamika pekerjaan/karier di Amerika Serikat pada pertengahan tahun 2015. Proyek ini dibuat sebagai Ujian Tengah Semester (UTS).

---

## Daftar Isi:

* Business Understanding
* Tentang Dataset
* Metodologi / Alur Kerja
* Key Findings (Temuan Utama)
* Tech Stack
* Cara Menjalankan

## (I) Business Understanding
### Latar Belakang & Tujuan Utama
Pada pertengahan tahun 2015, industri gaming berkembang pesat, penetrasi smartphone meluas, dan konektivitas internet (broadband) mulai dianggap sebagai kebutuhan dasar, baik untuk hiburan maupun dunia kerja. Tujuan utama dari analisis ini adalah memahami korelasi dan pola antara akses broadband, kebiasaan bermain game, dan dinamika pekerjaan/karier di Amerika Serikat.

## Nilai Bisnis
### Hasil analisis ini dapat dimanfaatkan oleh berbagai pemangku kepentingan
Perusahaan Telekomunikasi/ISP: Menyusun paket broadband yang disesuaikan dengan kebutuhan gamer dan pekerja remote.
Industri Gaming & Teknologi: Memetakan profil demografi gamer dan bagaimana gaming berinteraksi dengan aktivitas kerja mereka.
Pembuat Kebijakan (Pemerintah): Menilai dampak "kesenjangan digital" (digital divide) terhadap peluang kerja dan akses hiburan.

## Analytic Goals
* Segmentasi Profil Gamer: Mengidentifikasi karakteristik demografi dan infrastruktur dari segmen casual vs hardcore gamer (Clustering/Segmentation).
* Analisis Digital Divide & Pekerjaan: Mengidentifikasi perbedaan signifikan dalam status pekerjaan antara mereka yang memiliki akses broadband di rumah dibandingkan yang tidak.
* Interaksi Gaming dan Produktivitas: Melihat korelasi antara frekuensi bermain game dengan persepsi dampak otomatisasi di tempat kerja.
* Predictive Modeling (Opsional): Memprediksi kelompok pendapatan tinggi berdasarkan pola penggunaan internet dan kebiasaan gaming.

## (II) Tentang Dataset
* Sumber: Survei nasional di Amerika Serikat (Pew Research Center).
* Waktu Survei: 10 Juni - 12 Juli 2015.
* Tipe Data: Cross-sectional (potret sesaat) dengan variabel yang kaya (demografi, infrastruktur internet, perilaku gaming, status pekerjaan).
* Pembobotan: Terdapat kolom weight dan standwt yang menunjukkan data survei perlu diboboti (weighted) agar mewakili populasi nasional secara akurat.

### Tantangan & Risiko Data
* Usia Data (Data Decay): Lanskap broadband dan gaming telah berubah drastis sejak 2015. Insight bersifat historis.
* Kualitas Data & Missing Values: Terdapat banyak nilai kosong dan kode numerik skip logic (misal: 8, 9, 99 untuk "Tidak Tahu/Menolak").
* Bias Respons: Survei cenderung memiliki bias terhadap kelompok demografi tertentu.

## (III) Metodologi / Alur Kerja
Analisis dalam notebook dilakukan dengan alur kerja berikut:

1. Import Library & Load DataMengimpor library utama (pandas, numpy, matplotlib, seaborn) dan memuat dataset.
2. Exploratory Data Analysis (EDA)
    * Comparison: Perbandingan akses broadband berdasarkan tingkat pendapatan (Stacked Bar Chart).
    * Composition: Komposisi kepemilikan smartphone responden (Pie Chart).
    * Distribution: Distribusi umur responden (Histogram & KDE).
    * Relationship: Korelasi antar variabel numerik demografi (Heatmap).
3. Data Preprocessing
    * Pengecekan tipe data dan struktur dataset.
    * Parsing tanggal (int_date) menjadi format Datetime standar serta ekstraksi fitur tahun, bulan, dan hari.
4. Statistik Deskriptif & Missing Value Analysis
    * Analisis statistik dasar variabel numerik (weight, standwt, index).
    * Identifikasi jumlah dan persentase missing values per kolom.
5. Distribusi Fitur Demografis Utama
    * Distribusi Umur (Numerik Diskrit).
    * Distribusi Jenis Kelamin (Kategorikal).
    * Distribusi Tingkat Pendidikan (Kategorikal Ordinal).
    * Distribusi Pendapatan (Kategorikal Ordinal).
6. Analisis Inti: Internet & Broadband
    * Visualisasi proporsi pengguna vs non-pengguna internet.
7. Analisis Inti: Perilaku Gaming
    * Proporsi Gamer vs Non-Gamer.
    * Distribusi umur berdasarkan status gamer (Boxplot).
    * Proporsi gamer berdasarkan jenis kelamin (Stacked Bar Chart).

## (IV) Key Findings (Temuan Utama)
Berdasarkan analisis yang telah dilakukan, berikut adalah temuan-temuan utama:

1. Akses Broadband & Ekonomi: Terdapat keterkaitan antara kondisi ekonomi dan akses teknologi. Semakin tinggi tingkat pendapatan seseorang, semakin tinggi pula persentase kepemilikan akses broadband di rumah mereka.
2. Proporsi Gamer: Sebagian besar responden pada tahun 2015 teridentifikasi sebagai Non-Gamer, meskipun terdapat proporsi yang signifikan sebagai Gamer.
3. Distribusi Umur Gamer: Kelompok Gamer cenderung memiliki median usia yang lebih muda dibandingkan Non-Gamer, meskipun aktivitas gaming dijangkau oleh berbagai rentang usia.
4. Gaming & Jenis Kelamin: Pada tahun 2015, proporsi Gamer dan Non-Gamer cukup seimbang antara responden laki-laki dan perempuan. Tidak ada perbedaan yang signifikan dalam persentase Gamer antara kedua jenis kelamin.

## (V) Tech Stack
* Bahasa Pemrograman: Python 3
* Library Utama:
    * pandas (Manipulasi dan analisis data)
    * numpy (Komputasi numerik)
    * matplotlib & seaborn (Visualisasi data)
* Environment: Google Colaboratory / Jupyter Notebook

## (VI) Cara Menjalankan

1. Pastikan Anda memiliki environment Python dengan library yang dibutuhkan:
> pip install pandas numpy matplotlib seaborn

2. Unduh dataset 2015 Gaming Jobs and Broadband.csv dan sesuaikan path pembacaan file di dalam notebook jika diperlukan:
> df = pd.read_csv("/content/drive/MyDrive/UTS AVD MATKUL/2015 Gaming Jobs and Broadband.csv")
Disesuaikan dengan dimana directory file tersebut berada.

3. Buka dan jalankan file uts_avd_gaming_jobs_and_broadband.py atau konversi ke format .ipynb untuk pengalaman interaktif di Jupyter Notebook / Google Colab.
   
