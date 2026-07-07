# Assignment - To-Do List Sederhana (Easy)

## Tujuan Pembelajaran

- Mampu menggunakan global variable sebagai penyimpanan data.
- Mampu membuat function untuk memanipulasi array.
- Mampu menambahkan dan menampilkan data menggunakan array.
- Mampu membangun program sederhana berbasis console.

## Soal

Buat sebuah **global variable** berikut.

```javascript
const todos = [];
```

Kemudian buat dua buah function berikut.

```javascript
const addTodo = (task) => {
  // code here
};

const showTodos = () => {
  // code here
};
```

### Ketentuan

#### Global Variable

Gunakan array berikut sebagai tempat penyimpanan daftar tugas.

```javascript
const todos = [];
```

---

### Function `addTodo()`

Menambahkan sebuah tugas baru ke dalam array `todos`.

---

### Function `showTodos()`

Menampilkan seluruh daftar tugas yang ada di dalam array `todos`.

### Validasi

#### addTodo()

- `task` harus berupa string.
- `task` tidak boleh berupa string kosong.
- Tidak boleh ada tugas dengan nama yang sama.

#### showTodos()

- Jika belum ada tugas, tampilkan `"Belum ada tugas."`

---

## Result / Test Case

```javascript
// Test Case 1
addTodo("Belajar JavaScript");

showTodos();

// Output
["Belajar JavaScript"];

// Test Case 2
addTodo("Kerjakan tugas Sekolah Stack");

showTodos();

// Output
["Belajar JavaScript", "Kerjakan tugas Sekolah Stack"];

// Test Case 3
addTodo("Belajar JavaScript");

// Output
("Tugas sudah ada.");

// Test Case 4
addTodo("");

// Output
("Tugas tidak boleh kosong.");

// Test Case 5
const todos = [];

showTodos();

// Output
("Belum ada tugas.");
```
