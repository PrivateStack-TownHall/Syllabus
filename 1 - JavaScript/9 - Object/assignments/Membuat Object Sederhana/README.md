# Assignment - Membuat Object Sederhana (Easy)

## Tujuan Pembelajaran

- Memahami konsep dasar object di JavaScript.
- Mampu membuat object menggunakan function.
- Mampu mengembalikan object menggunakan `return`.
- Memahami struktur key dan value pada object.

## Soal

Buatlah sebuah function berikut.

```javascript
const createStudent = (name, age, studentClass) => {
  // code here
};
```

Function menerima tiga parameter:

- `name` (string)
- `age` (number)
- `studentClass` (string)

Kemudian function harus mengembalikan object dengan struktur berikut.

```javascript
{
  name,
  age,
  class: studentClass
}
```

### Validasi

- Jika `name` bukan string atau string kosong, tampilkan `"Nama harus berupa string."`
- Jika `age` bukan number atau kurang dari 0, tampilkan `"Umur tidak valid."`
- Jika `studentClass` bukan string atau string kosong, tampilkan `"Kelas harus berupa string."`

---

## Result / Test Case

```javascript
// Test Case 1
createStudent("Vincent", 25, "Fullstack JavaScript");

// Output
{
  name: "Vincent",
  age: 25,
  class: "Fullstack JavaScript"
}


// Test Case 2
createStudent("Budi", 20, "Backend");

// Output
{
  name: "Budi",
  age: 20,
  class: "Backend"
}


// Test Case 3
createStudent("", 20, "Frontend");

// Output
"Nama harus berupa string."


// Test Case 4
createStudent("Vincent", -1, "Frontend");

// Output
"Umur tidak valid."


// Test Case 5
createStudent("Vincent", 25, "");

// Output
"Kelas harus berupa string."
```
