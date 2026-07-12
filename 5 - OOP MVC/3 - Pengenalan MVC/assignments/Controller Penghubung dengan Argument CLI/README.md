# Controller Penghubung dengan Argument CLI (Medium)

## Tujuan Pembelajaran

- Memahami konsep arsitektur MVC (Model-View-Controller)
- Mampu membedakan tanggung jawab Model, View, dan Controller
- Mampu membaca input dari command line menggunakan pola command & params (process.argv)
- Mampu membuat Controller yang menghubungkan Model, View, dan input CLI

## Soal

Buat Controller yang membaca `command` dan `params`, membuat Model, lalu menampilkannya lewat View — gabungan dari dua soal sebelumnya dalam satu alur MVC penuh.

## Tasks

### Task 1
Siapkan `ProdukModel` dan `ProdukView` seperti pada dua soal sebelumnya.

### Task 2
Buat function `ProdukController()` yang membaca `command` dan `params`, mengonversi tipe data yang perlu, lalu memanggil Model dan View secara berurutan.

### Task 3
Panggil `ProdukController()` satu kali di baris terakhir file agar otomatis berjalan saat program dieksekusi.

## Results / Test Cases

### Test Case 1
```
Command: node index.js tambah Headset 450000
Output: Nama: Headset, Harga: Rp450000
```

### Test Case 2
```
Command: node index.js tambah Webcam 600000
Output: Nama: Webcam, Harga: Rp600000
```

## Tips dan Trik

- Controller sebaiknya menjadi satu-satunya bagian program yang berurusan langsung dengan `process.argv`; Model dan View tidak perlu tahu argument datang dari mana.
