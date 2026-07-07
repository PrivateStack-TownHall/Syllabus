# Assignment - Dot Notation vs Bracket Notation (Easy)

## Tujuan Pembelajaran

- Memahami cara mengakses properti pada object.
- Memahami perbedaan penggunaan **dot notation** dan **bracket notation**.
- Mampu mengakses properti object menggunakan kedua metode tersebut.
- Mampu memilih cara akses properti yang sesuai dengan kebutuhan.

## Soal

Buatlah sebuah function berikut.

```javascript
const showName = (person) => {
  // code here
};
```

Function menerima sebuah object `person` dengan struktur seperti berikut.

```javascript
{
  nama: "Vincent",
  umur: 25,
}
```

Kemudian tampilkan nilai properti `nama` menggunakan:

- **Dot notation**
- **Bracket notation**

> **Catatan:** Fokus utama assignment ini adalah memahami perbedaan cara mengakses properti object menggunakan **dot notation** dan **bracket notation**.

### Validasi

- Jika parameter bukan object, tampilkan `"Input harus berupa object."`
- Jika parameter bernilai `null`, tampilkan `"Object tidak boleh null."`
- Jika properti `nama` tidak ditemukan, tampilkan `"Properti nama tidak ditemukan."`

---

## Result / Test Case

```javascript
// Test Case 1
showName({
  nama: "Vincent",
  umur: 25,
});

// Output
Vincent;
Vincent;

// Test Case 2
showName({
  nama: "Budi",
});

// Output
Budi;
Budi;

// Test Case 3
showName({
  umur: 20,
});

// Output
("Properti nama tidak ditemukan.");

// Test Case 4
showName(null);

// Output
("Object tidak boleh null.");

// Test Case 5
showName("Hello");

// Output
("Input harus berupa object.");
```
