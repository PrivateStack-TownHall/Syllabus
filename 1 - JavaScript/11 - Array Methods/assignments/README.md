# Tujuan Pembelajaran
- Mampu menggunakan forEach, map, dan filter
- Mampu menggunakan find dan findIndex
- Memahami cara kerja reduce
- Mampu menggabungkan beberapa array method untuk transformasi data

---

# Assignment 1 - forEach (Easy)
Gunakan `forEach()` untuk mencetak setiap elemen array.

```js
let buah = ["Apel", "Jeruk", "Mangga"];

buah.forEach((item) => console.log(item));
```

**Hasil yang diharapkan:**
```
Apel
Jeruk
Mangga
```

---

# Assignment 2 - map vs forEach (Easy)
Gunakan `map()` untuk membuat array baru berisi hasil kuadrat dari setiap elemen.

```js
let angka = [1, 2, 3, 4];
let kuadrat = angka.map((n) => n * n);

console.log(kuadrat);
```

**Hasil yang diharapkan:**
```
[ 1, 4, 9, 16 ]
```

---

# Assignment 3 - filter (Easy)
Gunakan `filter()` untuk mendapatkan hanya angka genap dari sebuah array.

```js
let angka = [1, 2, 3, 4, 5, 6];
let genap = angka.filter((n) => n % 2 === 0);

console.log(genap);
```

**Hasil yang diharapkan:**
```
[ 2, 4, 6 ]
```

---

# Assignment 4 - find dan findIndex (Easy)
Gunakan `find()` dan `findIndex()` untuk mencari siswa dengan nama "Budi".

```js
let siswa = [{ nama: "Ani" }, { nama: "Budi" }, { nama: "Cici" }];

console.log(siswa.find((s) => s.nama === "Budi"));
console.log(siswa.findIndex((s) => s.nama === "Budi"));
```

**Hasil yang diharapkan:**
```
{ nama: 'Budi' }
1
```

---

# Assignment 5 - concat (Easy)
Gabungkan dua array menggunakan `concat()`.

```js
let arr1 = [1, 2, 3];
let arr2 = [4, 5, 6];
let gabungan = arr1.concat(arr2);

console.log(gabungan);
```

**Hasil yang diharapkan:**
```
[ 1, 2, 3, 4, 5, 6 ]
```

---

# Assignment 6 - reduce untuk Total (Medium)
Gunakan `reduce()` untuk menjumlahkan semua elemen dalam array.

```js
let angka = [10, 20, 30, 40];
let total = angka.reduce((acc, curr) => acc + curr, 0);

console.log(total);
```

**Hasil yang diharapkan:**
```
100
```

---

# Assignment 7 - map + filter (Medium)
Gunakan kombinasi `map()` dan `filter()` untuk mengambil nama siswa yang nilainya di atas 80.

```js
let siswa = [
  { nama: "Ani", nilai: 90 },
  { nama: "Budi", nilai: 75 },
  { nama: "Cici", nilai: 85 },
];

let namaLulus = siswa.filter((s) => s.nilai > 80).map((s) => s.nama);

console.log(namaLulus);
```

**Hasil yang diharapkan:**
```
[ 'Ani', 'Cici' ]
```

---

# Assignment 8 - Grouping dengan reduce (Hard)
Gunakan `reduce()` untuk mengelompokkan siswa berdasarkan kelas.

```js
let siswa = [
  { nama: "Ani", kelas: "12A" },
  { nama: "Budi", kelas: "12B" },
  { nama: "Cici", kelas: "12A" },
];

let hasil = siswa.reduce((acc, curr) => {
  if (!acc[curr.kelas]) acc[curr.kelas] = [];
  acc[curr.kelas].push(curr.nama);
  return acc;
}, {});

console.log(hasil);
```

**Hasil yang diharapkan:**
```
{ '12A': [ 'Ani', 'Cici' ], '12B': [ 'Budi' ] }
```
