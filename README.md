# Tugas Pengenalan Pola - Klasifikasi Gambar Awan, Gurun, Area Hijau, dan Air dari Citra Satelit
## Deskripsi Project


- Proyek ini bertujuan untuk mengembangkan model klasifikasi gambar yang dapat mengenali empat kategori berbeda: cloud (awan), desert (gurun), green area (area hijau), dan water (air) menggunakan data citra satelit.
- Dataset yang digunakan merupakan dataset  yang diambil dari platform kaggle [Link Dataset Satellite Image Classification di Kaggle](https://www.kaggle.com/datasets/mahmoudreda55/satellite-image-classification). Dataset berisi 1500 gambar dari serangkaian citra satelit yang sudah diklasifikasikan ke dalam empat kategori target: cloud, desert, green area, dan water.
![Cuplikan layar 2024-06-12 155746](https://github.com/DimasTeguhR/tubes-pengenalan-pola/assets/60166666/cbb4dc90-e277-40fc-ad56-8f688cdb4755)
  
Berikut adalah prosesnya:

1. Pengunduhan dan Ekstraksi Data

Data awalnya dimasukkan ke dalam Google Drive dalam bentuk file zip dengan nama "datasatelit.zip".
Kemudian, menggunakan kode zip_ref.extractall('/content'), file zip tersebut diekstraksi ke dalam direktori /content/.

2. Pengolahan Data Citra

Data citra terdiri dari empat kategori: cloudy, desert, green_area, dan water.
Data tersebut diproses menggunakan ImageDataGenerator dari Keras untuk melakukan augmentasi data seperti rotasi, flip horizontal, shear, zoom, dan fill mode.
Data yang telah di-augmentasi akan digunakan sebagai input untuk model CNN.

3. Arsitektur Convolutional Neural Network (CNN)

Model CNN yang digunakan memiliki arsitektur sebagai berikut:
Conv2D dengan 64 filter ukuran 3x3, fungsi aktivasi ReLU.
MaxPooling2D dengan ukuran pool 2x2.
Dropout layer dengan nilai dropout sebesar 0.4.
Flatten layer untuk meratakan output menjadi satu dimensi.
Dense layer dengan 64 neuron, fungsi aktivasi ReLU.
Dense layer dengan 256 neuron, fungsi aktivasi ReLU.
Dense layer output dengan 4 neuron (sesuai jumlah kategori), fungsi aktivasi softmax.

4. Pelatihan Model

Model CNN dilatih menggunakan metode model.fit dengan batch size 64, jumlah epoch 100, dan menggunakan callback untuk menghentikan pelatihan jika akurasi mencapai 0.92.
Data pelatihan dan validasi diambil dari direktori yang telah di-augmentasi sebelumnya.

5. Evaluasi Model

Grafik ditampilkan untuk memonitor akurasi dan loss dari setiap epoch pelatihan.
Model yang sudah dilatih akan diubah ke format TensorFlow Lite untuk keperluan deploy di perangkat mobile.

6. Prediksi

Setelah pelatihan, program memungkinkan pengguna untuk mengunggah gambar untuk diprediksi kategori mana gambar tersebut termasuk.
Model CNN akan memprediksi kategori gambar (cloudy, desert, green area, water) dan menampilkan hasil prediksi.

7. Analisis Hasil

Analisis hasil pelatihan menunjukkan bahwa model belajar dengan baik dalam 10 epoch yang dijalankan, dengan nilai loss yang semakin menurun dan akurasi yang semakin meningkat setiap epoch-nya. Hal ini menunjukkan potensi peningkatan kinerja model jika dilatih dengan lebih banyak epoch.
Program ini merupakan implementasi yang baik untuk memahami konsep dasar pengolahan citra menggunakan CNN, augmentasi data, pelatihan model, evaluasi kinerja model, dan prediksi. Dengan menambahkan lebih banyak data dan melatih model dengan lebih banyak epoch, kemungkinan dapat meningkatkan akurasi klasifikasi.

## Anggota Kelompok 
1. Dimas Teguh Ramadhani        (21102145)

## Kontribusi Anggota
1. Dimas Teguh Ramadhani        (21102145)
   - Mencari dataset
   - Membuat program untuk klasifikasi Gambar Awan, Gurun, Area Hijau, dan Air dari Citra Satelit
