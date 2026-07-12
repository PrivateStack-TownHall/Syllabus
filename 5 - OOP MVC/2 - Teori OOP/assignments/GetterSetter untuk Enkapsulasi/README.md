# Getter/Setter untuk Enkapsulasi (Easy)

## Tujuan Pembelajaran

- Memahami 4 pilar utama OOP: enkapsulasi, inheritance, polimorfisme, dan abstraksi
- Mampu menerapkan enkapsulasi menggunakan private field (`#`)
- Mampu membuat inheritance antar class menggunakan `extends` dan `super`
- Mampu menerapkan polimorfisme melalui method overriding

## Soal

Buat class `Suhu` dengan private field derajat Celsius, sediakan getter untuk mengonversinya ke Fahrenheit.

## Tasks

### Task 1
Buat class `Suhu` dengan private field `#celsius` yang diisi lewat constructor.

### Task 2
Buat getter `fahrenheit` yang menghitung dan mengembalikan konversi dari `#celsius` ke Fahrenheit.

## Results / Test Cases

### Test Case 1
```
Input: new Suhu(30).fahrenheit
Output: 86
```

### Test Case 2
```
Input: new Suhu(0).fahrenheit
Output: 32
```

## Tips dan Trik

- Rumus konversi Celsius ke Fahrenheit: `F = C * 9/5 + 32`.
