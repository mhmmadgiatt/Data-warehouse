# Pembangunan Data warehouse Merger Philip Morris Internasional dan Altria 

## Deskripsi

Pemanfaatan Data Warehouse dalam pemanfaatan bisnis sangatlah memiliki dampak positif bagi banyak perusahaan. Gudang
data/Data warehouse membentuk sebuah sistem yang bertugas mengarsipkan sekaligus melakukan analisis data historis untuk
menunjang keperluan informasi pada sebuah bisnis maupun organisasi. Dengan dibentuknya Data Warehouse, pihak bisnis/organisasi
dapat lebih mudah membuat suatu keputusan atau menganalisis keadaan organisasi dikarenakan Data Warehouse dapat membentuk
pengetahuan yang penting dimanfaatkan dalam aspek organisasi (Business Intelligence). Philip Morris International dan Altria adalah
dua perusahaan rokok yang cukup besar pada industri rokok. Pada tahun 2019, kedua perusahaan ini melakukan merger atau
penggabungan dibawah nama Phillip Morris Tentu dalam proses merger dari dua perusahaan ini, terdapat penggabungan banyak
komponen salah satunya adalah data yang menjadi poin penting pada setiap bisnis. Penelitian ini memiliki tujuan untuk membuat
Skema rancangan Data Warehouse bagi kedua perusahaan ini menggunakan Skema Star. Dengan pembentukan Skema Star,
diharapkan Philip Morris International dapat memiliki pengetahuan akan transaksi, kapasitas gudang dan pabriki, dan hubungan
transaksi dan gudang terhadap penjualan dan kapasitas sehingga dapat memberikan pengetahuan akan logistik, penyebaran, dan
penjualan Phillip Morris International.
## Tahapan Proyek

#### Proses Pengumpulan dan pengolahan data
- Laporan tahunan Philip Morris International 2022
- Laporan tahunan Altria 2022
- Laporan operasional Philip Morris International 2022
- Laporan operasional Altria 2022
- Laporan keuangan Philip Morris International Q4 2022
- Laporan keuangan Altria 2022

#### Data Cleaning
- Penghapusan Data Duplikat
1. Melakukan pengecekan data duplikat pada setiap tabel menggunakan metode duplicated() pada library Pandas.
2. Menghapus baris-baris yang merupakan data duplikat dari setiap tabel menggunakan metode drop_duplicates().

- Penanganan Missing Value
1. Melakukan pengecekan missing value atau data yang hilang pada setiap tabel menggunakan metode isnull().sum().
2. Menghapus baris-baris yang mengandung missing value dari setiap tabel menggunakan metode dropna().

- Penyeragaman Nama Kolom
1. Mengubah nama kolom pada tabel tertentu agar seragam dengan menggunakan metode rename().

#### Data Integration
- Data dari Philip Morris International dan Altria Group, Inc. Melakukan penggabungan data dari Philip Morris International dan Altria Group, Inc. untuk tabel Gudang, Pabrik, dan Transaksi menggunakan operasiconcat() pada library Pandas.
- Hasil dari proses ini adalah tiga tabel baru yang mencakup data dari kedua perusahaan, yaitu **gudang_df, pabrik_df, dan transaksi_df**.

#### Data Transformation
- Pencarian Transaksi Terbesar dan Terkecil di
Gudang
- Pencarian Kapasitas Gudang Terbesar, Terkecil,
dan Rata-rata
- Pencarian Jumlah Produksi Terbesar, Terkecil,
dan Rata-rata di Pabrik
- Konversi Satuan Ton menjadi Kilogram
- Konversi Mata Uang (USD ke IDR) pada Tabel
Transaksi.

#### Skema Star
![Skema Data Warehouse](https://github.com/mhmmadgiatt/Data-warehouse/blob/main/Skema%20Star.jpg)