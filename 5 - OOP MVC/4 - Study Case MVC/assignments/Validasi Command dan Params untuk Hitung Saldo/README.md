# Validasi Command dan Params untuk Hitung Saldo (Medium)

## Tujuan Pembelajaran

- Mampu menerapkan pola MVC dalam studi kasus yang lebih kompleks
- Mampu membangun aplikasi CLI sederhana dengan pola command & params (process.argv)
- Mampu mengintegrasikan OOP (class, method) ke dalam arsitektur MVC
- Mampu membangun mini project akhir yang membaca input dari command line

## Soal

Program menerima command `"hitung-saldo"` beserta `params` (saldo awal, jenis, jumlah), validasi command dan jumlah harus angka positif, lalu hitung saldo akhir.

## Tasks

### Task 1
Cek apakah `command` sama dengan `"hitung-saldo"`; jika tidak, tampilkan pesan error dan hentikan proses.

### Task 2
Ambil `saldoAwal`, `jenis`, `jumlah` dari `params` menggunakan destructuring, konversikan `saldoAwal` dan `jumlah` menjadi number.

### Task 3
Validasi `jumlah` harus angka positif; jika tidak valid, tampilkan pesan error dan hentikan proses.

### Task 4
Jika valid, hitung saldo akhir: tambahkan `jumlah` ke `saldoAwal` jika `jenis` "Pemasukan", kurangi jika "Pengeluaran".

## Results / Test Cases

### Test Case 1
```
Command: node index.js hitung-saldo 1000000 Pengeluaran 250000
Output: Saldo akhir: Rp750000
```

### Test Case 2
```
Command: node index.js hitung-saldo 500000 Pemasukan -200000
Output: Jumlah harus berupa angka positif
```

### Test Case 3
```
Command: node index.js cek 500000 Pemasukan 200000
Output: Command tidak dikenali
```

## Tips dan Trik

- Validasi command sebaiknya dilakukan paling awal, sebelum program repot-repot membaca `params`.
