# Mini CLI Manajemen Produk dengan Multiple Command (Hard)

## Tujuan Pembelajaran

- Memahami konsep arsitektur MVC (Model-View-Controller)
- Mampu membedakan tanggung jawab Model, View, dan Controller
- Mampu membaca input dari command line menggunakan pola command & params (process.argv)
- Mampu membuat Controller yang menghubungkan Model, View, dan input CLI

## Soal

Bangun program CLI yang mendukung dua command berbeda, `"tambah"` dan `"diskon"`, masing-masing dengan `params`-nya sendiri.

## Tasks

### Task 1
Rancang format pemanggilan program: `command` adalah `"tambah"` atau `"diskon"`, `params` menyesuaikan command tersebut.

### Task 2
Buat `ProdukModel` dengan method tambahan `hitungDiskon(persen)`.

### Task 3
Di dalam Controller, baca `command` dari `process.argv[2]` dan `params` dari `process.argv.slice(3)`, lalu gunakan percabangan (`if`/`switch`) untuk menentukan proses yang dijalankan.

### Task 4
Untuk command `"tambah"`: ambil nama & harga dari `params`, buat Model, tampilkan lewat View.

### Task 5
Untuk command `"diskon"`: ambil nama, harga, dan persen diskon dari `params`, hitung harga akhir menggunakan method Model, lalu tampilkan lewat View.

### Task 6
Tambahkan validasi: jika `command` tidak dikenali, tampilkan pesan error yang jelas.

## Results / Test Cases

### Test Case 1
```
Command: node index.js tambah Mouse 150000
Output: Nama: Mouse, Harga: Rp150000
```

### Test Case 2
```
Command: node index.js diskon Laptop 10000000 10
Output: Nama: Laptop, Harga Setelah Diskon: Rp9000000
```

### Test Case 3
```
Command: node index.js hapus Mouse
Output: Command tidak dikenali
```

## Tips dan Trik

- Pola "command pertama sebagai aksi" ini sering dipakai di CLI tools sungguhan (mirip perintah git yang punya sub-command seperti `git commit`, `git push`).
- Gunakan destructuring array yang berbeda untuk tiap command, karena jumlah dan urutan `params` bisa berbeda-beda tergantung command yang dipakai.
