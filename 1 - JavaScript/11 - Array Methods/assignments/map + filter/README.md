# Assignment - Kombinasi `map()` dan `filter()` (Medium)

## Tujuan Pembelajaran

- Memahami cara menggabungkan method `filter()` dan `map()`.
- Mampu melakukan penyaringan data berdasarkan suatu kondisi.
- Mampu melakukan transformasi data menggunakan `map()`.
- Mampu menyelesaikan permasalahan menggunakan kombinasi beberapa array method.

## Soal

Buatlah sebuah function berikut.

```javascript
const getPassedStudents = (students) => {
  // code here
};
```

Function menerima sebuah parameter berupa **array of object** dengan struktur seperti berikut.

```javascript
[
  {
    name: "Ani",
    score: 90,
  },
];
```

Gunakan kombinasi method **`filter()`** dan **`map()`** untuk mengambil **nama siswa** yang memiliki nilai **lebih dari 80**.

Function harus mengembalikan sebuah array yang hanya berisi nama siswa yang memenuhi syarat.

> **Catatan:** Fokus utama assignment ini adalah memahami cara menggabungkan `filter()` untuk menyaring data dan `map()` untuk mentransformasikan hasilnya menjadi array baru.

### Validasi

- Jika `students` bukan array, tampilkan `"Parameter harus berupa array."`
- Jika array kosong, kembalikan array kosong (`[]`).
- Jika salah satu data tidak memiliki properti `name` atau `score`, tampilkan `"Data student tidak valid."`

---

## Result / Test Case

```javascript
// Test Case 1
getPassedStudents([
  { name: "Ani", score: 90 },
  { name: "Budi", score: 75 },
  { name: "Cici", score: 85 },
]);

// Output
["Ani", "Cici"];

// Test Case 2
getPassedStudents([
  { name: "Doni", score: 88 },
  { name: "Eka", score: 92 },
]);

// Output
["Doni", "Eka"];

// Test Case 3
getPassedStudents([
  { name: "Budi", score: 70 },
  { name: "Rina", score: 80 },
]);

// Output
[];

// Test Case 4
getPassedStudents([{ name: "Ani" }]);

// Output
("Data student tidak valid.");

// Test Case 5
getPassedStudents("Hello");

// Output
("Parameter harus berupa array.");
```
