# Multiple Object dari Class yang Sama (Easy)

## Tujuan Pembelajaran

- Memahami konsep dasar Object-Oriented Programming (OOP)
- Mampu membuat class dan object di JavaScript
- Memahami constructor dan property dalam class
- Mampu membuat dan memanggil method di dalam class

## Soal

Buat dua object berbeda dari class `Produk` yang sama, lalu tampilkan keduanya.

## Tasks

### Task 1
Buat class `Produk` dengan constructor yang menerima `nama` dan `harga`.

### Task 2
Buat dua object berbeda dari class `Produk` dengan data yang berbeda, lalu tampilkan keduanya sekaligus dengan `console.log`.

## Results / Test Cases

### Test Case 1
```
Input: new Produk("Mouse", 150000), new Produk("Keyboard", 300000)
Output: Produk { nama: 'Mouse', harga: 150000 } Produk { nama: 'Keyboard', harga: 300000 }
```

## Tips dan Trik

- Setiap object yang dibuat dari `new` memiliki property masing-masing yang independen satu sama lain, meskipun berasal dari class yang sama.
