# Tujuan Pembelajaran
- Memahami tipe data primitif di JavaScript
- Mampu melakukan pengecekan tipe data menggunakan typeof
- Memahami konsep implicit type coercion
- Memahami perbedaan perbandingan == dan ===

---

# Assignment 1 - Tipe Data Primitif (Easy)
Buat variabel untuk masing-masing tipe data primitif: string, number, boolean, null, undefined.

```js
let namaTipe = "string";
let angka = 10;
let statusAktif = false;
let kosong = null;
let belumDiisi;

console.log(namaTipe, angka, statusAktif, kosong, belumDiisi);
```

**Hasil yang diharapkan:**
```
string 10 false null undefined
```

---

# Assignment 2 - Deklarasi Bertipe Data (Easy)
Deklarasikan variabel `nama` (string), `harga` (number), dan `tersedia` (boolean) untuk sebuah produk.

```js
let nama = "Keyboard Mechanical";
let harga = 750000;
let tersedia = true;

console.log(nama, harga, tersedia);
```

**Hasil yang diharapkan:**
```
Keyboard Mechanical 750000 true
```

---

# Assignment 3 - Cek typeof (Easy)
Cek hasil dari `typeof "Sekolah Stack"`.

```js
console.log(typeof "Sekolah Stack");
```

**Hasil yang diharapkan:**
```
string
```

---

# Assignment 4 - null vs undefined (Easy)
Buat variabel dengan nilai `null` dan variabel yang belum diberi nilai (undefined), lalu bandingkan keduanya.

```js
let a = null;
let b;

console.log(a, b);
console.log(a == b);
console.log(a === b);
```

**Hasil yang diharapkan:**
```
null undefined
true
false
```

---

# Assignment 5 - Mengecek Tipe Data (Easy)
Buat function untuk mengecek dan menampilkan tipe data dari sebuah variabel yang diberikan.

```js
function cekTipe(value) {
  console.log(typeof value);
}

cekTipe(100);
cekTipe("teks");
cekTipe(true);
```

**Hasil yang diharapkan:**
```
number
string
boolean
```

---

# Assignment 6 - Implicit Type Coercion (Medium)
Buat beberapa contoh operasi yang menunjukkan implicit type coercion, lalu jelaskan hasilnya dalam komentar.

```js
console.log("5" + 3);   // string + number
console.log("5" - 3);   // string - number
console.log(true + 1);  // boolean + number
```

**Hasil yang diharapkan:**
```
53
2
2
```

---

# Assignment 7 - Operasi Campuran Tipe Data (Medium)
Prediksi dan buktikan hasil dari operasi `"5" + 3` dan `"5" - 3` menggunakan console.log, lalu jelaskan alasannya dalam komentar.

```js
console.log("5" + 3); // digabung jadi string karena operator + dengan string
console.log("5" - 3); // dikonversi ke number karena operator -
```

**Hasil yang diharapkan:**
```
53
2
```

---

# Assignment 8 - Perbandingan == vs === (Hard)
Buat beberapa perbandingan menggunakan console.log untuk kombinasi nilai berbeda dengan `==` dan `===`, lalu simpulkan kenapa `===` lebih disarankan.

```js
console.log(0 == "0");           // ?
console.log(0 === "0");          // ?
console.log(null == undefined);  // ?
console.log(null === undefined); // ?
console.log(NaN == NaN);         // ?
```

**Hasil yang diharapkan:**
```
true
false
true
false
false
```
