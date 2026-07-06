# Tujuan Pembelajaran
- Mampu menggabungkan konsep variabel, function, kondisi, looping, dan array/object dalam satu program
- Mampu membangun program sederhana yang menyelesaikan masalah nyata
- Mampu menyusun program CRUD sederhana berbasis console
- Mampu membangun mini project akhir yang mengintegrasikan seluruh materi

---

# Assignment 1 - Konversi Suhu (Easy)
Buat program konversi suhu dari Celsius ke Fahrenheit menggunakan function.

```js
function celciusKeFahrenheit(celcius) {
  return (celcius * 9) / 5 + 32;
}

console.log(celciusKeFahrenheit(30));
```

**Hasil yang diharapkan:**
```
86
```

---

# Assignment 2 - To-Do List Sederhana (Easy)
Buat program to-do list berbasis console menggunakan array (tambah dan tampilkan daftar tugas).

```js
let todoList = [];

function tambahTugas(tugas) {
  todoList.push(tugas);
}

tambahTugas("Belajar JavaScript");
tambahTugas("Kerjakan tugas Sekolah Stack");

console.log(todoList);
```

**Hasil yang diharapkan:**
```
[ 'Belajar JavaScript', 'Kerjakan tugas Sekolah Stack' ]
```

---

# Assignment 3 - Total Belanja dengan Diskon (Easy)
Hitung total belanja dari beberapa item beserta diskon sederhana (diskon 10% jika total di atas 100.000).

```js
let belanja = [50000, 30000, 25000];
let total = belanja.reduce((acc, curr) => acc + curr, 0);

if (total > 100000) {
  total = total - total * 0.1;
}

console.log(total);
```

**Hasil yang diharapkan:**
```
94500
```

---

# Assignment 4 - Cek Bilangan Prima (Easy)
Buat function untuk mengecek apakah sebuah angka merupakan bilangan prima.

```js
function isPrima(angka) {
  if (angka < 2) return false;
  for (let i = 2; i < angka; i++) {
    if (angka % i === 0) return false;
  }
  return true;
}

console.log(isPrima(7));
console.log(isPrima(10));
```

**Hasil yang diharapkan:**
```
true
false
```

---

# Assignment 5 - Konversi Nilai ke Grade (Easy)
Buat program konversi nilai angka menjadi huruf (grade) menggunakan function dan if-else.

```js
function konversiGrade(nilai) {
  if (nilai >= 90) return "A";
  if (nilai >= 80) return "B";
  if (nilai >= 70) return "C";
  return "D";
}

console.log(konversiGrade(85));
```

**Hasil yang diharapkan:**
```
B
```

---

# Assignment 6 - CRUD Data Buku (Medium)
Buat program manajemen data buku (tambah, edit, hapus) menggunakan array of objects.

```js
let bukuList = [];

function tambahBuku(judul, penulis, tahun) {
  bukuList.push({ judul, penulis, tahun });
}

function editBuku(judul, dataBaru) {
  let buku = bukuList.find((b) => b.judul === judul);
  if (buku) Object.assign(buku, dataBaru);
}

function hapusBuku(judul) {
  bukuList = bukuList.filter((b) => b.judul !== judul);
}

tambahBuku("Laskar Pelangi", "Andrea Hirata", 2005);
editBuku("Laskar Pelangi", { tahun: 2006 });
console.log(bukuList);
```

**Hasil yang diharapkan:**
```
[ { judul: 'Laskar Pelangi', penulis: 'Andrea Hirata', tahun: 2006 } ]
```

---

# Assignment 7 - Pencarian Buku (Medium)
Buat program pencarian buku berdasarkan judul dari daftar array of objects yang sudah dibuat sebelumnya.

```js
let bukuList = [
  { judul: "Laskar Pelangi", penulis: "Andrea Hirata" },
  { judul: "Bumi Manusia", penulis: "Pramoedya" },
];

function cariBuku(judul) {
  return bukuList.find((b) => b.judul.toLowerCase() === judul.toLowerCase());
}

console.log(cariBuku("bumi manusia"));
```

**Hasil yang diharapkan:**
```
{ judul: 'Bumi Manusia', penulis: 'Pramoedya' }
```

---

# Assignment 8 - Kalkulator Kasir (Hard)
Buat mini project kalkulator kasir sederhana: menerima beberapa barang (nama, harga, jumlah), menghitung total belanja, menerapkan diskon jika total di atas nominal tertentu, dan menampilkan struk belanja.

```js
let keranjang = [
  { nama: "Kopi", harga: 20000, jumlah: 2 },
  { nama: "Roti", harga: 15000, jumlah: 3 },
];

let total = keranjang.reduce((acc, item) => acc + item.harga * item.jumlah, 0);
let diskon = total > 100000 ? total * 0.1 : 0;
let totalAkhir = total - diskon;

console.log("=== STRUK BELANJA ===");
keranjang.forEach((item) =>
  console.log(`${item.nama} x${item.jumlah} = ${item.harga * item.jumlah}`)
);
console.log("Total:", total);
console.log("Diskon:", diskon);
console.log("Total Akhir:", totalAkhir);
```

**Hasil yang diharapkan:**
```
=== STRUK BELANJA ===
Kopi x2 = 40000
Roti x3 = 45000
Total: 85000
Diskon: 0
Total Akhir: 85000
```
