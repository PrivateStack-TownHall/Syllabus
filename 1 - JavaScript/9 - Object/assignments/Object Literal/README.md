# Assignment - Object Literal (Easy)

## Tujuan Pembelajaran

- Memahami konsep dasar object literal di JavaScript.
- Mampu membuat object menggunakan object literal.
- Mampu mengembalikan object melalui sebuah function.
- Memahami struktur key dan value pada object.

## Soal

Buatlah sebuah function berikut.

```javascript
const createPerson = (nama, umur, pekerjaan) => {
  // code here
};
```

Function menerima tiga parameter:

- `nama` (string)
- `umur` (number)
- `pekerjaan` (string)

Kemudian function harus mengembalikan sebuah **object literal** dengan struktur berikut.

```javascript
{
  nama,
  umur,
  pekerjaan,
}
```

> **Catatan:** Fokus utama assignment ini adalah memahami cara membuat object literal menggunakan data yang diterima melalui parameter function.

### Validasi

- Jika `nama` bukan string atau string kosong, tampilkan `"Nama harus berupa string."`
- Jika `umur` bukan number atau bernilai kurang dari `0`, tampilkan `"Umur tidak valid."`
- Jika `pekerjaan` bukan string atau string kosong, tampilkan `"Pekerjaan harus berupa string."`

---

## Result / Test Case

```javascript
// Test Case 1
createPerson("Vincent", 25, "Frontend Developer");

// Output
{
  nama: "Vincent",
  umur: 25,
  pekerjaan: "Frontend Developer",
}


// Test Case 2
createPerson("Budi", 30, "Backend Developer");

// Output
{
  nama: "Budi",
  umur: 30,
  pekerjaan: "Backend Developer",
}


// Test Case 3
createPerson("", 25, "Frontend Developer");

// Output
"Nama harus berupa string."


// Test Case 4
createPerson("Vincent", -5, "Frontend Developer");

// Output
"Umur tidak valid."


// Test Case 5
createPerson("Vincent", 25, "");

// Output
"Pekerjaan harus berupa string."
```
