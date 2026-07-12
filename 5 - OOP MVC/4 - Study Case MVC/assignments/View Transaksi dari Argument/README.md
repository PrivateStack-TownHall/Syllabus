# View Transaksi dari Argument (Easy)

## Tujuan Pembelajaran

- Mampu menerapkan pola MVC dalam studi kasus yang lebih kompleks
- Mampu membangun aplikasi CLI sederhana dengan pola command & params (process.argv)
- Mampu mengintegrasikan OOP (class, method) ke dalam arsitektur MVC
- Mampu membangun mini project akhir yang membaca input dari command line

## Soal

Tampilkan data transaksi dari `params` menggunakan format `[jenis] keterangan: Rp jumlah`, dengan jumlah yang sudah dikonversi menjadi angka.

## Tasks

### Task 1
Baca `command` dari `process.argv[2]` dan `params` dari `process.argv.slice(3)`.

### Task 2
Ambil `jenis`, `jumlah` (dikonversi ke number), dan `keterangan` dari `params`.

### Task 3
Buat function `TransaksiView(jenis, jumlah, keterangan)` yang menampilkan data dalam format yang ditentukan.

## Results / Test Cases

### Test Case 1
```
Command: node index.js tambah Pengeluaran 20000 "Makan siang"
Output: [Pengeluaran] Makan siang: Rp20000
```

## Tips dan Trik

- Ingat gunakan tanda kutip di terminal untuk elemen `params` yang mengandung spasi.
