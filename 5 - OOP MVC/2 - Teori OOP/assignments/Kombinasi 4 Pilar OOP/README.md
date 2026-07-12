# Kombinasi 4 Pilar OOP (Hard)

## Tujuan Pembelajaran

- Memahami 4 pilar utama OOP: enkapsulasi, inheritance, polimorfisme, dan abstraksi
- Mampu menerapkan enkapsulasi menggunakan private field (`#`)
- Mampu membuat inheritance antar class menggunakan `extends` dan `super`
- Mampu menerapkan polimorfisme melalui method overriding

## Soal

Buat sistem kepegawaian sederhana: class `Karyawan` (enkapsulasi dengan private gaji), class `Manager` yang extends `Karyawan` (inheritance) dan meng-override method `hitungBonus()` (polimorfisme), dengan detail perhitungan bonus disembunyikan di dalam method (abstraksi).

## Tasks

### Task 1
Buat class `Karyawan` dengan private field `#gaji`, method `getGaji()` untuk membacanya, dan method `hitungBonus()` dengan persentase bonus tertentu.

### Task 2
Buat class `Manager` yang extends `Karyawan`.

### Task 3
Override method `hitungBonus()` di `Manager` dengan persentase bonus yang berbeda (lebih besar), menggunakan `getGaji()` untuk mengakses gaji dari parent.

### Task 4
Buat satu object `Karyawan` biasa dan satu object `Manager`, lalu bandingkan hasil `hitungBonus()` keduanya.

## Results / Test Cases

### Test Case 1
```
Input: new Karyawan("Budi", 5000000).hitungBonus()
Output: 250000
```

### Test Case 2
```
Input: new Manager("Vincent", 10000000).hitungBonus()
Output: 1500000
```

## Tips dan Trik

- Karena `#gaji` bersifat private, class turunan tidak bisa mengaksesnya langsung — gunakan method publik seperti `getGaji()` sebagai jembatan.
- Soal ini menggabungkan seluruh pilar OOP sekaligus: coba selesaikan satu pilar dulu (misalnya enkapsulasi), baru lanjut ke pilar berikutnya.
