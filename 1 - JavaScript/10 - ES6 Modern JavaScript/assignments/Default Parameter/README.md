# Assignment - Default Parameter (Easy)

## Tujuan Pembelajaran

- Memahami konsep default parameter pada JavaScript.
- Mampu membuat function dengan parameter default.
- Mampu menangani parameter yang tidak diberikan.
- Mampu mengembalikan nilai menggunakan `return`.

## Soal

Buatlah sebuah function berikut.

```javascript
const greet = (name = "Guest") => {
  // code here
};
```

Function menerima satu parameter `name`.

Jika parameter tidak diberikan, gunakan nilai default `"Guest"`.

### Validasi

- Jika `name` bukan string, tampilkan `"Name harus berupa string."`
- Jika `name` berupa string kosong, gunakan `"Guest"` sebagai nilai default.

---

## Result / Test Case

```javascript
// Test Case 1
greet();

// Output
("Hello, Guest!");

// Test Case 2
greet("Dino");

// Output
("Hello, Dino!");

// Test Case 3
greet("Vincent");

// Output
("Hello, Vincent!");

// Test Case 4
greet("");

// Output
("Hello, Guest!");

// Test Case 5
greet(123);

// Output
("Name harus berupa string.");
```
