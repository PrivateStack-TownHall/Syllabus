# Assignment - Pencarian Buku (Medium)

## Tujuan Pembelajaran

- Mampu menggunakan global variable sebagai penyimpanan data.
- Mampu membuat beberapa function yang saling bekerja sama.
- Mampu mencari data pada array of objects menggunakan perulangan.
- Mampu mengembalikan hasil pencarian berdasarkan kondisi tertentu.

## Soal

Buat sebuah **global variable** berikut.

```javascript
const books = [];
```

Kemudian buat dua buah function berikut.

```javascript
const addBook = (title, author, year) => {
  // code here
};

const findBookByTitle = (title) => {
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

### Function `addBook()`

Menambahkan buku baru ke dalam array `books`.

---

### Function `findBookByTitle()`

Mencari sebuah buku berdasarkan **title**.

Jika buku ditemukan, kembalikan object buku tersebut.

Jika tidak ditemukan, tampilkan:

```text
Buku tidak ditemukan.
```

> **Catatan:** Gunakan perulangan (`for`, `for...of`, atau `find()`) untuk melakukan pencarian data.

### Validasi

#### addBook()

- `title` harus berupa string.
- `author` harus berupa string.
- `year` harus berupa number.
- Tidak boleh ada judul buku yang sama.

#### findBookByTitle()

- Jika `title` bukan string atau string kosong, tampilkan `"Judul harus berupa string."`
- Jika buku tidak ditemukan, tampilkan `"Buku tidak ditemukan."`

---

## Result / Test Case

```javascript
// Test Case 1
addBook(
  "Bumi Manusia",
  "Pramoedya Ananta Toer",
  1980
);

findBookByTitle("Bumi Manusia");

// Output
{
  title: "Bumi Manusia",
  author: "Pramoedya Ananta Toer",
  year: 1980,
}


// Test Case 2
addBook(
  "Laskar Pelangi",
  "Andrea Hirata",
  2005
);

findBookByTitle("Laskar Pelangi");

// Output
{
  title: "Laskar Pelangi",
  author: "Andrea Hirata",
  year: 2005,
}


// Test Case 3
findBookByTitle("Atomic Habits");

// Output
"Buku tidak ditemukan."


// Test Case 4
findBookByTitle("");

// Output
"Judul harus berupa string."


// Test Case 5
addBook(
  "Bumi Manusia",
  "Pramoedya Ananta Toer",
  1980
);

// Output
"Judul buku sudah terdaftar."
```
