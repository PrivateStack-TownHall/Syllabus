# Assignment - Total Belanja dengan Diskon (Easy)

## Tujuan Pembelajaran

- Mampu menggunakan function untuk menyelesaikan perhitungan sederhana.
- Mampu mengolah data menggunakan array of objects.
- Mampu menerapkan percabangan (`if`) untuk menentukan diskon.
- Mampu memecah proses perhitungan menjadi beberapa function.

## Soal

Buatlah dua buah function berikut.

```javascript
const calculateTotal = (items) => {
  // code here
};

const calculateFinalTotal = (items) => {
  // code here
};
```

### Ketentuan

Data barang memiliki struktur berikut.

```javascript
{
  name,
  price,
  quantity,
}
```

---

### Function `calculateTotal()`

Function menerima array of objects, kemudian menghitung total seluruh belanja.

Rumus:

```text
price × quantity
```

---

### Function `calculateFinalTotal()`

Function memanggil `calculateTotal()`.

Jika total belanja **lebih dari 100000**, berikan diskon **10%**.

Kemudian kembalikan total akhir setelah dikurangi diskon.

### Validasi

#### calculateTotal()

- Parameter harus berupa array.
- Jika array kosong, kembalikan `0`.
- Seluruh `price` dan `quantity` harus berupa number.

#### calculateFinalTotal()

- Gunakan hasil dari `calculateTotal()`.
- Jika parameter bukan array, tampilkan `"Parameter harus berupa array."`

---

## Result / Test Case

```javascript
// Test Case 1
calculateFinalTotal([
  {
    name: "Kopi",
    price: 20000,
    quantity: 2,
  },
  {
    name: "Roti",
    price: 15000,
    quantity: 3,
  },
]);

// Output
85000;

// Test Case 2
calculateFinalTotal([
  {
    name: "Laptop",
    price: 5000000,
    quantity: 1,
  },
]);

// Output
4500000;

// Test Case 3
calculateFinalTotal([]);

// Output
0;

// Test Case 4
calculateFinalTotal([
  {
    name: "Kopi",
    price: "20000",
    quantity: 2,
  },
]);

// Output
("Seluruh harga dan jumlah harus berupa number.");

// Test Case 5
calculateFinalTotal("Hello");

// Output
("Parameter harus berupa array.");
```
