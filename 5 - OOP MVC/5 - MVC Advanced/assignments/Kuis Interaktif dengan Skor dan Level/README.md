# Kuis Interaktif dengan Skor dan Level (Hard)

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

Buat program kuis pilihan ganda interaktif. Program menampilkan beberapa soal satu per satu, mencocokkan jawaban pengguna, lalu menampilkan skor akhir dan level berdasarkan skor tersebut.

## Tasks

### Task 1
Install dan import `prompt-sync`.

### Task 2
Buat `SoalModel` berupa array minimal 3 soal pilihan ganda tetap, masing-masing berisi pertanyaan, daftar pilihan, dan jawaban benar.

### Task 3
Buat function `tentukanLevel(skor)` yang mengembalikan "Mahir" jika skor >= 80, "Menengah" jika skor >= 50, dan "Pemula" untuk sisanya.

### Task 4
Buat Controller dengan loop yang menampilkan tiap soal beserta pilihannya, lalu meminta jawaban pengguna.

### Task 5
Cocokkan jawaban pengguna dengan jawaban benar pada soal tersebut; jika benar, tambahkan poin ke skor.

### Task 6
Setelah semua soal selesai ditanyakan, hitung level berdasarkan skor akhir menggunakan `tentukanLevel()`.

### Task 7
Tampilkan skor akhir dan level menggunakan View.

## Results / Test Cases

### Test Case 1
```
Input: jawab semua soal dengan benar
Output:
=== Hasil Kuis ===
Skor: 99
Level: Mahir
```

### Test Case 2
```
Input: hanya 1 dari 3 soal terjawab benar
Output:
=== Hasil Kuis ===
Skor: 33
Level: Pemula
```

## Tips dan Trik

- Bagi 100 poin secara merata ke seluruh soal (misalnya `Math.round(100 / jumlahSoal)`) supaya skor akhir tetap masuk akal berapapun jumlah soalnya.
- Gunakan `.toUpperCase()` pada jawaban pengguna sebelum dibandingkan, supaya jawaban huruf kecil maupun besar tetap dianggap sama.
