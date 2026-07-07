# Assignment - Menjumlahkan Nilai dengan `reduce()` (Medium)

## Tujuan Pembelajaran

- Memahami fungsi method `reduce()` pada array.
- Mampu menggabungkan seluruh elemen array menjadi satu nilai.
- Memahami konsep accumulator pada `reduce()`.
- Mampu menggunakan callback function untuk melakukan perhitungan.

## Soal

Buatlah sebuah function berikut.

```javascript
const calculateTotal = (numbers) => {
  // code here
};
```

Function menerima sebuah parameter berupa array angka.

Gunakan method **`reduce()`** untuk menghitung total seluruh elemen dalam array, kemudian kembalikan hasilnya.

> **Catatan:** Fokus utama assignment ini adalah memahami cara kerja **`reduce()`** dalam menggabungkan seluruh elemen array menjadi satu nilai.

### Validasi

- Jika `numbers` bukan array, tampilkan `"Parameter harus berupa array."`
- Jika array kosong, kembalikan `0`.
- Jika terdapat elemen yang bukan number, tampilkan `"Seluruh elemen harus berupa number."`

---

## Result / Test Case

```javascript
// Test Case 1
calculateTotal([10, 20, 30, 40]);

// Output
100;

// Test Case 2
calculateTotal([5, 10, 15]);

// Output
30;

// Test Case 3
calculateTotal([]);

// Output
0;

// Test Case 4
calculateTotal([10, "20", 30]);

// Output
("Seluruh elemen harus berupa number.");

// Test Case 5
calculateTotal("Hello");

// Output
("Parameter harus berupa array.");
```
