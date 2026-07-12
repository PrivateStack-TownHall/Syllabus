# View untuk Menampilkan Data dari Argument (Easy)

## Tujuan Pembelajaran

- Memahami konsep arsitektur MVC (Model-View-Controller)
- Mampu membedakan tanggung jawab Model, View, dan Controller
- Mampu membaca input dari command line menggunakan pola command & params (process.argv)
- Mampu membuat Controller yang menghubungkan Model, View, dan input CLI

## Soal

Gunakan data dari `params` untuk ditampilkan lewat function View dengan format yang rapi dan harga yang sudah dikonversi ke angka.

## Tasks

### Task 1
Baca `command` dari `process.argv[2]` dan `params` dari `process.argv.slice(3)`.

### Task 2
Ambil `params[0]` sebagai nama dan konversikan `params[1]` menjadi number sebagai harga.

### Task 3
Buat function `ProdukView(nama, harga)` yang menampilkan `Nama: ..., Harga: Rp...`, lalu panggil menggunakan data dari params.

## Results / Test Cases

### Test Case 1
```
Command: node index.js tambah Mouse 150000
Output: Nama: Mouse, Harga: Rp150000
```

### Test Case 2
```
Command: node index.js tambah Monitor 2500000
Output: Nama: Monitor, Harga: Rp2500000
```

## Tips dan Trik

- Selalu konversi elemen `params` yang seharusnya berupa angka menggunakan `Number()`, karena semua elemen `params` masih berupa string.
