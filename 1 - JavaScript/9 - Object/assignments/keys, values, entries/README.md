# Assignment - Object.keys(), Object.values(), dan Object.entries() (Medium)

## Tujuan Pembelajaran

- Memahami fungsi `Object.keys()`, `Object.values()`, dan `Object.entries()`.
- Mampu mengambil daftar key, value, dan pasangan key-value dari sebuah object.
- Mampu membuat function yang menerima object sebagai parameter.
- Mampu mengembalikan hasil pengolahan object menggunakan method bawaan JavaScript.

## Soal

Buatlah sebuah function berikut.

```javascript
const getObjectInfo = (obj) => {
  // code here
};
```

Function menerima sebuah object, kemudian menampilkan hasil dari:

- `Object.keys()`
- `Object.values()`
- `Object.entries()`

Gunakan object yang sama untuk ketiga method tersebut.

> **Catatan:** Fokus utama assignment ini adalah memahami perbedaan hasil yang dikembalikan oleh `Object.keys()`, `Object.values()`, dan `Object.entries()`.

### Validasi

- Jika parameter bukan object, tampilkan `"Input harus berupa object."`
- Jika parameter bernilai `null`, tampilkan `"Object tidak boleh null."`
- Jika object tidak memiliki properti, tampilkan `"Object kosong."`

---

## Result / Test Case

```javascript
// Test Case 1
getObjectInfo({
  nama: "Mouse",
  harga: 150000,
});

// Output
["nama", "harga"][("Mouse", 150000)][(["nama", "Mouse"], ["harga", 150000])];

// Test Case 2
getObjectInfo({
  nama: "Keyboard",
  harga: 350000,
  stok: 10,
});

// Output
["nama", "harga", "stok"][("Keyboard", 350000, 10)][
  (["nama", "Keyboard"], ["harga", 350000], ["stok", 10])
];

// Test Case 3
getObjectInfo({});

// Output
("Object kosong.");

// Test Case 4
getObjectInfo(null);

// Output
("Object tidak boleh null.");

// Test Case 5
getObjectInfo("Hello");

// Output
("Input harus berupa object.");
```
