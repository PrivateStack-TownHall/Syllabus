# Assignment - Konversi Suhu Celsius ke Fahrenheit (Easy)

## Tujuan Pembelajaran

- Mampu membuat function dengan parameter dan nilai kembalian.
- Mampu menggunakan variabel untuk melakukan perhitungan.
- Mampu menerapkan rumus konversi suhu.
- Mampu melakukan validasi sederhana terhadap input.

## Soal

Buatlah sebuah function berikut.

```javascript
const convertToFahrenheit = (celsius) => {
  // code here
};
```

Function menerima satu parameter berupa suhu dalam satuan **Celsius**, kemudian mengembalikan hasil konversinya ke dalam satuan **Fahrenheit**.

Gunakan rumus berikut.

```text
Fahrenheit = (Celsius × 9 / 5) + 32
```

> **Catatan:** Fokus utama assignment ini adalah memahami cara menggunakan function untuk menyelesaikan perhitungan sederhana menggunakan rumus matematika.

### Validasi

- Jika `celsius` bukan number, tampilkan `"Suhu harus berupa number."`

---

## Result / Test Case

```javascript
// Test Case 1
convertToFahrenheit(30);

// Output
86;

// Test Case 2
convertToFahrenheit(0);

// Output
32;

// Test Case 3
convertToFahrenheit(100);

// Output
212;

// Test Case 4
convertToFahrenheit(-40);

// Output
-40;

// Test Case 5
convertToFahrenheit("30");

// Output
("Suhu harus berupa number.");
```
