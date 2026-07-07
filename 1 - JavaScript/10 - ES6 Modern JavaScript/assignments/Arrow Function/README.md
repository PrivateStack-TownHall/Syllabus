# Assignment - Arrow Function (Easy)

## Tujuan Pembelajaran

- Memahami sintaks arrow function.
- Mampu membuat function menggunakan arrow function.
- Mampu menerima parameter dan mengembalikan nilai.
- Memahami perbedaan penulisan dengan function biasa.

## Soal

Buatlah sebuah function berikut.

```javascript
const square = (number) => {
  // code here
};
```

Function menerima satu angka, kemudian mengembalikan nilai kuadrat dari angka tersebut.

### Validasi

- Jika parameter bukan number, tampilkan `"Input harus berupa number."`

---

## Result / Test Case

```javascript
// Test Case 1
square(6);

// Output
36;

// Test Case 2
square(10);

// Output
100;

// Test Case 3
square(-5);

// Output
25;

// Test Case 4
square("6");

// Output
("Input harus berupa number.");
```
