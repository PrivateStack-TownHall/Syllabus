# Default Value pada Constructor (Easy)

## Tujuan Pembelajaran

- Memahami konsep dasar Object-Oriented Programming (OOP)
- Mampu membuat class dan object di JavaScript
- Memahami constructor dan property dalam class
- Mampu membuat dan memanggil method di dalam class

## Soal

Buat class `Akun` dengan constructor yang memberi nilai default `saldo = 0` jika tidak diisi.

## Tasks

### Task 1
Buat class `Akun` dengan constructor menerima `nama` dan `saldo`, lalu beri nilai default `0` untuk parameter `saldo`.

### Task 2
Buat object tanpa mengisi parameter `saldo`, lalu tampilkan nilai `saldo` tersebut untuk membuktikan default value bekerja.

## Results / Test Cases

### Test Case 1
```
Input: new Akun("Vincent").saldo
Output: 0
```

### Test Case 2
```
Input: new Akun("Budi", 50000).saldo
Output: 50000
```

## Tips dan Trik

- Default parameter dituliskan langsung di deklarasi constructor, misalnya `constructor(nama, saldo = 0)`.
