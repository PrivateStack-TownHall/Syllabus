# Assignment - Mengakses Properti Object (Easy)

## Tujuan Pembelajaran

- Memahami cara mengakses properti pada object.
- Mampu menggunakan object sebagai parameter function.
- Mampu melakukan validasi data sebelum diproses.
- Mampu mengembalikan hasil menggunakan `return`.

## Soal

Buatlah sebuah function berikut.

```javascript
const showBook = (book) => {
  // code here
};
```

Function menerima sebuah object `book` dengan format berikut.

```javascript
{
  title: "JavaScript Dasar",
  pages: 180,
  author: "Santino"
}
```

Function harus mengembalikan informasi judul dan penulis buku.

### Validasi

- Jika parameter bukan object, tampilkan `"Book harus berupa object"`.
- Jika properti `title` atau `author` tidak ada, tampilkan `"Data book tidak lengkap"`.

---

## Result / Test Case

```javascript
// Test Case 1
showBook({
  title: "JavaScript Dasar",
  pages: 180,
  author: "Santino",
});

// Output
("JavaScript Dasar - Santino");

// Test Case 2
showBook({
  title: "Clean Code",
  author: "Robert C. Martin",
});

// Output
("Clean Code - Robert C. Martin");

// Test Case 3
showBook({
  title: "JavaScript",
});

// Output
("Data book tidak lengkap");

// Test Case 4
showBook("Hello");

// Output
("Book harus berupa object");
```
