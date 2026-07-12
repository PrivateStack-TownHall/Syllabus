# Membuat Class Sederhana (Easy)

## Tujuan Pembelajaran

- Memahami konsep dasar Object-Oriented Programming (OOP)
- Mampu membuat class dan object di JavaScript
- Memahami constructor dan property dalam class
- Mampu membuat dan memanggil method di dalam class

## Soal

Buat class `Mobil` dengan properti `merk` dan `warna`, lalu buat satu object dari class tersebut dan tampilkan propertinya.

## Tasks

### Task 1
Buat class bernama `Mobil` dengan constructor yang menerima dua parameter: `merk` dan `warna`. Simpan kedua parameter tersebut sebagai property pada object menggunakan `this`.

### Task 2
Buat satu object baru dari class `Mobil` menggunakan keyword `new`, lalu tampilkan property `merk` dan `warna` dari object tersebut ke console.

## Results / Test Cases

### Test Case 1
```
Input: new Mobil("Toyota", "Merah")
Output: Toyota Merah
```

### Test Case 2
```
Input: new Mobil("Honda", "Hitam")
Output: Honda Hitam
```

## Tips dan Trik

- Gunakan `this.namaProperty = value` di dalam constructor untuk menyimpan data ke object.
- Property yang disimpan lewat `this` di constructor otomatis bisa diakses lewat `namaObject.namaProperty`.
