# Getter dan Setter (Medium)

## Tujuan Pembelajaran

- Memahami konsep dasar Object-Oriented Programming (OOP)
- Mampu membuat class dan object di JavaScript
- Memahami constructor dan property dalam class
- Mampu membuat dan memanggil method di dalam class

## Soal

Buat class `Produk` dengan getter dan setter untuk properti harga. Setter harus menolak nilai negatif.

## Tasks

### Task 1
Buat class `Produk` dengan constructor yang menyimpan `nama` dan harga awal ke property internal (misalnya `_harga`).

### Task 2
Buat getter `harga` yang mengembalikan nilai `_harga`.

### Task 3
Buat setter `harga` yang memeriksa apakah nilai baru negatif; jika iya tampilkan pesan penolakan, jika tidak simpan nilainya.

### Task 4
Uji dengan mencoba mengisi harga negatif, lalu tampilkan nilai harga akhirnya.

## Results / Test Cases

### Test Case 1
```
Input:
let produk1 = new Produk("Mouse", 100000);
produk1.harga = -5000;
produk1.harga

Output:
Harga tidak boleh negatif
100000
```

### Test Case 2
```
Input:
let produk2 = new Produk("Keyboard", 200000);
produk2.harga = 250000;
produk2.harga

Output: 250000
```

## Tips dan Trik

- Properti internal biasanya diberi awalan underscore (`_harga`) agar tidak bentrok nama dengan getter/setter yang bernama `harga`.
