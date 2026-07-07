# Assignment - Menampilkan Data dengan `forEach()` (Easy)

## Tujuan Pembelajaran

- Memahami fungsi method `forEach()` pada array.
- Mampu melakukan iterasi terhadap setiap elemen array.
- Mampu menggunakan callback function pada method `forEach()`.
- Memahami bahwa `forEach()` digunakan untuk menjalankan aksi pada setiap elemen array.

## Soal

Buatlah sebuah function berikut.

```javascript
const printFruits = (fruits) => {
  // code here
};
```

Function menerima sebuah parameter berupa array yang berisi nama buah.

Gunakan method **`forEach()`** untuk menampilkan setiap elemen array ke console.

> **Catatan:** Fokus utama assignment ini adalah memahami cara kerja method `forEach()` untuk melakukan iterasi pada setiap elemen array.

### Validasi

- Jika `fruits` bukan array, tampilkan `"Parameter harus berupa array."`
- Jika array kosong, tampilkan `"Array kosong."`

---

## Result / Test Case

```javascript
// Test Case 1
printFruits(["Apel", "Jeruk", "Mangga"]);

// Output
Apel;
Jeruk;
Mangga;

// Test Case 2
printFruits(["Semangka", "Melon"]);

// Output
Semangka;
Melon;

// Test Case 3
printFruits([]);

// Output
("Array kosong.");

// Test Case 4
printFruits("Hello");

// Output
("Parameter harus berupa array.");
```
