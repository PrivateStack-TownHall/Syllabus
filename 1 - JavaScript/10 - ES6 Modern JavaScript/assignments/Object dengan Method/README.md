# Assignment - Object dengan Method (Hard)

## Tujuan Pembelajaran

- Memahami cara membuat method di dalam object.
- Mampu menggunakan shorthand method pada object.
- Memahami penggunaan keyword `this`.
- Mampu menggabungkan properti dan method dalam sebuah object.

## Soal

Buatlah sebuah function berikut.

```javascript
const createProduct = (name, price) => {
  // code here
};
```

Function menerima dua parameter:

- `name`
- `price`

Kemudian function harus mengembalikan sebuah object dengan struktur berikut.

```javascript
{
  name,
  price,
  getInfo() {
    // code here
  },
  applyDiscount(percent) {
    // code here
  }
}
```

### Ketentuan

- Method `getInfo()` mengembalikan string:

```text
Produk: <name> - Rp<price>
```

- Method `applyDiscount(percent)` mengurangi harga berdasarkan persentase yang diberikan, kemudian mengembalikan harga terbaru.

Gunakan keyword `this` untuk mengakses properti object.

### Validasi

- Jika `name` bukan string atau string kosong, tampilkan `"Nama produk harus berupa string."`
- Jika `price` bukan number atau kurang dari 0, tampilkan `"Harga tidak valid."`
- Jika `percent` bukan number atau di luar rentang 0–100, tampilkan `"Persentase diskon tidak valid."`

---

## Result / Test Case

```javascript
// Test Case 1
const product = createProduct("Mouse", 150000);

product.getInfo();

// Output
("Produk: Mouse - Rp150000");

// Test Case 2
const product = createProduct("Keyboard", 300000);

product.applyDiscount(10);

// Output
270000;

// Test Case 3
const product = createProduct("Monitor", 2000000);

product.applyDiscount(25);

// Output
1500000;

// Test Case 4
createProduct("", 150000);

// Output
("Nama produk harus berupa string.");

// Test Case 5
const product = createProduct("Mouse", 150000);

product.applyDiscount(120);

// Output
("Persentase diskon tidak valid.");
```
