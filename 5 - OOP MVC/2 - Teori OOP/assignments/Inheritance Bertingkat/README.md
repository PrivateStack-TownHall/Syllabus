# Inheritance Bertingkat (Medium)

## Tujuan Pembelajaran

- Memahami 4 pilar utama OOP: enkapsulasi, inheritance, polimorfisme, dan abstraksi
- Mampu menerapkan enkapsulasi menggunakan private field (`#`)
- Mampu membuat inheritance antar class menggunakan `extends` dan `super`
- Mampu menerapkan polimorfisme melalui method overriding

## Soal

Buat 3 tingkat inheritance: `Hewan` → `Mamalia` → `Kucing`, lalu buktikan `Kucing` bisa mengakses method dari seluruh parent-nya.

## Tasks

### Task 1
Buat class `Hewan` dengan method `bernafas()`.

### Task 2
Buat class `Mamalia` yang extends `Hewan`, tambahkan method `menyusui()`.

### Task 3
Buat class `Kucing` yang extends `Mamalia`, tambahkan method `bersuara()`.

### Task 4
Buat object dari `Kucing`, lalu panggil ketiga method dari tiga level class berbeda secara berurutan.

## Results / Test Cases

### Test Case 1
```
Input:
let kucing1 = new Kucing();
kucing1.bernafas();
kucing1.menyusui();
kucing1.bersuara();

Output:
Bernafas
Menyusui anaknya
Meong!
```

## Tips dan Trik

- Rantai inheritance bisa lebih dari satu tingkat; sebuah class bisa mewarisi method dari parent, grandparent, dan seterusnya selama masih terhubung lewat `extends`.
