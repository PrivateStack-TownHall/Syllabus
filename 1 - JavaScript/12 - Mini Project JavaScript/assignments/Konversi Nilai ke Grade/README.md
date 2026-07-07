# Assignment - Konversi Nilai ke Grade (Easy)

## Tujuan Pembelajaran

- Mampu membuat function dengan parameter dan nilai kembalian.
- Mampu menggunakan percabangan `if...else if...else`.
- Mampu mengonversi nilai angka menjadi grade huruf.
- Mampu menerapkan validasi sederhana pada input.

## Soal

Buatlah sebuah function berikut.

```javascript
const getGrade = (score) => {
  // code here
};
```

Function menerima satu parameter berupa nilai (`score`), kemudian mengembalikan grade berdasarkan ketentuan berikut.

| Nilai    | Grade |
| -------- | ----- |
| 90 - 100 | A     |
| 80 - 89  | B     |
| 70 - 79  | C     |
| 60 - 69  | D     |
| 0 - 59   | E     |

> **Catatan:** Fokus utama assignment ini adalah memahami penggunaan `if...else if...else` untuk menentukan grade berdasarkan rentang nilai.

### Validasi

- Jika `score` bukan number, tampilkan `"Nilai harus berupa number."`
- Jika `score` kurang dari `0` atau lebih dari `100`, tampilkan `"Nilai harus berada di antara 0 dan 100."`

---

## Result / Test Case

```javascript
// Test Case 1
getGrade(85);

// Output
("B");

// Test Case 2
getGrade(95);

// Output
("A");

// Test Case 3
getGrade(70);

// Output
("C");

// Test Case 4
getGrade(120);

// Output
("Nilai harus berada di antara 0 dan 100.");

// Test Case 5
getGrade("85");

// Output
("Nilai harus berupa number.");
```
