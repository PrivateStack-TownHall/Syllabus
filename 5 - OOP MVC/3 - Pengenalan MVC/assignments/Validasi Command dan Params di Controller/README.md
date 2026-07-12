# Validasi Command dan Params di Controller (Medium)

## Tujuan Pembelajaran

- Memahami konsep arsitektur MVC (Model-View-Controller)
- Mampu membedakan tanggung jawab Model, View, dan Controller
- Mampu membaca input dari command line menggunakan pola command & params (process.argv)
- Mampu membuat Controller yang menghubungkan Model, View, dan input CLI

## Soal

Tambahkan validasi: `command` harus `"tambah"`, `params` harus lengkap, dan harga harus berupa angka positif, sebelum data diteruskan ke Model.

## Tasks

### Task 1
Di dalam Controller, cek apakah `command` sama dengan `"tambah"`; jika tidak, tampilkan pesan "Command tidak dikenali" dan hentikan proses.

### Task 2
Ambil `nama` dan `hargaRaw` dari `params` menggunakan destructuring, lalu cek apakah keduanya terisi.

### Task 3
Jika `params` tidak lengkap, tampilkan pesan error dan hentikan proses menggunakan `return`.

### Task 4
Konversi `hargaRaw` ke number, lalu cek apakah hasilnya valid (bukan `NaN`) dan lebih besar dari 0.

### Task 5
Jika semua validasi lolos, lanjutkan proses seperti biasa (buat Model, tampilkan View).

## Results / Test Cases

### Test Case 1
```
Command: node index.js hapus Mouse 150000
Output: Command tidak dikenali
```

### Test Case 2
```
Command: node index.js tambah Mouse
Output: Params tidak lengkap. Contoh: node index.js tambah <nama> <harga>
```

### Test Case 3
```
Command: node index.js tambah Mouse -1000
Output: Harga tidak valid
```

### Test Case 4
```
Command: node index.js tambah Mouse 150000
Output: Nama: Mouse, Harga: Rp150000
```

## Tips dan Trik

- Gunakan destructuring array `const [nama, hargaRaw] = params;` untuk mengambil elemen params dengan nama variabel yang jelas.
- Gunakan `isNaN()` untuk memeriksa apakah hasil konversi angka valid atau tidak.
