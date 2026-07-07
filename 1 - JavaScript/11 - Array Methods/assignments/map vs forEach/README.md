# Assignment - Transformasi Data dengan `map()` (Easy)

## Tujuan Pembelajaran

- Memahami fungsi method `map()` pada array.
- Mampu mentransformasikan setiap elemen array menjadi nilai baru.
- Memahami bahwa `map()` selalu menghasilkan array baru.
- Mampu menggunakan callback function pada method `map()`.

## Soal

Buatlah sebuah function berikut.

```javascript
const squareNumbers = (numbers) => {
  // code here
};
```

Function menerima sebuah parameter berupa array angka.

Gunakan method **`map()`** untuk mengubah setiap angka menjadi **hasil kuadratnya**, kemudian kembalikan array baru yang berisi hasil transformasi tersebut.

> **Catatan:** Fokus utama assignment ini adalah memahami cara kerja method `map()` dalam mentransformasikan setiap elemen array tanpa mengubah array asli.

### Validasi

- Jika `numbers` bukan array, tampilkan `"Parameter harus berupa array."`
- Jika array kosong, kembalikan array kosong (`[]`).
- Jika terdapat elemen yang bukan number, tampilkan `"Seluruh elemen harus berupa number."`

---

## Result / Test Case

```javascript
// Test Case 1
squareNumbers([1, 2, 3, 4]);

// Output
[1, 4, 9, 16];

// Test Case 2
squareNumbers([5, 6]);

// Output
[25, 36];

// Test Case 3
squareNumbers([]);

// Output
[];

// Test Case 4
squareNumbers([1, "2", 3]);

// Output
("Seluruh elemen harus berupa number.");

// Test Case 5
squareNumbers("Hello");

// Output
("Parameter harus berupa array.");
```
