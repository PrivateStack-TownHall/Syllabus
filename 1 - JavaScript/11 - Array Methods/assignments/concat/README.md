# Assignment - Menggabungkan Array dengan `concat()` (Easy)

## Tujuan Pembelajaran

- Memahami fungsi method `concat()` pada array.
- Mampu menggabungkan dua array menjadi array baru.
- Memahami bahwa `concat()` tidak mengubah array asli.
- Mampu menggunakan method `concat()` untuk memanipulasi array.

## Soal

Buatlah sebuah function berikut.

```javascript
const mergeArrays = (arr1, arr2) => {
  // code here
};
```

Function menerima dua parameter berupa array, kemudian gabungkan kedua array tersebut menggunakan method **`concat()`**.

Function harus mengembalikan sebuah array baru yang berisi seluruh elemen dari kedua array.

> **Catatan:** Fokus utama assignment ini adalah memahami cara kerja method `concat()` dalam menggabungkan dua array tanpa mengubah array aslinya.

### Validasi

- Jika `arr1` bukan array, tampilkan `"Parameter pertama harus berupa array."`
- Jika `arr2` bukan array, tampilkan `"Parameter kedua harus berupa array."`
- Jika kedua parameter berupa array kosong, kembalikan array kosong (`[]`).

---

## Result / Test Case

```javascript
// Test Case 1
mergeArrays([1, 2, 3], [4, 5, 6]);

// Output
[1, 2, 3, 4, 5, 6];

// Test Case 2
mergeArrays(["Apel"], ["Jeruk", "Mangga"]);

// Output
["Apel", "Jeruk", "Mangga"];

// Test Case 3
mergeArrays([], [1, 2]);

// Output
[1, 2];

// Test Case 4
mergeArrays([], []);

// Output
[];

// Test Case 5
mergeArrays("Hello", [1, 2]);

// Output
("Parameter pertama harus berupa array.");
```
