# Assignment - Menambah dan Menghapus Elemen di Awal Array (Easy)

## Tujuan Pembelajaran

- Memahami fungsi method `shift()` dan `unshift()` pada array.
- Mampu menambahkan elemen ke awal array menggunakan `unshift()`.
- Mampu menghapus elemen pertama dari array menggunakan `shift()`.
- Mampu memanipulasi isi array menggunakan method bawaan JavaScript.

## Soal

Diberikan sebuah array yang berisi beberapa angka.

Buatlah sebuah program dengan langkah-langkah berikut:

1. Tambahkan sebuah elemen baru ke **awal array** menggunakan method `unshift()`.
2. Tampilkan isi array setelah proses penambahan.
3. Hapus elemen pertama menggunakan method `shift()`.
4. Tampilkan kembali isi array setelah proses penghapusan.

> **Catatan:** Fokus utama assignment ini adalah memahami cara kerja method `shift()` dan `unshift()` dalam memanipulasi elemen pada array.

## Result / Test Case

**Input**

```javascript
const numbers = [2, 3, 4];

numbers.unshift(1);
numbers.shift();
```

**Output**

```text
[1, 2, 3, 4]
[2, 3, 4]
```
