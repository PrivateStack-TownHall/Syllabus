# Assignment - CRUD Data Buku (Medium)

## Tujuan Pembelajaran

- Mampu menggabungkan penggunaan variabel, function, kondisi, dan array of objects.
- Mampu membangun program CRUD sederhana berbasis console.
- Mampu memanipulasi data menggunakan beberapa function.
- Memahami penggunaan global variable sebagai penyimpanan data sementara.

## Soal

Buat sebuah **global variable** berikut.

```javascript
const books = [];
```

Kemudian buat beberapa function berikut.

```javascript
const addBook = (title, author, year) => {
  // code here
};

const updateBook = (title, newData) => {
  // code here
};

const deleteBook = (title) => {
  // code here
};

const showBooks = () => {
  // code here
};
```

### Ketentuan

#### Global Variable

Gunakan array berikut sebagai tempat penyimpanan data.

```javascript
const books = [];
```

Setiap buku memiliki struktur berikut.

```javascript
{
  title,
  author,
  year,
}
```

---

#### Function `addBook()`

Menambahkan buku baru ke dalam array `books`.

---

#### Function `updateBook()`

Mengubah data buku berdasarkan **title**.

Parameter kedua berupa object.

Contoh:

```javascript
updateBook("Laskar Pelangi", {
  year: 2008,
});
```

---

#### Function `deleteBook()`

Menghapus buku berdasarkan **title**.

---

#### Function `showBooks()`

Menampilkan seluruh data buku.

### Validasi

#### addBook()

- `title` harus berupa string.
- `author` harus berupa string.
- `year` harus berupa number.
- Tidak boleh ada judul buku yang sama.

#### updateBook()

- Jika buku tidak ditemukan, tampilkan `"Buku tidak ditemukan."`

#### deleteBook()

- Jika buku tidak ditemukan, tampilkan `"Buku tidak ditemukan."`

---

## Result / Test Case

```javascript
// Test Case 1
addBook("Laskar Pelangi", "Andrea Hirata", 2006);

showBooks();

// Output
[
  {
    title: "Laskar Pelangi",
    author: "Andrea Hirata",
    year: 2006,
  },
];

// Test Case 2
addBook("Atomic Habits", "James Clear", 2018);

showBooks();

// Output
[
  {
    title: "Laskar Pelangi",
    author: "Andrea Hirata",
    year: 2006,
  },
  {
    title: "Atomic Habits",
    author: "James Clear",
    year: 2018,
  },
];

// Test Case 3
updateBook("Laskar Pelangi", {
  year: 2008,
});

showBooks();

// Output
[
  {
    title: "Laskar Pelangi",
    author: "Andrea Hirata",
    year: 2008,
  },
  {
    title: "Atomic Habits",
    author: "James Clear",
    year: 2018,
  },
];

// Test Case 4
deleteBook("Atomic Habits");

showBooks();

// Output
[
  {
    title: "Laskar Pelangi",
    author: "Andrea Hirata",
    year: 2008,
  },
];

// Test Case 5
addBook("Laskar Pelangi", "Andrea Hirata", 2006);

// Output
("Judul buku sudah terdaftar.");
```
