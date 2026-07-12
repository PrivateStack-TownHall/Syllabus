# Booking Tiket Bioskop Interaktif (Hard)

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

Buat program CLI pemesanan tiket bioskop. Program menampilkan daftar film beserta harga dan sisa kursi, lalu pengguna memilih film dan jumlah tiket yang diinginkan.

## Tasks

### Task 1
Install dan import `prompt-sync`.

### Task 2
Buat `FilmModel` berupa array data film tetap dengan properti `judul`, `harga`, dan `kursiTersedia`.

### Task 3
Buat `FilmView` untuk menampilkan daftar film dengan nomor urut beserta sisa kursinya.

### Task 4
Buat Controller: tampilkan daftar film, lalu minta pengguna memilih nomor film.

### Task 5
Validasi nomor film yang dipilih harus ada dalam daftar; jika tidak, tampilkan pesan error dan hentikan program.

### Task 6
Minta input jumlah tiket, validasi jumlah tersebut tidak melebihi `kursiTersedia` pada film yang dipilih.

### Task 7
Jika valid, kurangi `kursiTersedia` sesuai jumlah tiket, hitung total harga, lalu tampilkan hasil pemesanan (film, jumlah, total bayar).

## Results / Test Cases

### Test Case 1
```
Input: pilih film 1, jumlah tiket 2
Output:
=== Tiket Berhasil Dipesan ===
Film: Petualangan Luar Angkasa
Jumlah: 2
Total Bayar: Rp70000
```

### Test Case 2
```
Input: pilih film 5 (tidak ada dalam daftar)
Output: Nomor film tidak valid
```

### Test Case 3
```
Input: pilih film 2, jumlah tiket 5 (padahal kursi tersisa cuma 2)
Output: Kursi tidak cukup
```

## Tips dan Trik

- Ingat bahwa nomor yang ditampilkan ke pengguna dimulai dari 1, sedangkan index array dimulai dari 0 — kurangi 1 saat mengubah input menjadi index.
- Kurangi `kursiTersedia` hanya setelah validasi jumlah tiket berhasil, bukan sebelumnya.
