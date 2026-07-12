# Manajemen Perpustakaan dengan Denda Keterlambatan (Hard)

## Tujuan Pembelajaran

- Mampu membangun aplikasi CLI interaktif menggunakan package eksternal prompt-sync
- Mampu menggabungkan OOP dan MVC dalam studi kasus yang bervariasi dan kompleks
- Mampu merancang alur program dengan banyak validasi, percabangan, dan perulangan
- Mampu mengelola state aplikasi yang berubah secara dinamis berdasarkan input pengguna

## Cara Install

Sebelum mengerjakan soal ini, install package `prompt-sync` terlebih dahulu:

```bash
npm init -y
npm i prompt-sync
```
Lalu import di bagian paling atas file kamu:
```js
const prompt = require("prompt-sync")();
```

## Soal

Buat program CLI yang menerima data buku yang dipinjam (judul dan jumlah hari peminjaman) secara berulang, menghitung denda jika melewati batas peminjaman, lalu menampilkan ringkasan beserta total denda.

## Tasks

### Task 1
Install dan import `prompt-sync`.

### Task 2
Buat class `PeminjamanModel` dengan array kosong, batas hari peminjaman (misalnya 7 hari), dan tarif denda per hari (misalnya Rp2.000).

### Task 3
Buat method `tambah(judul, jumlahHari)` di dalam Model yang menghitung hari keterlambatan (jika ada) dan besar dendanya, lalu menyimpannya ke array.

### Task 4
Buat method `totalDenda()` yang menjumlahkan seluruh denda dari semua buku yang tersimpan.

### Task 5
Buat Controller dengan loop yang meminta judul buku secara berulang sampai pengguna mengetik "selesai".

### Task 6
Untuk tiap buku, minta input jumlah hari peminjaman, validasi harus angka positif, lalu tambahkan ke Model.

### Task 7
Setelah loop selesai, tampilkan ringkasan seluruh buku (status tepat waktu/telat beserta dendanya) dan total denda menggunakan View.

## Results / Test Cases

### Test Case 1
```
Input: "Laskar Pelangi"/5 hari, "Bumi Manusia"/10 hari, lalu "selesai"
Output:
=== Ringkasan Peminjaman ===
Laskar Pelangi (5 hari): Tepat waktu
Bumi Manusia (10 hari): Telat, denda Rp6000
Total Denda: Rp6000
```

## Tips dan Trik

- Gunakan `Math.max(0, jumlahHari - batasHari)` untuk memastikan hari keterlambatan tidak pernah bernilai negatif.
- Hitung dan simpan denda langsung saat data ditambahkan ke Model, supaya `totalDenda()` tinggal menjumlahkan nilai yang sudah ada.
