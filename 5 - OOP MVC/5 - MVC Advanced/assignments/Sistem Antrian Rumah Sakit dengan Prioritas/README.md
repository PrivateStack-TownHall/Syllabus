# Sistem Antrian Rumah Sakit dengan Prioritas (Hard)

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

Buat program CLI yang menerima data pasien (nama dan kategori) secara berulang, lalu mengurutkan antrian berdasarkan prioritas kategori sebelum ditampilkan.

## Tasks

### Task 1
Install dan import `prompt-sync`.

### Task 2
Buat class `Pasien` dengan method `getPrioritas()` yang mengembalikan nilai default (misalnya `3` untuk kategori umum).

### Task 3
Buat class `PasienBPJS` dan `PasienDarurat` yang masing-masing extends `Pasien`, dan override `getPrioritas()` dengan nilai lebih kecil untuk prioritas lebih tinggi (semakin kecil angka, semakin diprioritaskan).

### Task 4
Buat Controller dengan loop yang meminta nama pasien secara berulang sampai pengguna mengetik "selesai".

### Task 5
Untuk tiap pasien, minta input kategori ("umum"/"bpjs"/"darurat"), validasi kategori tersebut, lalu buat object dari class yang sesuai.

### Task 6
Simpan seluruh object pasien ke dalam array, lalu urutkan array tersebut berdasarkan hasil `getPrioritas()` sebelum ditampilkan.

### Task 7
Tampilkan urutan antrian akhir menggunakan View.

## Results / Test Cases

### Test Case 1
```
Input: Budi/umum, Ani/darurat, Cici/bpjs, lalu "selesai"
Output:
=== Urutan Antrian ===
1. Ani (darurat)
2. Cici (bpjs)
3. Budi (umum)
```

## Tips dan Trik

- Gunakan `Array.prototype.sort()` dengan fungsi pembanding `(a, b) => a.getPrioritas() - b.getPrioritas()` untuk mengurutkan dari prioritas tertinggi (angka terkecil) ke terendah.
- Polimorfisme di soal ini terlihat dari cara kamu memanggil `getPrioritas()` yang sama persis untuk semua jenis pasien, tapi hasilnya berbeda tergantung class-nya.
