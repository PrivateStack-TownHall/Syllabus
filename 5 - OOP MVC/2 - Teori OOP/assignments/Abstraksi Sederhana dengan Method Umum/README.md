# Abstraksi Sederhana dengan Method Umum (Easy)

## Tujuan Pembelajaran

- Memahami 4 pilar utama OOP: enkapsulasi, inheritance, polimorfisme, dan abstraksi
- Mampu menerapkan enkapsulasi menggunakan private field (`#`)
- Mampu membuat inheritance antar class menggunakan `extends` dan `super`
- Mampu menerapkan polimorfisme melalui method overriding

## Soal

Buat class `Kendaraan` yang menyembunyikan detail teknis internal di dalam method privat, sehingga pengguna hanya perlu memanggil satu method publik tanpa tahu detailnya.

## Tasks

### Task 1
Buat class `Kendaraan` dengan satu method publik `nyalakan()`.

### Task 2
Buat satu method lain (misalnya `_prosesInternal()`) yang berisi "detail teknis" dan dipanggil dari dalam `nyalakan()`.

### Task 3
Pastikan pengguna cukup memanggil `nyalakan()` saja tanpa perlu tahu isi `_prosesInternal()`.

## Results / Test Cases

### Test Case 1
```
Input: new Kendaraan().nyalakan()
Output: Kendaraan menyala
```

## Tips dan Trik

- Awalan underscore (`_namaMethod`) adalah konvensi umum untuk menandai method yang sifatnya "internal" dan tidak dimaksudkan dipanggil langsung dari luar.
