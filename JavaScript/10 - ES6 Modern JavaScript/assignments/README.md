# Tujuan Pembelajaran
- Mampu menggunakan arrow function, template literal, dan destructuring
- Memahami spread dan rest operator
- Mampu menggunakan default dan rest parameter secara bersamaan
- Memahami penggabungan object menggunakan spread operator

---

# Assignment 1 - Arrow Function (Easy)
Ubah function biasa berikut menjadi arrow function.

```js
// function biasa
function kali(a, b) {
  return a * b;
}

// arrow function
const kaliArrow = (a, b) => a * b;

console.log(kaliArrow(4, 5));
```

**Hasil yang diharapkan:**
```
20
```

---

# Assignment 2 - Template Literal (Easy)
Gabungkan string dan variabel menggunakan template literal.

```js
let nama = "Vincent";
let umur = 25;

console.log(`Halo, nama saya ${nama} dan umur saya ${umur} tahun.`);
```

**Hasil yang diharapkan:**
```
Halo, nama saya Vincent dan umur saya 25 tahun.
```

---

# Assignment 3 - Destructuring (Easy)
Lakukan destructuring pada array dan object berikut.

```js
let angka = [1, 2, 3];
let [a, b, c] = angka;
console.log(a, b, c);

let siswa = { nama: "Vincent", umur: 25 };
let { nama, umur } = siswa;
console.log(nama, umur);
```

**Hasil yang diharapkan:**
```
1 2 3
Vincent 25
```

---

# Assignment 4 - Spread Operator pada Array (Easy)
Gabungkan dua array menggunakan spread operator.

```js
let buah1 = ["Apel", "Jeruk"];
let buah2 = ["Mangga", "Anggur"];
let semuaBuah = [...buah1, ...buah2];

console.log(semuaBuah);
```

**Hasil yang diharapkan:**
```
[ 'Apel', 'Jeruk', 'Mangga', 'Anggur' ]
```

---

# Assignment 5 - let/const vs var (Easy)
Tunjukkan contoh sederhana perbedaan block scope `let`/`const` dengan `var`.

```js
{
  var a = "var";
  let b = "let";
}

console.log(a);
// console.log(b); // error karena b hanya ada di dalam block
```

**Hasil yang diharapkan:**
```
var
```

---

# Assignment 6 - Default & Rest Parameter (Medium)
Buat function dengan default parameter dan rest parameter sekaligus.

```js
function buatPesan(judul = "Info", ...isi) {
  console.log(judul + ": " + isi.join(", "));
}

buatPesan("Pengumuman", "Libur", "Besok", "Ujian");
```

**Hasil yang diharapkan:**
```
Pengumuman: Libur, Besok, Ujian
```

---

# Assignment 7 - Destructuring dengan Renaming (Medium)
Lakukan destructuring pada object dengan mengganti nama variabel hasil destructuring.

```js
let siswa = { nama: "Vincent", kelas: "12A" };
let { nama: namaSiswa, kelas: kelasSiswa } = siswa;

console.log(namaSiswa, kelasSiswa);
```

**Hasil yang diharapkan:**
```
Vincent 12A
```

---

# Assignment 8 - Merge Object dengan Spread (Hard)
Gabungkan dua object yang memiliki properti sama menggunakan spread operator, lalu jelaskan properti mana yang menang.

```js
let default_ = { warna: "Merah", ukuran: "M" };
let custom = { warna: "Biru" };

let hasil = { ...default_, ...custom };

console.log(hasil);
```

**Hasil yang diharapkan:**
```
{ warna: 'Biru', ukuran: 'M' }
```
