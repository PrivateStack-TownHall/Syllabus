# Inheritance Sederhana (Easy)

## Tujuan Pembelajaran

- Memahami 4 pilar utama OOP: enkapsulasi, inheritance, polimorfisme, dan abstraksi
- Mampu menerapkan enkapsulasi menggunakan private field (`#`)
- Mampu membuat inheritance antar class menggunakan `extends` dan `super`
- Mampu menerapkan polimorfisme melalui method overriding

## Soal

Buat class `Hewan` dengan method `bersuara()`, lalu buat class `Kucing` yang extends dari `Hewan` tanpa mengubah apapun.

## Tasks

### Task 1
Buat class `Hewan` dengan method `bersuara()` yang menampilkan pesan umum.

### Task 2
Buat class `Kucing` yang extends `Hewan`, tanpa menambahkan method baru apapun.

### Task 3
Buat object dari `Kucing`, lalu panggil method `bersuara()` untuk membuktikan method tersebut diwariskan.

## Results / Test Cases

### Test Case 1
```
Input: new Kucing().bersuara()
Output: Hewan mengeluarkan suara
```

## Tips dan Trik

- Class turunan (`extends`) otomatis mewarisi seluruh method dari parent class-nya, meskipun tidak dituliskan ulang.
