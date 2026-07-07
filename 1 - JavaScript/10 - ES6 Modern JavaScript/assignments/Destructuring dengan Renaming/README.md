# Assignment - Object Destructuring dengan Renaming (Medium)

## Tujuan Pembelajaran

- Memahami konsep object destructuring di JavaScript.
- Mampu melakukan destructuring dengan mengganti nama variabel (_renaming_).
- Mampu membuat function yang menerima object sebagai parameter.
- Mampu mengakses data object menggunakan sintaks destructuring.

## Soal

Buatlah sebuah function berikut.

```javascript
const showStudent = (student) => {
  // code here
};
```

Function menerima sebuah object dengan struktur seperti berikut.

```javascript
{
  name: "Vincent",
  class: "12A"
}
```

Lakukan **object destructuring** dengan **mengganti nama variabel hasil destructuring**, kemudian tampilkan nama dan kelas siswa.

Sebagai contoh:

- `name` menjadi `studentName`
- `class` menjadi `studentClass`

> **Catatan:** Fokus utama assignment ini adalah memahami cara melakukan **renaming** saat menggunakan object destructuring.

### Validasi

- Jika parameter bukan object, tampilkan `"Student harus berupa object."`
- Jika parameter bernilai `null`, tampilkan `"Object tidak boleh null."`
- Jika properti `name` atau `class` tidak ditemukan, tampilkan `"Data student tidak lengkap."`

---

## Result / Test Case

```javascript
// Test Case 1
showStudent({
  name: "Vincent",
  class: "12A",
});

// Output
Vincent
12A


// Test Case 2
showStudent({
  name: "Budi",
  class: "11B",
});

// Output
Budi
11B


// Test Case 3
showStudent({
  name: "Andi",
});

// Output
"Data student tidak lengkap."


// Test Case 4
showStudent(null);

// Output
"Object tidak boleh null."


// Test Case 5
showStudent("Hello");

// Output
"Student harus berupa object."
```
