# Tujuan Pembelajaran
- Mampu membuat dan mengakses object literal
- Memahami dot notation dan bracket notation
- Mampu memanipulasi properti object (tambah, hapus, ubah)
- Mampu melakukan deep clone terhadap nested object

---

# Assignment 1 - Object Literal (Easy)
Buat object literal dengan properti nama, umur, dan pekerjaan.

```js
let siswa = {
  nama: "Vincent",
  umur: 25,
  pekerjaan: "Frontend Developer",
};

console.log(siswa);
```

**Hasil yang diharapkan:**
```
{ nama: 'Vincent', umur: 25, pekerjaan: 'Frontend Developer' }
```

---

# Assignment 2 - Dot vs Bracket Notation (Easy)
Akses properti `nama` menggunakan dot notation dan bracket notation.

```js
let siswa = { nama: "Vincent", umur: 25 };

console.log(siswa.nama);
console.log(siswa["nama"]);
```

**Hasil yang diharapkan:**
```
Vincent
Vincent
```

---

# Assignment 3 - Menambah Properti (Easy)
Tambahkan properti baru `email` ke dalam object yang sudah ada.

```js
let siswa = { nama: "Vincent", umur: 25 };
siswa.email = "vincent@email.com";

console.log(siswa);
```

**Hasil yang diharapkan:**
```
{ nama: 'Vincent', umur: 25, email: 'vincent@email.com' }
```

---

# Assignment 4 - Menghapus Properti (Easy)
Hapus properti `umur` dari object menggunakan `delete`.

```js
let siswa = { nama: "Vincent", umur: 25 };
delete siswa.umur;

console.log(siswa);
```

**Hasil yang diharapkan:**
```
{ nama: 'Vincent' }
```

---

# Assignment 5 - Object.keys() (Easy)
Tampilkan seluruh nama properti (key) dari sebuah object menggunakan `Object.keys()`.

```js
let siswa = { nama: "Vincent", umur: 25, kelas: "12A" };

console.log(Object.keys(siswa));
```

**Hasil yang diharapkan:**
```
[ 'nama', 'umur', 'kelas' ]
```

---

# Assignment 6 - Object dengan Method (Medium)
Buat object `mobil` yang memiliki method `nyalakanMesin()`.

```js
let mobil = {
  merk: "Toyota",
  nyalakanMesin: function () {
    console.log(this.merk + ": Mesin menyala!");
  },
};

mobil.nyalakanMesin();
```

**Hasil yang diharapkan:**
```
Toyota: Mesin menyala!
```

---

# Assignment 7 - keys, values, entries (Medium)
Tampilkan hasil dari `Object.keys()`, `Object.values()`, dan `Object.entries()` untuk object yang sama.

```js
let produk = { nama: "Mouse", harga: 150000 };

console.log(Object.keys(produk));
console.log(Object.values(produk));
console.log(Object.entries(produk));
```

**Hasil yang diharapkan:**
```
[ 'nama', 'harga' ]
[ 'Mouse', 150000 ]
[ [ 'nama', 'Mouse' ], [ 'harga', 150000 ] ]
```

---

# Assignment 8 - Deep Clone Manual (Hard)
Buat function untuk melakukan deep clone terhadap object yang memiliki nested object, tanpa menggunakan library eksternal.

```js
function deepClone(obj) {
  if (typeof obj !== "object" || obj === null) return obj;

  let clone = Array.isArray(obj) ? [] : {};
  for (let key in obj) {
    clone[key] = deepClone(obj[key]);
  }
  return clone;
}

let asli = { nama: "Vincent", alamat: { kota: "Bekasi" } };
let salinan = deepClone(asli);
salinan.alamat.kota = "Jakarta";

console.log(asli.alamat.kota);
console.log(salinan.alamat.kota);
```

**Hasil yang diharapkan:**
```
Bekasi
Jakarta
```
