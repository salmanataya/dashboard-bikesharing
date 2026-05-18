# Bike Sharing Data Analysis Dashboard

## Deskripsi Proyek

Proyek ini bertujuan untuk menganalisis pola penggunaan layanan bike sharing berdasarkan faktor waktu, cuaca, dan tipe pengguna menggunakan dataset Bike Sharing Dataset tahun 2011–2012.

Analisis dilakukan untuk mengeksplorasi:
- Pola peminjaman sepeda berdasarkan jam
- Perbedaan penggunaan pada hari kerja dan akhir pekan
- Pengaruh kondisi cuaca terhadap jumlah peminjaman
- Proporsi pengguna casual dan registered

Dashboard interaktif dibuat menggunakan Streamlit untuk mempermudah eksplorasi data dan visualisasi insight.

---

## Struktur Direktori

submission

├── dashboard

│   ├── dashboard.py

│   ├── day.csv

│   └── hour_full.csv

├── data

│   ├── day.csv

│   └── hour.csv

├── notebook.ipynb

├── README.md

└── requirements.txt

---

## Business Questions

1. Pada pukul berapa rata-rata jumlah peminjaman sepeda mencapai titik tertinggi dalam satu hari selama periode 2011–2012 sehingga dapat digunakan untuk mengidentifikasi jam operasional dengan permintaan tertinggi?
2. Bagaimana perbedaan pola rata-rata peminjaman sepeda antara hari kerja (Senin–Jumat) dan akhir pekan (Sabtu–Minggu) selama periode 2011–2012 untuk memahami perubahan perilaku penggunaan sepeda berdasarkan jenis hari?
3. Bagaimana pola rata-rata jumlah peminjaman sepeda pada setiap bulan selama periode 2011–2012 untuk mengidentifikasi bulan dengan tingkat penggunaan tertinggi dan terendah?
4. Seberapa besar perbedaan rata-rata jumlah peminjaman sepeda per jam berdasarkan kondisi cuaca selama periode 2011–2012, serta bagaimana pengaruh kondisi cuaca terhadap tingkat penggunaan layanan bike sharing?
5. Bagaimana proporsi peminjaman sepeda per jam antara pengguna *casual* dan *registered* selama periode 2011–2012 untuk mengidentifikasi karakteristik dan pola penggunaan dari masing-masing tipe pengguna?

---

## Analisis Lanjutan
1. Hourly Demand Segmentation Analysis
   Analisis ini bertujuan mengelompokkan jam operasional berdasarkan tingkat permintaan peminjaman sepeda untuk membantu optimalisasi operasional layanan. Analisis dilakukan dengan menghitung rata-rata jumlah peminjaman sepeda (`cnt`) pada setiap jam selama periode 2011–2012. Selanjutnya, dilakukan segmentasi tingkat permintaan menggunakan pendekatan berbasis quantile menjadi tiga kategori, yaitu
   - Low Demand,
   - - Medium Demand, dan
     - - High Demand.
2. Weather Sensitivity Analysis
   Analisis ini bertujuan mengukur seberapa sensitif penggunaan bike sharing terhadap perubahan kondisi cuaca. Analisis dilakukan dengan menghitung rata-rata jumlah peminjaman sepeda (`cnt`) pada setiap kategori kondisi cuaca. Selanjutnya, dihitung persentase penurunan penggunaan layanan pada kondisi cuaca tertentu dibandingkan kondisi cuaca cerah sebagai baseline utama. Persentase penurunan dihitung menggunakan rumus $$\frac{Mean Clear−Mean Cuaca Tertentu}{Mean Clear} \times 100%.$$

---

## Data Preparation
Tahapan persiapan data yang dilakukan meliputi:
1. Pemeriksaan missing values
2. Pemeriksaan duplicate data
3. Pemeriksaan invalid dan inconsistent values
4. Pemeriksaan outlier menggunakan metode IQR
5. Pemeriksaan kelengkapan data waktu pada dataset harian dan per jam
Hasil analisis prapemrosan menunjukkan bahwa secara umum kualitas data sudah baik dan layak digunakan untuk analisis eksploratif dan visualisasi.

---

## Tools and Libraries
Proyek ini menggunakan beberapa library Python berikut:
1. Pandas
2. NumPy
3. Matplotlib
4. Seaborn
5. Streamlit

---

## Main Insights
1. Pola peminjaman sepeda menunjukkan adanya jam-jam sibuk tertentu yang berkaitan dengan aktivitas harian pengguna.
2. Pengguna registered mendominasi jumlah peminjaman dibandingkan pengguna casual.
3. Kondisi cuaca memengaruhi jumlah peminjaman sepeda.
4. Terdapat perbedaan pola penggunaan antara hari kerja dan akhir pekan.
