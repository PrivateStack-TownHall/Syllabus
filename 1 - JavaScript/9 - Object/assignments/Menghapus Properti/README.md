# Assignment - Menghapus Properti Object (Easy)

## Tujuan Pembelajaran

- Memahami cara menghapus properti pada object menggunakan operator `delete`.
- Mampu memanipulasi object menggunakan JavaScript.
- Mampu membuat function yang menerima object sebagai parameter.
- Mampu mengembalikan object yang telah diperbarui.

## Soal

Buatlah sebuah function berikut.

```javascript
const removeAge = (person) => {
  // code here
};
```

Function menerima sebuah object `person`, kemudian hapus properti `umur` menggunakan operator `delete`.

Setelah properti berhasil dihapus, kembalikan object yang telah diperbarui.

> **Catatan:** Fokus utama assignment ini adalah memahami cara menghapus properti dari sebuah object menggunakan operator `delete`.

### Validasi

- Jika `person` bukan object, tampilkan `"Person harus berupa object."`
- Jika `person` bernilai `null`, tampilkan `"Object tidak boleh null."`
- Jika properti `umur` tidak ditemukan, tampilkan `"Properti umur tidak ditemukan."`

---

## Result / Test Case

```javascript
// Test Case 1
removeAge({
  nama: "Vincent",
  umur: 25,
});

// Output
{
  nama: "Vincent",
}


// Test Case 2
removeAge({
  nama: "Budi",
  umur: 30,
  email: "budi@email.com",
});

// Output
{
  nama: "Budi",
  email: "budi@email.com",
}


// Test Case 3
removeAge({
  nama: "Vincent",
});

// Output
"Properti umur tidak ditemukan."


// Test Case 4
removeAge(null);

// Output
"Object tidak boleh null."


// Test Case 5
removeAge("Hello");

// Output
"Person harus berupa object."
```
