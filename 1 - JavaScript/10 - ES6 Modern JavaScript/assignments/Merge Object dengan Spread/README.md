# Assignment - Menggabungkan Object dengan Spread Operator (Hard)

## Tujuan Pembelajaran

- Memahami penggunaan **spread operator (`...`)** pada object.
- Mampu menggabungkan dua object menjadi object baru.
- Memahami urutan prioritas properti saat terjadi duplikasi key.
- Mampu memanfaatkan spread operator untuk mempermudah manipulasi object.

## Soal

Buatlah sebuah function berikut.

```javascript
const mergeObjects = (obj1, obj2) => {
  // code here
};
```

Function menerima dua buah object, kemudian menggabungkannya menggunakan **spread operator (`...`)**.

Jika terdapat **properti dengan nama yang sama**, maka gunakan nilai dari **object kedua (`obj2`)**.

Setelah itu, jelaskan melalui komentar mengapa nilai dari object kedua menggantikan nilai pada object pertama.

> **Catatan:** Fokus utama assignment ini adalah memahami cara kerja **spread operator** saat menggabungkan object serta mengetahui prioritas properti ketika terjadi key yang sama.

### Validasi

- Jika `obj1` bukan object, tampilkan `"Parameter pertama harus berupa object."`
- Jika `obj2` bukan object, tampilkan `"Parameter kedua harus berupa object."`
- Jika salah satu parameter bernilai `null`, tampilkan `"Object tidak boleh null."`

---

## Result / Test Case

```javascript
// Test Case 1
mergeObjects(
  {
    warna: "Merah",
    ukuran: "M",
  },
  {
    warna: "Biru",
  }
);

// Output
{
  warna: "Biru",
  ukuran: "M",
}


// Test Case 2
mergeObjects(
  {
    nama: "Vincent",
    umur: 25,
  },
  {
    pekerjaan: "Frontend Developer",
  }
);

// Output
{
  nama: "Vincent",
  umur: 25,
  pekerjaan: "Frontend Developer",
}


// Test Case 3
mergeObjects(null, { warna: "Biru" });

// Output
"Object tidak boleh null."


// Test Case 4
mergeObjects("Hello", { warna: "Biru" });

// Output
"Parameter pertama harus berupa object."


// Test Case 5
mergeObjects({ warna: "Merah" }, 123);

// Output
"Parameter kedua harus berupa object."
```
