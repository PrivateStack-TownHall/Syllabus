# Assignment - Spread Operator pada Array (Easy)

## Tujuan Pembelajaran

- Memahami konsep **spread operator (`...`)** pada array.
- Mampu menggabungkan dua array menjadi satu array baru.
- Memahami bahwa spread operator menghasilkan array baru tanpa mengubah array asli.
- Mampu menggunakan spread operator untuk menyederhanakan manipulasi array.

## Soal

Buatlah sebuah function berikut.

```javascript
const mergeArrays = (arr1, arr2) => {
  // code here
};
```

Function menerima dua parameter berupa array, kemudian gabungkan kedua array tersebut menggunakan **spread operator (`...`)**.

Function harus mengembalikan sebuah array baru yang berisi seluruh elemen dari kedua array.

> **Catatan:** Fokus utama assignment ini adalah memahami cara kerja **spread operator** dalam menggabungkan beberapa array menjadi satu array baru.

### Validasi

- Jika `arr1` bukan array, tampilkan `"Parameter pertama harus berupa array."`
- Jika `arr2` bukan array, tampilkan `"Parameter kedua harus berupa array."`
- Jika kedua parameter berupa array kosong, kembalikan array kosong (`[]`).

---

## Result / Test Case

```javascript
// Test Case 1
mergeArrays(["Apel", "Jeruk"], ["Mangga", "Anggur"]);

// Output
["Apel", "Jeruk", "Mangga", "Anggur"];

// Test Case 2
mergeArrays([1, 2, 3], [4, 5]);

// Output
[1, 2, 3, 4, 5];

// Test Case 3
mergeArrays([], ["Mangga"]);

// Output
["Mangga"];

// Test Case 4
mergeArrays([], []);

// Output
[];

// Test Case 5
mergeArrays("Hello", ["Mangga"]);

// Output
("Parameter pertama harus berupa array.");
```
