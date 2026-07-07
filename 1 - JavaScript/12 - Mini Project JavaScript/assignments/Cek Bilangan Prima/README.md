# Assignment - Cek Bilangan Prima (Easy)

## Tujuan Pembelajaran

- Mampu memecah permasalahan menjadi beberapa function.
- Mampu menggunakan function, kondisi, dan perulangan dalam satu program.
- Memahami konsep bilangan prima berdasarkan jumlah faktor.
- Mampu memanfaatkan hasil dari sebuah function di dalam function lain.

## Soal

Buatlah dua buah function berikut.

```javascript
const countFactors = (number) => {
  // code here
};

const checkPrime = (number) => {
  // code here
};
```

### Ketentuan

#### Function `countFactors(number)`

Function digunakan untuk menghitung jumlah faktor dari sebuah angka.

Contoh:

- 6 memiliki faktor `1, 2, 3, 6` → jumlah faktor = **4**
- 7 memiliki faktor `1, 7` → jumlah faktor = **2**

Function ini **tidak perlu dipanggil secara langsung pada test case**, tetapi digunakan oleh `checkPrime()`.

#### Function `checkPrime(number)`

Function memanggil `countFactors(number)`.

Jika jumlah faktor sama dengan **2**, kembalikan:

```javascript
true;
```

Selain itu kembalikan:

```javascript
false;
```

> **Petunjuk:** Bilangan prima adalah bilangan yang memiliki tepat dua faktor, yaitu 1 dan dirinya sendiri.

### Validasi

- Jika parameter bukan number, tampilkan `"Input harus berupa number."`
- Jika angka kurang dari atau sama dengan 0, tampilkan `"Angka harus lebih dari 0."`

---

## Result / Test Case

```javascript
// Test Case 1
checkPrime(7);

// Output
true;

// Test Case 2
checkPrime(12);

// Output
false;

// Test Case 3
checkPrime(2);

// Output
true;

// Test Case 4
checkPrime(-5);

// Output
("Angka harus lebih dari 0.");

// Test Case 5
checkPrime("10");

// Output
("Input harus berupa number.");
```
