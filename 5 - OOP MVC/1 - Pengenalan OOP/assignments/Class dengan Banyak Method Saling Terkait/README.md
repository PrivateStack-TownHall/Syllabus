# Class dengan Banyak Method Saling Terkait (Hard)

## Tujuan Pembelajaran

- Memahami konsep dasar Object-Oriented Programming (OOP)
- Mampu membuat class dan object di JavaScript
- Memahami constructor dan property dalam class
- Mampu membuat dan memanggil method di dalam class

## Soal

Buat class `KeranjangBelanja` yang memiliki method untuk menambah barang, menghitung total belanja, dan menampilkan daftar barang.

## Tasks

### Task 1
Buat class `KeranjangBelanja` dengan constructor yang menginisialisasi array kosong untuk menyimpan barang.

### Task 2
Buat method `tambahBarang(nama, harga, jumlah)` yang menambahkan object barang baru ke dalam array tersebut.

### Task 3
Buat method `hitungTotal()` yang menjumlahkan `harga * jumlah` dari seluruh barang di dalam array.

### Task 4
Buat method `tampilkanDaftar()` yang mencetak setiap barang beserta subtotalnya.

### Task 5
Buat satu object, tambahkan beberapa barang, lalu panggil `tampilkanDaftar()` dan `hitungTotal()`.

## Results / Test Cases

### Test Case 1
```
Input:
let keranjang1 = new KeranjangBelanja();
keranjang1.tambahBarang("Kopi", 20000, 2);
keranjang1.tambahBarang("Roti", 15000, 3);
keranjang1.tampilkanDaftar();
keranjang1.hitungTotal();

Output:
Kopi x2 = 40000
Roti x3 = 45000
Total: 85000
```

### Test Case 2
```
Input:
let keranjang2 = new KeranjangBelanja();
keranjang2.tambahBarang("Buku", 50000, 1);
keranjang2.hitungTotal();

Output: 50000
```

## Tips dan Trik

- Gunakan `Array.prototype.reduce()` untuk menjumlahkan total dari seluruh item di dalam array secara ringkas.
- Pisahkan tanggung jawab tiap method: satu method fokus untuk satu tugas saja (menambah, menghitung, atau menampilkan).
