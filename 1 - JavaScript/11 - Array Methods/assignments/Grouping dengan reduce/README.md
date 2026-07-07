# Assignment - Mengelompokkan Data dengan `reduce()` (Hard)

## Tujuan Pembelajaran

- Memahami fungsi method `reduce()` pada array.
- Mampu mengubah array menjadi object menggunakan `reduce()`.
- Mampu mengelompokkan data berdasarkan suatu properti.
- Mampu menyelesaikan permasalahan transformasi data menggunakan `reduce()`.

## Soal

Buatlah sebuah function berikut.

```javascript
const groupStudentsByClass = (students) => {
  // code here
};
```

Function menerima sebuah parameter berupa **array of object** dengan struktur berikut.

```javascript
[
  {
    name: "Ani",
    class: "12A",
  },
];
```

Gunakan method **`reduce()`** untuk mengelompokkan nama siswa berdasarkan kelas.

Function harus mengembalikan sebuah object dengan format berikut.

```javascript
{
  "12A": ["Ani", "Cici"],
  "12B": ["Budi"],
}
```

> **Catatan:** Fokus utama assignment ini adalah memahami bagaimana `reduce()` dapat digunakan untuk mengubah sebuah array menjadi object yang dikelompokkan berdasarkan suatu properti.

### Validasi

- Jika `students` bukan array, tampilkan `"Parameter harus berupa array."`
- Jika array kosong, kembalikan object kosong (`{}`).
- Jika salah satu data tidak memiliki properti `name` atau `class`, tampilkan `"Data student tidak valid."`

---

## Result / Test Case

```javascript
// Test Case 1
groupStudentsByClass([
  { name: "Ani", class: "12A" },
  { name: "Budi", class: "12B" },
  { name: "Cici", class: "12A" },
]);

// Output
{
  "12A": ["Ani", "Cici"],
  "12B": ["Budi"],
}


// Test Case 2
groupStudentsByClass([
  { name: "Doni", class: "11A" },
  { name: "Eka", class: "11A" },
]);

// Output
{
  "11A": ["Doni", "Eka"],
}


// Test Case 3
groupStudentsByClass([]);

// Output
{}


// Test Case 4
groupStudentsByClass([
  { name: "Ani" },
]);

// Output
"Data student tidak valid."


// Test Case 5
groupStudentsByClass("Hello");

// Output
"Parameter harus berupa array."
```
