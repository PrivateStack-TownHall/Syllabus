# Tujuan Pembelajaran
- Memahami penggunaan let, const, dan var beserta scope-nya
- Memahami konsep hoisting
- Mampu mendeklarasikan variabel dengan baik dan benar
- Memahami temporal dead zone (TDZ)

---

# Assignment 1 - let vs const (Easy)
Buat variabel dengan `let` dan `const`, lalu coba ubah nilainya untuk melihat perbedaannya.

```js
let umur = 20;
umur = 21;

const nama = "Vincent";
// nama = "Budi"; // akan error jika baris ini dijalankan

console.log(umur, nama);
```

**Hasil yang diharapkan:**
```
21 Vincent
```

---

# Assignment 2 - Deklarasi Variabel Nama & Umur (Easy)
Buat variabel `nama` dan `umur`, lalu tampilkan ke console dalam satu kalimat.

```js
let nama = "Vincent";
let umur = 25;

console.log(`Nama saya ${nama}, umur ${umur} tahun.`);
```

**Hasil yang diharapkan:**
```
Nama saya Vincent, umur 25 tahun.
```

---

# Assignment 3 - Tipe Data Objek (Easy)
Sebutkan dan buat contoh dari tipe data reference (object, array, function).

```js
let obj = { nama: "Vincent" };
let arr = [1, 2, 3];
let fn = function () {};

console.log(typeof obj, typeof arr, typeof fn);
```

**Hasil yang diharapkan:**
```
object object function
```

---

# Assignment 4 - Hoisting var (Easy)
Buktikan konsep hoisting pada `var` dengan memanggil variabel sebelum dideklarasikan.

```js
console.log(pesan); // apa hasilnya?
var pesan = "Halo Sekolah Stack";
console.log(pesan);
```

**Hasil yang diharapkan:**
```
undefined
Halo Sekolah Stack
```

---

# Assignment 5 - Multi Deklarasi (Easy)
Deklarasikan 3 variabel sekaligus dalam satu baris menggunakan `let`.

```js
let kota = "Bekasi", provinsi = "Jawa Barat", negara = "Indonesia";

console.log(kota, provinsi, negara);
```

**Hasil yang diharapkan:**
```
Bekasi Jawa Barat Indonesia
```

---

# Assignment 6 - Scope var, let, const (Medium)
Buat contoh kode yang menunjukkan perbedaan scope antara `var` dan `let` di dalam block `if`.

```js
if (true) {
  var a = "var di dalam block";
  let b = "let di dalam block";
}

console.log(a); // bisa diakses
console.log(b); // error, cek di console
```

**Hasil yang diharapkan:**
```
var di dalam block
ReferenceError: b is not defined
```

---

# Assignment 7 - Temporal Dead Zone (Medium)
Buktikan temporal dead zone dengan mengakses variabel `let` sebelum dideklarasikan.

```js
console.log(skor); // apa hasilnya?
let skor = 100;
```

**Hasil yang diharapkan:**
```
ReferenceError: Cannot access 'skor' before initialization
```

---

# Assignment 8 - Block Scope dalam Loop (Hard)
Buat dua buah loop `for`, satu menggunakan `var` dan satu menggunakan `let`, lalu simpan function di dalam array pada tiap iterasi. Jelaskan mengapa hasil akhirnya berbeda.

```js
let fnVar = [];
for (var i = 0; i < 3; i++) {
  fnVar.push(() => console.log("var:", i));
}
fnVar.forEach((fn) => fn());

let fnLet = [];
for (let j = 0; j < 3; j++) {
  fnLet.push(() => console.log("let:", j));
}
fnLet.forEach((fn) => fn());
```

**Hasil yang diharapkan:**
```
var: 3
var: 3
var: 3
let: 0
let: 1
let: 2
```
