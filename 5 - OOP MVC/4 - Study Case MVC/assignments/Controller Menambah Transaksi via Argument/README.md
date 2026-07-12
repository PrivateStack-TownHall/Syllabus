# Controller Menambah Transaksi via Argument (Medium)

## Tujuan Pembelajaran

- Mampu menerapkan pola MVC dalam studi kasus yang lebih kompleks
- Mampu membangun aplikasi CLI sederhana dengan pola command & params (process.argv)
- Mampu mengintegrasikan OOP (class, method) ke dalam arsitektur MVC
- Mampu membangun mini project akhir yang membaca input dari command line

## Soal

Buat Controller yang membaca `command` dan `params`, membuat data transaksi lewat Model, lalu menampilkannya lewat View — gabungan dari dua soal sebelumnya dalam satu alur MVC penuh.

## Tasks

### Task 1
Siapkan `TransaksiModel` dan `TransaksiView` seperti pada dua soal sebelumnya.

### Task 2
Buat function `TransaksiController()` yang membaca `command` dan `params`, mengonversi tipe data yang perlu, membuat Model, lalu memanggil View.

### Task 3
Panggil `TransaksiController()` satu kali di akhir file.

## Results / Test Cases

### Test Case 1
```
Command: node index.js tambah Pemasukan 500000 Gaji
Output: [Pemasukan] Gaji: Rp500000
```

## Tips dan Trik

- Sama seperti soal MVC sebelumnya, Controller adalah satu-satunya bagian yang perlu tahu tentang `process.argv`.
