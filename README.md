# Fall Detection dan Prediksi Sebelum Jatuh

Proyek ini berfokus pada deteksi jatuh dari citra CCTV menggunakan deep learning. Sistem dirancang untuk mengklasifikasikan kondisi seseorang ke dalam tiga kelas: Normal, Pre-Fall, dan Fall.

## Anggota Kelompok

1. Cindy Natasa (103102400024)
2. Muhammad Alfayyadh Nezzati Qosim (103102400029)
3. Khalid Muhammad (103102400033)
4. Ivana Gabby Lauretta (103102400037)
5. Evelyna Angie (103102400040)

## Latar Belakang

Deteksi jatuh sangat penting untuk lingkungan seperti rumah sakit, panti jompo, dan tempat dengan pemantauan pasien. Sistem ini diharapkan dapat memberi peringatan lebih awal sebelum jatuh terjadi sehingga tindakan pencegahan bisa dilakukan lebih cepat.

## Novelty

Penelitian ini menekankan deteksi jatuh dari citra CCTV dengan tiga kelas: Normal, Pre-Fall, dan Fall. Model dibangun menggunakan ResNet50 dan transfer learning agar lebih baik dalam mengenali pose manusia. Selain itu, data kelas minoritas diseimbangkan dengan oversampling supaya hasil prediksi lebih seimbang.

## Tujuan

- Mengembangkan sistem deteksi jatuh dari citra CCTV.
- Membagi kondisi menjadi tiga kelas: Normal, Pre-Fall, dan Fall.
- Memberikan peringatan lebih awal sebelum jatuh terjadi.
- Meningkatkan akurasi model dengan pendekatan deep learning dan data yang lebih seimbang.

## Metode

Data gambar berasal dari dua kumpulan citra CCTV yang sudah diberi label pose. Gambar diubah ke ukuran 224×224, dinormalisasi, dan diberi augmentasi agar model lebih kuat saat melatih. Model yang digunakan adalah ResNet50 dengan pretrained ImageNet untuk klasifikasi 3 kelas. Karena data tidak seimbang, kelas minoritas ditambah dengan oversampling. Evaluasi dilakukan dengan akurasi, precision, recall, F1-score, dan confusion matrix.

## Hasil

Model cukup baik dalam mengenali kelas Fall, tetapi masih kesulitan pada kelas Pre-Fall karena jumlah datanya sedikit. Hasil evaluasi menunjukkan akurasi sebesar 71.39%. Kelas Normal sering salah diprediksi sebagai Fall, sedangkan kelas Pre-Fall sering tertukar dengan Normal. Secara umum, model lebih kuat dalam membedakan Normal dan Fall dibandingkan mengenali fase sebelum jatuh.

## Persyaratan

Install package Python berikut:

```bash
pip install torch torchvision torchaudio pandas numpy scikit-learn pillow matplotlib
```

## Cara Menjalankan

1. Buka file notebook `WithNewFeatures(1).ipynb`.
2. Pastikan dataset sudah tersedia di laptop.
3. Sesuaikan path dataset pada bagian awal notebook.
4. Jalankan semua sel secara berurutan.

## Catatan

Jika dataset berada di lokasi berbeda, ubah nilai `TRAIN_DIR` dan `TEST_DIR` sesuai path komputer Anda.
