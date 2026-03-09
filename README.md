# ✈️ Tourism Prediction: Prediksi Kunjungan Wisatawan Mancanegara (BPS Data)

Proyek ini bertujuan untuk memprediksi jumlah kunjungan wisatawan mancanegara (wisman) ke Indonesia berdasarkan pintu masuk utama menggunakan pendekatan **CRISP-DM (Cross-Industry Standard Process for Data Mining)**. Penelitian ini membandingkan pola kunjungan pada periode pra-pandemi dan pasca-pandemi untuk memberikan wawasan strategis bagi sektor pariwisata.

## 📌 1. Business Understanding
Data kunjungan wisman merupakan indikator utama untuk mengukur kinerja industri pariwisata. Informasi ini penting untuk perencanaan strategis, promosi, dan alokasi sumber daya.

* **Tujuan**:
    * Memprediksi jumlah kunjungan wisatawan di tiap pintu masuk (udara, laut, darat).
    * Menganalisis perubahan jumlah kunjungan sebelum dan sesudah pandemi.
    * Memberikan gambaran visual dan numerik terhadap tren kunjungan.
* **Manfaat**:
    * **Pemerintah**: Dasar evaluasi kebijakan pariwisata pascapandemi.
    * **Sektor Industri**: Identifikasi peluang pasar dan strategi pemasaran.

## 📊 2. Data Understanding
* **Sumber Data**: Dataset diperoleh dari [BPS – Jumlah Kunjungan Wisatawan Mancanegara per Bulan](https://www.bps.go.id).
* **Rentang Waktu**:
    * **2010–2019**: Periode Pra-COVID.
    * **2023–2024**: Periode Pasca-COVID.
    * *Catatan*: Tahun 2020–2022 tidak digunakan karena dianggap tidak representatif akibat pembatasan perjalanan global selama pandemi.
* **Struktur Kolom**:
    * `Tanggal`: Format YYYY-MM-DD.
    * `Pintu Masuk`: Lokasi masuk (bandara, pelabuhan, perbatasan).
    * `Jumlah Kunjungan`: Angka numerik wisatawan yang tercatat.

## 🛠️ 3. Data Preparation
Proses pengolahan data meliputi beberapa tahapan kritis:
* **Data Cleaning**: Menghapus entri agregat seperti "A. Pintu Udara", "B. Pintu Laut", "C. Pintu Darat", serta "Total" agar tidak mengganggu akurasi model.
* **Transformasi**:
    * Mengubah format data dari *wide* menjadi *long format*.
    * Mapping nama bulan dari Bahasa Indonesia ke Bahasa Inggris.
    * Konversi kolom menjadi tipe data `datetime` dan numerik.
* **Integrasi**: Menggabungkan seluruh file CSV tahunan menjadi satu dataset tunggal `jumlah_kunjungan_wisman_2010_2024.csv`.

## 🤖 4. Modeling & Evaluation
* **Algoritma**: Proyek ini menggunakan **Random Forest Regressor** untuk melakukan prediksi.
* **Pembagian Data**: Data dibagi menggunakan metode **Train-Test Split** dengan rasio **80:20**.
* **Metrik Evaluasi**: Performa model dievaluasi menggunakan *Mean Absolute Error* (MAE), *Mean Squared Error* (MSE), dan *R-Squared* (R2) Score.

## 🚀 Teknologi yang Digunakan
* **Bahasa**: Python
* **Library**:
    * `pandas` & `numpy` (Manipulasi Data)
    * `matplotlib` & `seaborn` (Visualisasi)
    * `scikit-learn` (Machine Learning)
    * `datetime` & `dateutil` (Pemrosesan Waktu)

---
*README ini disusun berdasarkan dokumentasi proyek pada notebook CRISP_DM_TimeSeries_Skripsi_split80_20.ipynb.*
