# Model Transaksi dari Argument CLI (Easy)

## Tujuan Pembelajaran

- Mampu menerapkan pola MVC dalam studi kasus yang lebih kompleks
- Mampu membangun aplikasi CLI sederhana dengan pola command & params (process.argv)
- Mampu mengintegrasikan OOP (class, method) ke dalam arsitektur MVC
- Mampu membangun mini project akhir yang membaca input dari command line

## Soal

Buat program yang membaca `command` beserta `params` (jenis, jumlah, keterangan transaksi) dari command line, simpan ke dalam Model, dan tampilkan hasilnya.

## Tasks

### Task 1
Buat class `TransaksiModel` dengan constructor menerima `jenis`, `jumlah`, `keterangan`.

### Task 2
Baca `command` dari `process.argv[2]` dan `params` dari `process.argv.slice(3)`.

### Task 3
Buat object `TransaksiModel` menggunakan `params[0]`, `params[1]`, `params[2]`, lalu tampilkan hasilnya.

## Results / Test Cases

### Test Case 1
```
Command: node index.js tambah Pemasukan 500000 Gaji
Output: TransaksiModel { jenis: 'Pemasukan', jumlah: '500000', keterangan: 'Gaji' }
```

## Tips dan Trik

- Jika keterangan terdiri dari beberapa kata (misalnya "Gaji Bulanan"), gunakan tanda kutip saat menjalankan perintah, contoh: `node index.js tambah Pemasukan 500000 "Gaji Bulanan"`.
