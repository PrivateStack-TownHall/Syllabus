# Method dalam Class (Easy)

## Tujuan Pembelajaran

- Memahami konsep dasar Object-Oriented Programming (OOP)
- Mampu membuat class dan object di JavaScript
- Memahami constructor dan property dalam class
- Mampu membuat dan memanggil method di dalam class

## Soal

Tambahkan method `sapa()` pada class `Siswa` yang menampilkan salam menggunakan nama siswa tersebut.

## Tasks

### Task 1
Buat class `Siswa` dengan constructor yang menyimpan `nama`.

### Task 2
Tambahkan method `sapa()` di dalam class yang menampilkan kalimat salam menggunakan `this.nama`.

### Task 3
Buat object dari class tersebut dan panggil method `sapa()`.

## Results / Test Cases

### Test Case 1
```
Input: new Siswa("Vincent").sapa()
Output: Halo, nama saya Vincent
```

### Test Case 2
```
Input: new Siswa("Ani").sapa()
Output: Halo, nama saya Ani
```

## Tips dan Trik

- Di dalam method, gunakan `this.nama` untuk mengakses property milik object yang sedang memanggil method tersebut.
