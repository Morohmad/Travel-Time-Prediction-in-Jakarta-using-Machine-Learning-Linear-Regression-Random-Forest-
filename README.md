# Prediksi Harga Rumah Menggunakan Machine Learning

## Deskripsi Proyek

Proyek ini dibuat dalam rangka mengikuti **Kompetisi Machine Learning Yandex x Komdigi Digital Talent Scholarship (DTS) 2025** yang diselenggarakan oleh **Yandex** bekerja sama dengan **Kementerian Komunikasi dan Digital Republik Indonesia (Komdigi)**.

Tujuan proyek ini adalah membangun model machine learning untuk memprediksi **harga rumah (house price prediction)** berdasarkan karakteristik properti yang tersedia pada dataset.

---

## Tujuan

* Melakukan eksplorasi dan analisis data properti.
* Melakukan pembersihan dan praproses data.
* Membangun model prediksi harga rumah.
* Membandingkan performa algoritma Linear Regression dan Random Forest Regression.
* Menghasilkan prediksi harga rumah pada data uji.

---

## Dataset

Dataset terdiri dari data properti untuk pelatihan dan pengujian model.

### File Dataset

* `train_sample.csv.csv` → Data pelatihan
* `test_sample.csv.csv` → Data pengujian

### Variabel Target

| Variabel | Keterangan                       |
| -------- | -------------------------------- |
| `price`  | Harga rumah yang akan diprediksi |

### Variabel Fitur

| Variabel     | Keterangan                     |
| ------------ | ------------------------------ |
| `sold_date`  | Tanggal penjualan properti     |
| `sold_price` | Harga jual sebelumnya          |
| `year_built` | Tahun pembangunan rumah        |
| `garage`     | Jumlah garasi                  |
| `sqft`       | Luas bangunan (square feet)    |
| `type`       | Jenis properti                 |
| `transport`  | Akses transportasi             |
| `services`   | Ketersediaan layanan/fasilitas |
| `beds`       | Jumlah kamar tidur             |
| `floors`     | Jumlah lantai                  |
| `baths`      | Jumlah kamar mandi             |
| `lot_sqft`   | Luas tanah (square feet)       |

---

## Tahapan Pengerjaan

### 1. Data Understanding

Melakukan pemeriksaan struktur data, tipe data, serta identifikasi nilai yang hilang (missing values).

### 2. Data Cleaning

Tahap pembersihan data meliputi:

* Menangani missing values.
* Menghapus data yang tidak relevan.
* Memastikan format data sesuai untuk pemodelan.

### 3. Exploratory Data Analysis (EDA)

Analisis dilakukan untuk memahami pola data melalui:

* Visualisasi hubungan luas bangunan terhadap harga rumah.
* Distribusi jumlah kamar tidur.
* Identifikasi outlier menggunakan boxplot.

### 4. Penanganan Outlier

Data dengan jumlah kamar tidur yang sangat ekstrem dihapus untuk mengurangi pengaruh outlier terhadap model.

### 5. Feature Engineering

#### Encoding Variabel Kategorikal

Variabel kategorikal diubah menjadi numerik menggunakan teknik **One-Hot Encoding**.

#### Normalisasi Data

Fitur numerik dinormalisasi menggunakan **MinMaxScaler** agar berada pada rentang yang seragam.

### 6. Pelatihan Model

Dua algoritma regresi digunakan:

#### Linear Regression

Digunakan sebagai model dasar untuk mempelajari hubungan linier antara fitur dan harga rumah.

#### Random Forest Regression

Metode ensemble berbasis kumpulan decision tree yang mampu menangani hubungan nonlinier dan meningkatkan akurasi prediksi.

---

## Alur Kerja

```text
Data Understanding
        ↓
Data Cleaning
        ↓
Exploratory Data Analysis
        ↓
Penanganan Outlier
        ↓
Encoding & Scaling
        ↓
Training Model
        ↓
Evaluasi Model
        ↓
Prediksi Data Uji
```

---

## Metode Evaluasi

Kinerja model dievaluasi menggunakan:

* Mean Absolute Error (MAE)
* Mean Squared Error (MSE)
* Root Mean Squared Error (RMSE)

Metrik tersebut digunakan untuk mengukur seberapa dekat hasil prediksi terhadap nilai sebenarnya.

---

## Teknologi yang Digunakan

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* Jupyter Notebook

---

## Struktur Proyek

```text
.
├── train_sample.csv.csv
├── test_sample.csv.csv
├── upload.ipynb
├── submission.csv
├── submission1.csv
└── README.md
```

---

## Hasil

Model machine learning berhasil digunakan untuk memprediksi harga rumah berdasarkan karakteristik properti seperti luas bangunan, jumlah kamar tidur, jumlah kamar mandi, luas tanah, dan fitur lainnya.

Perbandingan antara Linear Regression dan Random Forest Regression dilakukan untuk mengetahui model yang memberikan performa terbaik pada dataset yang digunakan.

---

## Penulis

**Mohammad Rohmad Nurkhoirofiq**
