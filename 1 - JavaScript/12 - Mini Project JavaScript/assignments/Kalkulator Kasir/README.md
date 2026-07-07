# Assignment - Mini Project Kasir Sederhana (Hard)

## Tujuan Pembelajaran

- Mampu menggabungkan konsep variabel, function, kondisi, looping, array, dan object dalam satu program.
- Mampu membangun mini project berbasis console dengan beberapa function.
- Mampu mengelola data menggunakan global variable.
- Mampu menghitung total belanja, diskon, dan menampilkan struk belanja.

## Soal

Buat sebuah **global variable** berikut.

```javascript
const cart = [];
```

Kemudian buat beberapa function berikut.

```javascript
const addItem = (name, price, quantity) => {
  // code here
};

const calculateTotal = () => {
  // code here
};

const calculateDiscount = (total) => {
  // code here
};

const calculateFinalTotal = () => {
  // code here
};

const printReceipt = () => {
  // code here
};
```

### Ketentuan

Gunakan array berikut sebagai tempat penyimpanan data belanja.

```javascript
const cart = [];
```

Setiap barang memiliki struktur berikut.

```javascript
{
  name,
  price,
  quantity,
}
```

---

### Function `addItem()`

Menambahkan barang ke dalam keranjang belanja.

---

### Function `calculateTotal()`

Menghitung total seluruh belanja.

Rumus:

```text
harga × quantity
```

---

### Function `calculateDiscount(total)`

Hitung diskon berdasarkan aturan berikut.

| Total Belanja | Diskon |
| ------------- | ------ |
| ≥ 100000      | 10%    |
| < 100000      | 0%     |

Function mengembalikan nominal diskon.

---

### Function `calculateFinalTotal()`

Mengembalikan total akhir setelah dikurangi diskon.

---

### Function `printReceipt()`

Menampilkan struk belanja dengan format berikut.

```text
=== STRUK BELANJA ===
Kopi x2 = 40000
Roti x3 = 45000

Total: 85000
Diskon: 0
Total Akhir: 85000
```

### Validasi

#### addItem()

- `name` harus berupa string.
- `price` harus berupa number lebih dari 0.
- `quantity` harus berupa number lebih dari 0.
- Tidak boleh ada nama barang yang sama di dalam keranjang.

#### calculateTotal()

- Jika keranjang kosong, kembalikan `0`.

#### printReceipt()

- Jika keranjang kosong, tampilkan `"Keranjang masih kosong."`

---

## Result / Test Case

```javascript
// Test Case 1
addItem("Kopi", 20000, 2);
addItem("Roti", 15000, 3);

printReceipt();

// Output
=== STRUK BELANJA ===
Kopi x2 = 40000
Roti x3 = 45000

Total: 85000
Diskon: 0
Total Akhir: 85000


// Test Case 2
addItem("Susu", 30000, 2);

printReceipt();

// Output
=== STRUK BELANJA ===
Kopi x2 = 40000
Roti x3 = 45000
Susu x2 = 60000

Total: 145000
Diskon: 14500
Total Akhir: 130500


// Test Case 3
addItem("Kopi", 20000, 1);

// Output
"Barang sudah ada di keranjang."


// Test Case 4
addItem("Teh", -5000, 2);

// Output
"Harga tidak valid."


// Test Case 5
const cart = [];

printReceipt();

// Output
"Keranjang masih kosong."
```
