# Model Produk dari Argument CLI (Easy)

## Tujuan Pembelajaran

- Memahami konsep arsitektur MVC (Model-View-Controller)
- Mampu membedakan tanggung jawab Model, View, dan Controller
- Mampu membaca input dari command line menggunakan pola command & params (process.argv)
- Mampu membuat Controller yang menghubungkan Model, View, dan input CLI

## Soal

Buat program yang membaca command beserta params (nama dan harga produk) dari command line, lalu gunakan Model `ProdukModel` untuk menyimpan datanya dan tampilkan hasilnya.

## Tasks

### Task 1
Buat class `ProdukModel` dengan constructor menerima `nama` dan `harga`.

### Task 2
Baca `command` dari `process.argv[2]`, dan `params` dari `process.argv.slice(3)` sebagai array berisi sisa argument.

### Task 3
Buat object `ProdukModel` menggunakan `params[0]` sebagai nama dan `params[1]` sebagai harga, lalu tampilkan hasilnya ke console.

## Results / Test Cases

### Test Case 1
```
Command: node index.js tambah Mouse 150000
Output: ProdukModel { nama: 'Mouse', harga: '150000' }
```

### Test Case 2
```
Command: node index.js tambah Keyboard 300000
Output: ProdukModel { nama: 'Keyboard', harga: '300000' }
```

## Tips dan Trik

- Pola `command` + `params` sering dipakai di CLI tools sungguhan: `command` adalah kata pertama setelah nama file (biasanya sebuah aksi), sedangkan `params` adalah sisa argument setelahnya dalam bentuk array.
- `process.argv.slice(3)` akan selalu mengembalikan array, meskipun argumentnya cuma satu atau bahkan kosong.
