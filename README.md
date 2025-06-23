Nama  : Raja Naufal Fadhil Ns

NIM   : 2306020

# UAS - Kecerdasan Buatan: Deteksi Pesan Spam dengan CNN

Repositori ini merupakan hasil pengerjaan **Ujian Akhir Semester** mata kuliah **Kecerdasan Buatan** yang berfokus pada penerapan **Deep Learning**, khususnya **Convolutional Neural Network (CNN)**, dalam mendeteksi pesan **spam** pada data teks.

---

## Tujuan Proyek

- Membangun sistem klasifikasi teks berbasis CNN
- Mendeteksi dan mengklasifikasikan pesan sebagai **spam** atau **non-spam (ham)**
- Mengevaluasi performa CNN dalam domain teks dengan dataset sederhana

## Langkah-Langkah Pengerjaan

### 1. Import Library
- Menggunakan pustaka:
  - `pandas`, `numpy`, `matplotlib`
  - `sklearn` untuk pemrosesan label dan pembagian data
  - `tensorflow.keras` untuk membangun model

### 2. Load Dataset
- Dataset `spam.csv` dimuat menggunakan `pandas`
- Label dikonversi menjadi nilai numerik:
  - `spam` = 1
  - `ham` = 0
- Fitur dan label dipisahkan untuk proses pelatihan

### 3. Preprocessing Teks
- Membersihkan teks dari karakter tidak penting
- Tokenisasi menggunakan `Tokenizer`
- Padding untuk menyeragamkan panjang input teks

### 4. Membangun Model CNN
- **Layer-layer:**
  - `Embedding` untuk representasi kata
  - `Conv1D` untuk ekstraksi fitur
  - `MaxPooling1D` untuk mengurangi dimensi
  - `Flatten` dan `Dense` untuk klasifikasi
- Fungsi aktivasi akhir: `sigmoid` untuk binary classification

### 5. Training Model
- Menggunakan:
  - **Loss Function:** `binary_crossentropy`
  - **Optimizer:** `Adam`
- Model divalidasi dengan data validasi (20% dari data training)

### 6. Evaluasi
- Visualisasi grafik akurasi dan loss selama training
- Model disimpan dalam format `.h5`

### 7. Pengujian
- Model diuji pada data uji
- Performa dicek berdasarkan metrik akurasi

---

## Alasan Menggunakan CNN

CNN efektif dalam menangkap pola spasial dalam data teks setelah proses embedding. CNN juga lebih efisien dan cepat dibanding RNN untuk teks pendek seperti SMS, serta menunjukkan performa yang baik dalam tugas klasifikasi.

---

## Hasil Model

- **Akurasi Training:** ~98%
- **Akurasi Validasi:** >97%
- Model menunjukkan hasil yang sangat baik dalam membedakan pesan spam dan non-spam

---

## Kesimpulan

Model CNN berhasil digunakan untuk mendeteksi spam. Dengan preprocessing teks yang baik dan arsitektur yang sesuai, model memberikan hasil klasifikasi yang akurat dan efisien.

---

