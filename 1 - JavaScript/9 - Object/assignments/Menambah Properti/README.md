# Assignment - Menambah Properti Object (Easy)

## Tujuan Pembelajaran

- Memahami cara menambahkan properti baru pada object.
- Mampu memanipulasi object menggunakan JavaScript.
- Mampu membuat function yang menerima object sebagai parameter.
- Mampu mengembalikan object yang telah diperbarui.

## Soal

Buatlah sebuah function berikut.

```javascript
const addEmail = (person, email) => {
  // code here
};
```

Function menerima sebuah object `person` dan sebuah parameter `email`.

Tambahkan properti baru bernama `email` ke dalam object tersebut, kemudian kembalikan object yang telah diperbarui.

> **Catatan:** Fokus utama assignment ini adalah memahami cara menambahkan properti baru pada object menggunakan JavaScript.

### Validasi

- Jika `person` bukan object, tampilkan `"Person harus berupa object."`
- Jika `person` bernilai `null`, tampilkan `"Object tidak boleh null."`
- Jika `email` bukan string atau string kosong, tampilkan `"Email harus berupa string."`
- Jika object sudah memiliki properti `email`, tampilkan `"Email sudah terdaftar."`

---

## Result / Test Case

```javascript
// Test Case 1
addEmail(
  {
    nama: "Vincent",
    umur: 25,
  },
  "vincent@email.com"
);

// Output
{
  nama: "Vincent",
  umur: 25,
  email: "vincent@email.com",
}


// Test Case 2
addEmail(
  {
    nama: "Budi",
    umur: 30,
  },
  "budi@email.com"
);

// Output
{
  nama: "Budi",
  umur: 30,
  email: "budi@email.com",
}


// Test Case 3
addEmail(
  {
    nama: "Vincent",
    umur: 25,
    email: "vincent@email.com",
  },
  "baru@email.com"
);

// Output
"Email sudah terdaftar."


// Test Case 4
addEmail(null, "vincent@email.com");

// Output
"Object tidak boleh null."


// Test Case 5
addEmail(
  {
    nama: "Vincent",
    umur: 25,
  },
  ""
);

// Output
"Email harus berupa string."
```
