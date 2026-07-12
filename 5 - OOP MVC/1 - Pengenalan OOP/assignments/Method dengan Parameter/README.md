# Method dengan Parameter (Easy)

## Tujuan Pembelajaran

- Memahami konsep dasar Object-Oriented Programming (OOP)
- Mampu membuat class dan object di JavaScript
- Memahami constructor dan property dalam class
- Mampu membuat dan memanggil method di dalam class

## Soal

Buat class `Kalkulator` dengan method `tambah(a, b)` yang mengembalikan hasil penjumlahan dua angka.

## Tasks

### Task 1
Buat class `Kalkulator` tanpa constructor khusus (tidak perlu menyimpan property apapun).

### Task 2
Tambahkan method `tambah(a, b)` yang mengembalikan hasil penjumlahan `a` dan `b` menggunakan `return`.

## Results / Test Cases

### Test Case 1
```
Input: new Kalkulator().tambah(5, 10)
Output: 15
```

### Test Case 2
```
Input: new Kalkulator().tambah(-3, 8)
Output: 5
```

## Tips dan Trik

- Method tidak selalu harus menggunakan `this` jika tidak butuh mengakses property object.
