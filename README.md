# 🎓 Sistem Prediksi Kelulusan Mahasiswa – MLOps & Streamlit

<p align="center">

**Praktikum Rekayasa Perangkat Lunak (RPL) – Pertemuan 10**

*Machine Learning Model Deployment menggunakan Streamlit*

</p>

---

## 📌 Deskripsi Proyek

Sistem Prediksi Kelulusan Mahasiswa merupakan aplikasi berbasis web yang dikembangkan untuk menerapkan konsep dasar Machine Learning Operations (MLOps) dalam proses pengembangan perangkat lunak.

Aplikasi ini menggunakan algoritma **Decision Tree Classifier** untuk memprediksi status kelulusan mahasiswa berdasarkan dua variabel utama, yaitu Indeks Prestasi Kumulatif (IPK) dan jumlah Satuan Kredit Semester (SKS).

Model Machine Learning dilatih menggunakan Python, kemudian disimpan dalam format `.pkl` menggunakan Joblib. Model tersebut selanjutnya diintegrasikan ke dalam aplikasi web interaktif menggunakan Streamlit sehingga pengguna dapat memasukkan data dan memperoleh hasil prediksi secara langsung.

## 🎯 Tujuan Pengembangan

Proyek ini memiliki beberapa tujuan, yaitu:

1. Memahami proses pelatihan model Machine Learning menggunakan Python.
2. Menerapkan algoritma Decision Tree Classifier untuk klasifikasi kelulusan mahasiswa.
3. Melakukan penyimpanan dan pengelolaan model Machine Learning menggunakan Joblib.
4. Membangun antarmuka pengguna (User Interface) menggunakan Streamlit.
5. Mengimplementasikan konsep pemisahan antara model Machine Learning dan antarmuka aplikasi.
6. Memahami proses deployment sederhana model Machine Learning ke dalam aplikasi berbasis web.

## ⚙️ Teknologi dan Library

| Teknologi | Kegunaan |
|---|---|
| Python | Bahasa pemrograman utama |
| Scikit-learn | Pembuatan dan pelatihan model |
| NumPy | Pengolahan data numerik |
| Pandas | Pengolahan data |
| Joblib | Penyimpanan dan pemanggilan model |
| Streamlit | Pembuatan aplikasi web |

## 🧠 Algoritma Machine Learning

Algoritma yang digunakan dalam proyek ini adalah **Decision Tree Classifier**.

Decision Tree merupakan algoritma klasifikasi yang bekerja dengan membentuk struktur pohon keputusan berdasarkan pola pada data latihan.

Data yang digunakan dalam proses pelatihan terdiri dari dua fitur:

- **IPK:** Nilai indeks prestasi kumulatif mahasiswa.
- **Total SKS:** Jumlah satuan kredit semester yang telah ditempuh mahasiswa.

Target klasifikasi terdiri dari dua kategori:

- `1` = Lulus
- `0` = Tidak Lulus

Model dilatih menggunakan lima contoh data sesuai dengan skenario pada modul praktikum.

## 🏗️ Arsitektur Sistem

Alur kerja sistem terdiri dari beberapa tahapan:

1. **Input Data:** Menyiapkan data latihan berupa IPK dan Total SKS.
2. **Model Training:** Melatih model menggunakan Decision Tree Classifier.
3. **Model Export:** Menyimpan model ke dalam file `model_kelulusan.pkl`.
4. **Model Loading:** Memanggil model yang telah disimpan menggunakan Joblib.
5. **User Interface:** Menampilkan form input menggunakan Streamlit.
6. **Prediction:** Memproses data masukan dan menampilkan hasil prediksi kelulusan.

## 📂 Struktur Repository

```text
Praktik_MLOps_Streamlit/
│
├── 1_latih_model.py       # Script pelatihan model Machine Learning
├── app.py                # Aplikasi web menggunakan Streamlit
├── model_kelulusan.pkl   # File model hasil pelatihan
├── requirements.txt      # Daftar library yang dibutuhkan
└── README.md             # Dokumentasi proyek
```

## 🚀 Instalasi dan Menjalankan Aplikasi

Ikuti langkah-langkah berikut untuk menjalankan proyek di komputer lokal.

### 1. Clone Repository

```bash
git clone URL_REPOSITORY_KAMU
```

### 2. Masuk ke Folder Proyek

```bash
cd Praktik_MLOps_Streamlit
```

### 3. Instalasi Library

```bash
python -m pip install -r requirements.txt
```

### 4. Melatih Model Machine Learning

Jalankan perintah:

```bash
python 1_latih_model.py
```

Jika berhasil, sistem akan menghasilkan file `model_kelulusan.pkl` yang digunakan sebagai model prediksi.

### 5. Menjalankan Aplikasi Streamlit

Jalankan perintah:

```bash
python -m streamlit run app.py
```

Setelah berhasil, aplikasi akan terbuka melalui browser dan siap digunakan.

## 🖥️ Fitur Aplikasi

Aplikasi Sistem Prediksi Kelulusan Mahasiswa memiliki beberapa fitur utama:

- Input nilai IPK dengan rentang 0.0–4.0.
- Input jumlah Total SKS.
- Tombol untuk menjalankan prediksi kelulusan.
- Menampilkan hasil klasifikasi secara langsung.
- Indikator hasil prediksi dengan tampilan hijau dan merah.

## 🧪 Pengujian Sistem

Pengujian dilakukan menggunakan dua skenario sesuai modul praktikum.

| No. | IPK | Total SKS | Hasil yang Diharapkan |
|---|---:|---:|---|
| 1 | 3.8 | 150 | Lulus Tepat Waktu |
| 2 | 2.5 | 110 | Tidak Lulus |

Pengujian bertujuan memastikan aplikasi dapat menerima input, memanggil model Machine Learning, dan menampilkan hasil klasifikasi.

## 📚 Implementasi MLOps

Konsep MLOps dasar diterapkan melalui proses pemisahan antara pelatihan model dan penggunaan model pada aplikasi.

File `1_latih_model.py` berfungsi untuk membangun dan melatih model, sedangkan `app.py` bertugas memuat model yang telah disimpan dan menyediakan antarmuka bagi pengguna.

Pemisahan ini membuat proses pengembangan dan penggunaan model menjadi lebih terstruktur serta memudahkan pengelolaan aplikasi.

## ⚠️ Catatan

Model dalam proyek ini menggunakan lima data latihan sederhana sesuai contoh pada modul praktikum. Oleh karena itu, hasil prediksi hanya ditujukan untuk demonstrasi pembelajaran dan belum dapat digunakan sebagai dasar penentuan kelulusan mahasiswa secara nyata.

## 👨‍💻 Identitas Pengembang

**Nama:** Muh Dhia Ul Khaq 
**NIM:** 60124025
**Program Studi:** Sains Data  
**Kelas:** Sains Data A  
**Fakultas:** Sains dan Teknologi  
**Universitas:** UIN K.H. Abdurrahman Wahid Pekalongan  

**Mata Kuliah:** Rekayasa Perangkat Lunak (RPL)  
**Praktikum:** Pertemuan 10 – Kolaborasi Tim (Git) & MLOps Dasar

---

<p align="center">

**Developed for RPL Practical Assignment – 2026**

*Machine Learning • Python • Streamlit • MLOps*

</p>
