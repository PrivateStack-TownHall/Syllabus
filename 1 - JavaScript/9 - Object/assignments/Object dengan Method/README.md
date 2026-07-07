# Assignment - Object dengan Method (Medium)

## Tujuan Pembelajaran

- Memahami cara membuat method di dalam object.
- Memahami penggunaan keyword `this` untuk mengakses properti object.
- Mampu membuat object menggunakan function.
- Mampu memanggil method pada sebuah object.

## Soal

Buatlah sebuah function berikut.

```javascript
const createCar = (brand) => {
  // code here
};
```

Function menerima sebuah parameter `brand`, kemudian mengembalikan sebuah object `mobil` dengan struktur sebagai berikut.

- Properti:
  - `brand`

- Method:
  - `nyalakanMesin()`

Method `nyalakanMesin()` harus mengembalikan string dengan format berikut.

```text
<brand>: Mesin menyala!
```

Gunakan keyword `this` untuk mengakses nilai `brand` di dalam method.

> **Catatan:** Fokus utama assignment ini adalah memahami cara membuat method pada object serta penggunaan keyword `this` untuk mengakses properti milik object tersebut.

### Validasi

- Jika `brand` bukan string, tampilkan `"Brand harus berupa string."`
- Jika `brand` berupa string kosong, tampilkan `"Brand tidak boleh kosong."`

---

## Result / Test Case

```javascript
// Test Case 1
const mobil1 = createCar("Toyota");

mobil1.nyalakanMesin();

// Output
("Toyota: Mesin menyala!");

// Test Case 2
const mobil2 = createCar("Honda");

mobil2.nyalakanMesin();

// Output
("Honda: Mesin menyala!");

// Test Case 3
createCar("");

// Output
("Brand tidak boleh kosong.");

// Test Case 4
createCar(123);

// Output
("Brand harus berupa string.");
```
