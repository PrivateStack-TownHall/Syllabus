# Assignment - Mencari Data dengan `find()` dan `findIndex()` (Easy)

## Tujuan Pembelajaran

- Memahami fungsi method `find()` dan `findIndex()` pada array.
- Mampu mencari elemen berdasarkan suatu kondisi.
- Memahami perbedaan hasil yang dikembalikan oleh `find()` dan `findIndex()`.
- Mampu menggunakan callback function pada array method.

## Soal

Buatlah sebuah function berikut.

```javascript
const findStudent = (students, name) => {
  // code here
};
```

Function menerima dua parameter:

- `students` berupa array of object.
- `name` berupa nama siswa yang ingin dicari.

Gunakan method **`find()`** untuk mencari object siswa, kemudian gunakan **`findIndex()`** untuk mencari indeks siswa tersebut.

Function harus mengembalikan hasil pencarian dalam bentuk object berikut.

```javascript
{
  student,
  index,
}
```

> **Catatan:** Fokus utama assignment ini adalah memahami perbedaan penggunaan `find()` dan `findIndex()` dalam mencari data pada array.

### Validasi

- Jika `students` bukan array, tampilkan `"Parameter students harus berupa array."`
- Jika `name` bukan string atau string kosong, tampilkan `"Nama harus berupa string."`
- Jika data tidak ditemukan, tampilkan `"Siswa tidak ditemukan."`

---

## Result / Test Case

```javascript
// Test Case 1
findStudent(
  [
    { nama: "Andi" },
    { nama: "Budi" },
    { nama: "Cindy" },
  ],
  "Budi"
);

// Output
{
  student: { nama: "Budi" },
  index: 1,
}


// Test Case 2
findStudent(
  [
    { nama: "Andi" },
    { nama: "Budi" },
    { nama: "Cindy" },
  ],
  "Andi"
);

// Output
{
  student: { nama: "Andi" },
  index: 0,
}


// Test Case 3
findStudent(
  [
    { nama: "Andi" },
    { nama: "Budi" },
  ],
  "Vincent"
);

// Output
"Siswa tidak ditemukan."


// Test Case 4
findStudent(
  "Hello",
  "Budi"
);

// Output
"Parameter students harus berupa array."


// Test Case 5
findStudent(
  [
    { nama: "Andi" },
    { nama: "Budi" },
  ],
  ""
);

// Output
"Nama harus berupa string."
```
