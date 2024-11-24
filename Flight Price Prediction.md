# Laporan Proyek Machine Learning - Diajeng Mahai Sukma
## Domain Proyek
[EaseMyTrip](https://www.easemytrip.com/) sebagai Online Travel Agency menghadapi tantangan dalam mengelola harga tiket pesawat yang fluktuatif, yang dapat mempengearuhi pendapatan dan daya saing mereka di pasar. Dengan memanfaatkan prediksi harga yang cerdas, EaseMyTrip dapat menentukan strategi penetapan harga yang lebih efektif, memaksimalkan keuntungan dari setiap transaksi.

## Problem Statement
- Faktor-faktor apa saja yang paling signifikan mempengaruhi fluktuasi harga tiket pesawat?
- Bagaimana prediksi harga dapat meningkatkan konversi penjualan pada platform EaseyMyTrip
- Bagaimana model prediksi harga dapat diintegrasikan untuk menyesuaikan strategi penetapan harga yang mengoptimalkan revenue?

## Goals
- Memahami fakkor-faktor yang mempengaruhi harga tiket pesawat

## Data Understanding
Dataset yang digunakan pada proyek ini diambil dari paltform [Kaggle](https://www.kaggle.com/datasets/shubhambathwal/flight-price-prediction?resource=download&select=Clean_Dataset.csv) yang berisi 300.153 records.Berikut merupakan penjelasan fitur-fitur yang ada di dataset Flight Price Prediction:

- Airline: Nama perusahaan maskapai penerbangan. Variable ini memiliki 6 maskapai penerbangan yang berbeda.
- Flight: Kode penerbangan pesawat. Ini merupakan variable kategorikal.
- Source City: Kota dari mana asal penerbangan. Ini adalah fitur kategorikal yang memiliki 6 kota unik.
- Departure Time: Fitur ini menyimpan informasi mengenai waktu keberangkatan dan memiliki 6 label waktu yang unik.
- Stops: Fitur kategorikal dengan 3 nilai berbeda yang menyimpan jumlah pemberhentian antara kota asal dan kota tujuan.
- Arrival Time: Fitur ini memiliki enam label waktu yang berbeda dan menyimpan informasi tentang waktu kedatangan.
- Destination City: Kota tujuan dari penerbangan. Ini adalah fitur kategorikal yang memiliki 6 kota unik.
- Class: Fitur kategorikal yang berisi informasi tentang kelas kursi; fitur ini memiliki dua nilai yang berbeda: Bisnis dan Ekonomi.
- Duration: Fitur kontinu yang menampilkan jumlah keseluruhan waktu yang dibutuhkan untuk melakukan perjalanan antar kota dalam jam.
- Days Left: Ini adalah karakteristik turunan yang dihitung dengan mengurangi tanggal perjalanan dengan tanggal pemesanan.
- Price: Variabel target menyimpan informasi harga tiket.

Pada tahapan ini dilakukan Exploratory Data Analysis seperti Check Missing Values, Unique Values, Descriptive Statistics, Univariate Analysis, serta Bivariate Analysis yang bertujuan untuk menganalisis karakteristik pada data.

## Data Preparation
Tahap ini merupakan proses transformasi pada data sehingga menjadi bentuk yang cocok untuk proses pemodelan. Ada beberapa tahapan yang dilakukan yaitu:
- Handling Outliers
- Categorical Encoding
- Standardization
- Feature Selection

## Modeling
Dalam proyek ini digunakan model Random Forest karena sebagai model ensemble, Random Forest dapat membantu dalam menangani non-linearitas dan interaksi antar fitur dengan memberikan prediksi yang lebih stabil. Setelah itu dilakukan hyperparameter tuning untuk mencapai kinerja terbaik pada dataset yang digunakan.

## Evaluation
Metrik yang digunakan pada prediksi ini adalah RMSE atau Root Mean Squared Error yang mengukur rata-rata perbedaan antara nilai prediksi model dengan nilai aktual. Selain itu, digunakan juga metrik R-squared atau R2 Score yang menunjukkan seberapa baik model dapat menjelaskan variabilitas dalam data.


## Kesimpulan
Secara keseluruhan, fitur yang paling berpengaruh positif adalah class Economy, Airline Vistara dan days left <= 15.00, sementara duration dan direct flight memberikan pengaruh negatif terhadap prediksi ini. Dan untuk Pola Revenue,
Pola Revenue
- Selama 15 hari sebelum tanggal penerbangan, perusahaan mulai melihat peningkatan yang signifikan dalam revenue. Hal ini menunjukkan bahwa konsumen cenderung melakukan pemesanan lebih banyak menjelang waktu keberangkatan.
- Temuan ini menyiratkan bahwa perusahaan dapat mempertimbangkan untuk mengadopsi strategi pemasaran yang lebih agresif dan promosi pada periode 15 hari menjelang keberangkatan. Ini bisa termasuk penawaran khusus atau diskon untuk mendorong konsumen memesan lebih awal.