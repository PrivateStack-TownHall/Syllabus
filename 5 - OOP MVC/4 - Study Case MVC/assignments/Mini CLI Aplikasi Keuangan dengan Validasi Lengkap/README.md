# Mini CLI Aplikasi Keuangan dengan Validasi Lengkap (Hard)

## Tujuan Pembelajaran

- Mampu menerapkan pola MVC dalam studi kasus yang lebih kompleks
- Mampu membangun aplikasi CLI sederhana dengan pola command & params (process.argv)
- Mampu mengintegrasikan OOP (class, method) ke dalam arsitektur MVC
- Mampu membangun mini project akhir yang membaca input dari command line

## Soal

Bangun program CLI dengan command `"tambah-transaksi"` yang menerima `params` (jenis, jumlah, keterangan), melakukan validasi lengkap, lalu menampilkan hasil transaksi beserta saldo akhir dari saldo awal tetap yang sudah ditentukan di dalam program.

## Tasks

### Task 1
Tentukan saldo awal tetap di dalam program, misalnya `1000000` (tidak perlu dari argument).

### Task 2
Cek apakah `command` sama dengan `"tambah-transaksi"`; jika tidak, tampilkan pesan error dan hentikan proses.

### Task 3
Ambil `jenis`, `jumlah`, `keterangan` dari `params` menggunakan destructuring.

### Task 4
Validasi: `jenis` harus "Pemasukan" atau "Pengeluaran", dan `jumlah` harus berupa angka positif. Jika tidak valid, tampilkan pesan error yang jelas dan hentikan program.

### Task 5
Jika valid, hitung saldo akhir berdasarkan jenis transaksi terhadap saldo awal, lalu tampilkan ringkasan transaksi dan saldo akhir menggunakan View.

## Results / Test Cases

### Test Case 1
```
Command: node index.js tambah-transaksi Pengeluaran 250000 Belanja
Output:
[Pengeluaran] Belanja: Rp250000
Saldo akhir: Rp750000
```

### Test Case 2
```
Command: node index.js cek Pengeluaran 250000 Belanja
Output: Command tidak dikenali
```

### Test Case 3
```
Command: node index.js tambah-transaksi Investasi 100000 Saham
Output: Jenis transaksi tidak valid
```

### Test Case 4
```
Command: node index.js tambah-transaksi Pemasukan -50000 Bonus
Output: Jumlah harus berupa angka positif
```

## Tips dan Trik

- Susun urutan validasi dari yang paling penting: cek `command` dulu, baru cek `jenis`, baru cek `jumlah`.
- Pisahkan bagian "menghitung" dan "menampilkan" agar kode lebih mudah ditelusuri jika terjadi kesalahan.
