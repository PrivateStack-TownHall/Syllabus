# Tujuan Pembelajaran
- Memahami apa itu JavaScript dan perannya dalam web development
- Mampu menuliskan dan menjalankan kode JavaScript dasar
- Memahami perbedaan var, let, dan const
- Memahami konsep dasar asynchronous JavaScript

---

# Assignment 1 - Hello World (Easy)
Tampilkan teks "Hello, Sekolah Stack!" ke console.

```js
console.log("Hello, Sekolah Stack!");
```

**Hasil yang diharapkan:**
```
Hello, Sekolah Stack!
```

---

# Assignment 2 - Deklarasi Variabel (Easy)
Buat 3 variabel: `nama` (string), `umur` (number), `isMember` (boolean), lalu tampilkan ketiganya.

```js
let nama = "Vincent";
let umur = 25;
let isMember = true;

console.log(nama, umur, isMember);
```

**Hasil yang diharapkan:**
```
Vincent 25 true
```

---

# Assignment 3 - Komentar Kode (Easy)
Tambahkan komentar satu baris dan komentar banyak baris untuk menjelaskan kode di bawah ini.

```js
// TODO: tambahkan komentar di sini
let harga = 15000;
/*
  TODO: tambahkan komentar
  banyak baris di sini
*/
console.log(harga);
```

**Hasil yang diharapkan:**
```
15000
```

---

# Assignment 4 - var vs let vs const (Easy)
Buktikan apa yang terjadi jika variabel `const` dicoba diubah nilainya.

```js
const PI = 3.14;
PI = 3.14159; // coba jalankan baris ini
```

**Hasil yang diharapkan:**
```
TypeError: Assignment to constant variable.
```

---

# Assignment 5 - Statement vs Expression (Easy)
Buatlah satu contoh statement dan satu contoh expression, lalu jelaskan perbedaannya lewat komentar.

```js
// statement
if (true) {
  console.log("ini statement");
}

// expression
let hasil = 5 + 3;
```

**Hasil yang diharapkan:**
```
ini statement
```

---

# Assignment 6 - Client-side vs Server-side (Medium)
Buat contoh kode sederhana yang menunjukkan JavaScript berjalan di browser (client-side), lalu jelaskan perbedaannya dengan Node.js (server-side) dalam komentar.

```js
// client-side: dijalankan di browser
document.getElementById("btn").addEventListener("click", () => {
  alert("Diklik dari browser!");
});
```

**Hasil yang diharapkan:**
```
(muncul alert "Diklik dari browser!" saat tombol diklik di browser)
```

---

# Assignment 7 - Data Type Check (Medium)
Buat beberapa variabel dengan tipe data berbeda, lalu cek tipe datanya menggunakan `typeof`.

```js
let a = "Sekolah Stack";
let b = 100;
let c = true;
let d;

console.log(typeof a, typeof b, typeof c, typeof d);
```

**Hasil yang diharapkan:**
```
string number boolean undefined
```

---

# Assignment 8 - Asynchronous Sederhana (Hard)
Jelaskan konsep single-threaded pada JavaScript menggunakan `setTimeout`, lalu tebak urutan output-nya sebelum dijalankan.

```js
console.log("Mulai");

setTimeout(() => {
  console.log("Proses async selesai");
}, 1000);

console.log("Selesai");
```

**Hasil yang diharapkan:**
```
Mulai
Selesai
Proses async selesai
```
