# Tugas Pengenalan Pola - Klasifikasi Gambar Awan, Gurun, Area Hijau, dan Air dari Citra Satelit
## Deskripsi Project


- Proyek ini bertujuan untuk mengembangkan model klasifikasi gambar yang dapat mengenali empat kategori berbeda: cloud (awan), desert (gurun), green area (area hijau), dan water (air) menggunakan data citra satelit.
- Dataset yang digunakan merupakan dataset  yang diambil dari platform kaggle [Link Dataset Satellite Image Classification di Kaggle](https://www.kaggle.com/datasets/mahmoudreda55/satellite-image-classification). Dataset berisi 1500 gambar dari serangkaian citra satelit yang sudah diklasifikasikan ke dalam empat kategori target: cloud, desert, green area, dan water.
- Data diasukan ke /content di drive dalam bentuk zip.
- lalu di extract dengan code
- Model disimpan di file utama yaitu main.py.
- Proses feature recognition/pengenalan ciri dilakukan secara otomati oleh arsitektur CNN yang dibangun pada tiap layernya.
- Layer konvolusi bertugas dalam proses feature extraction/pengambilan ciri dimana setiap fitur/ciri dari gambar diekstraksi ke dalam bentuk numerik. firtu yang sudah dalam bentuk numerik ini kemudian dapat digunakan untuk pemrosesan seperti klasifikasi. Fitur yang diekstraksi dapat berupa warna, teksture, dll. 
- Feature recognition/pengenalan ciri bertujuan untuk mengambil fitur yang memiliki pengaruh besar atau penting terhadap keseluruhan data. Proses ini dilakukan pada pooling layer dan fully connected layer.
- Model yang digunakan dibangun secara manual dengan menambahkan layer konvolusi dan dropout ke arsitektur CNN yang telah dibagikan sebelumnya. Training hanya dilakukan dalam 10 epoch mengingat banyaknya jumlah data yang diproses.
- Proses evaluasi menunjukkan dari 10 epoch yang dijalankan, model berhasil belajar dengan baik jika dilihat dari nilai loss tiap epoch nya yang semakin menurun. Nilai akurasi setiap epoch juga semakin meningkat. Hal ini menunjukkan jika epoch ditambah, maka terdapat kemungkinan nilai akurasi yang didapat menjadi lebih tinggi.

## Anggota Kelompok 
1. Dimas Teguh Ramadhani        (21102145)

## Kontribusi Anggota
1. Dimas Teguh Ramadhani        (21102145)
   - Mencari dataset
   - Membuat program untuk klasifikasi Gambar Awan, Gurun, Area Hijau, dan Air dari Citra Satelit
