# Tujuan Pembelajaran
- Mampu menggunakan if, else if, dan else
- Mampu menggunakan switch case
- Memahami nested condition
- Mampu menggabungkan beberapa kondisi dalam satu logika

---

# Assignment 1 - Positif Negatif Nol (Easy)
Buat kode untuk menentukan apakah sebuah angka positif, negatif, atau nol.

```js
let angka = -3;

if (angka > 0) {
  console.log("Positif");
} else if (angka < 0) {
  console.log("Negatif");
} else {
  console.log("Nol");
}
```

**Hasil yang diharapkan:**
```
Negatif
```

---

# Assignment 2 - Switch Hari (Easy)
Gunakan `switch` untuk menampilkan nama hari berdasarkan angka 1-7.

```js
let hari = 3;

switch (hari) {
  case 1:
    console.log("Senin");
    break;
  case 2:
    console.log("Selasa");
    break;
  case 3:
    console.log("Rabu");
    break;
  default:
    console.log("Hari tidak valid");
}
```

**Hasil yang diharapkan:**
```
Rabu
```

---

# Assignment 3 - If Tanpa Else (Easy)
Buat kode if tanpa else untuk memberi peringatan jika stok barang di bawah 10.

```js
let stok = 5;

if (stok < 10) {
  console.log("Stok menipis!");
}
```

**Hasil yang diharapkan:**
```
Stok menipis!
```

---

# Assignment 4 - Nested If (Easy)
Buat nested if untuk mengecek kelayakan mendaftar SIM (umur >= 17 dan punya KTP).

```js
let umur = 18;
let punyaKTP = true;

if (umur >= 17) {
  if (punyaKTP) {
    console.log("Boleh mendaftar SIM");
  } else {
    console.log("Wajib punya KTP dulu");
  }
} else {
  console.log("Umur belum cukup");
}
```

**Hasil yang diharapkan:**
```
Boleh mendaftar SIM
```

---

# Assignment 5 - Habis Dibagi 2 dan 3 (Easy)
Cek apakah suatu angka habis dibagi 2 dan 3 sekaligus.

```js
let angka = 12;

if (angka % 2 === 0 && angka % 3 === 0) {
  console.log(angka + " habis dibagi 2 dan 3");
} else {
  console.log(angka + " tidak habis dibagi keduanya");
}
```

**Hasil yang diharapkan:**
```
12 habis dibagi 2 dan 3
```

---

# Assignment 6 - Kategori Nilai (Medium)
Buat program untuk menentukan kategori nilai (A, B, C, D) berdasarkan skor menggunakan if-else if.

```js
let skor = 82;

if (skor >= 90) {
  console.log("A");
} else if (skor >= 80) {
  console.log("B");
} else if (skor >= 70) {
  console.log("C");
} else {
  console.log("D");
}
```

**Hasil yang diharapkan:**
```
B
```

---

# Assignment 7 - If-Else ke Switch Case (Medium)
Ubah program kategori nilai berbentuk if-else menjadi bentuk switch case menggunakan pembulatan puluhan sebagai case.

```js
let skor = 82;
let puluhan = Math.floor(skor / 10);

switch (true) {
  case puluhan >= 9:
    console.log("A");
    break;
  case puluhan === 8:
    console.log("B");
    break;
  case puluhan === 7:
    console.log("C");
    break;
  default:
    console.log("D");
}
```

**Hasil yang diharapkan:**
```
B
```

---

# Assignment 8 - Jumlah Hari dalam Bulan (Hard)
Buat program untuk menentukan jumlah hari dalam sebuah bulan, termasuk logika tahun kabisat untuk Februari.

```js
let bulan = 2;
let tahun = 2024;
let jumlahHari;

if ([1, 3, 5, 7, 8, 10, 12].includes(bulan)) {
  jumlahHari = 31;
} else if ([4, 6, 9, 11].includes(bulan)) {
  jumlahHari = 30;
} else {
  let kabisat = (tahun % 4 === 0 && tahun % 100 !== 0) || tahun % 400 === 0;
  jumlahHari = kabisat ? 29 : 28;
}

console.log(jumlahHari);
```

**Hasil yang diharapkan:**
```
29
```
