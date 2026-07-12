# Sistem Parkir dengan Tarif Bertingkat (Hard)

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

Buat program CLI sistem parkir yang menerima data kendaraan (jenis dan durasi parkir dalam jam) secara berulang, menghitung tarif berdasarkan jenis kendaraan menggunakan inheritance dan polimorfisme, lalu menampilkan struk dan total pendapatan.

## Tasks

### Task 1
Install dan import `prompt-sync`.

### Task 2
Buat class `Kendaraan` dengan method `hitungTarif()` yang mengembalikan `0` sebagai default.

### Task 3
Buat class `Mobil` dan `Motor` yang masing-masing extends `Kendaraan`, dan override `hitungTarif()` dengan tarif per jam yang berbeda (mobil lebih mahal dari motor).

### Task 4
Buat Controller dengan loop yang meminta jenis kendaraan secara berulang sampai pengguna mengetik "selesai".

### Task 5
Validasi jenis kendaraan harus "mobil" atau "motor"; ulangi input jika tidak valid.

### Task 6
Minta input durasi parkir dalam jam, validasi harus angka positif, lalu buat object dari class yang sesuai dan hitung tarifnya.

### Task 7
Tampilkan struk untuk tiap kendaraan yang diproses, dan tampilkan total pendapatan keseluruhan setelah loop berhenti.

## Results / Test Cases

### Test Case 1
```
Input: mobil/3 jam, motor/2 jam, lalu "selesai"
Output:
mobil (3 jam): Rp15000
motor (2 jam): Rp4000
Total Pendapatan Parkir: Rp19000
```

## Tips dan Trik

- Polimorfisme di soal ini terlihat dari cara kamu memanggil `hitungTarif()` yang sama persis untuk `Mobil` maupun `Motor`, tapi hasilnya berbeda tergantung object-nya.
- Akumulasikan `totalPendapatan` di luar loop (sebelum `while` dimulai), lalu tambahkan nilainya setiap kali satu kendaraan selesai diproses.
