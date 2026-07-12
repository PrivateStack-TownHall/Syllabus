# Method Overriding (Easy)

## Tujuan Pembelajaran

- Memahami 4 pilar utama OOP: enkapsulasi, inheritance, polimorfisme, dan abstraksi
- Mampu menerapkan enkapsulasi menggunakan private field (`#`)
- Mampu membuat inheritance antar class menggunakan `extends` dan `super`
- Mampu menerapkan polimorfisme melalui method overriding

## Soal

Buat class `Kucing` yang extends `Hewan` dan meng-override method `bersuara()` dengan suara yang berbeda.

## Tasks

### Task 1
Buat class `Hewan` dengan method `bersuara()` yang menampilkan pesan umum.

### Task 2
Buat class `Kucing` yang extends `Hewan`, lalu tuliskan ulang (override) method `bersuara()` dengan isi yang berbeda.

## Results / Test Cases

### Test Case 1
```
Input: new Kucing().bersuara()
Output: Meong!
```

### Test Case 2
```
Input: new Hewan().bersuara()
Output: Hewan mengeluarkan suara
```

## Tips dan Trik

- Method dengan nama yang sama di class turunan akan menggantikan (override) method milik parent saat dipanggil dari object turunan.
