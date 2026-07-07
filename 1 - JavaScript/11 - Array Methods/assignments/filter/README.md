# Assignment - Filter Angka Genap (Easy)

## Tujuan Pembelajaran

- Memahami fungsi method `filter()` pada array.
- Mampu menyaring data berdasarkan suatu kondisi.
- Mampu menggunakan callback function pada method `filter()`.
- Mampu mengembalikan array baru hasil proses filtering.

## Soal

Buatlah sebuah function berikut.

```javascript
const getEvenNumbers = (numbers) => {
  // code here
};
```

Function menerima sebuah parameter berupa array angka, kemudian gunakan method **`filter()`** untuk mengambil **hanya bilangan genap**.

Function harus mengembalikan array baru yang berisi seluruh angka genap.

> **Catatan:** Fokus utama assignment ini adalah memahami cara kerja method `filter()` untuk menyaring elemen array berdasarkan suatu kondisi.

### Validasi

- Jika `numbers` bukan array, tampilkan `"Parameter harus berupa array."`
- Jika array kosong, kembalikan array kosong (`[]`).
- Jika array tidak memiliki bilangan genap, kembalikan array kosong (`[]`).

---

## Result / Test Case

```javascript
// Test Case 1
getEvenNumbers([1, 2, 3, 4, 5, 6]);

// Output
[2, 4, 6];

// Test Case 2
getEvenNumbers([10, 15, 20, 25]);

// Output
[10, 20];

// Test Case 3
getEvenNumbers([1, 3, 5]);

// Output
[];

// Test Case 4
getEvenNumbers([]);

// Output
[];

// Test Case 5
getEvenNumbers("Hello");

// Output
("Parameter harus berupa array.");
```
