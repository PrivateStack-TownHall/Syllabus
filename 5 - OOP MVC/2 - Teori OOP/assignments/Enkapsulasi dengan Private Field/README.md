# Enkapsulasi dengan Private Field (Easy)

## Tujuan Pembelajaran

- Memahami 4 pilar utama OOP: enkapsulasi, inheritance, polimorfisme, dan abstraksi
- Mampu menerapkan enkapsulasi menggunakan private field (`#`)
- Mampu membuat inheritance antar class menggunakan `extends` dan `super`
- Mampu menerapkan polimorfisme melalui method overriding

## Soal

Buat class `Akun` dengan properti saldo bersifat private (`#saldo`), lalu buat method untuk menambah dan membaca nilainya.

## Tasks

### Task 1
Buat class `Akun` dengan private field `#saldo` yang diinisialisasi `0`.

### Task 2
Buat method `tambahSaldo(jumlah)` yang menambahkan nilai ke `#saldo`, dan method `cekSaldo()` yang mengembalikan nilainya.

## Results / Test Cases

### Test Case 1
```
Input:
let akun1 = new Akun();
akun1.tambahSaldo(50000);
akun1.cekSaldo();

Output: 50000
```

### Test Case 2
```
Input: new Akun().cekSaldo()
Output: 0
```

## Tips dan Trik

- Private field (diawali `#`) hanya bisa diakses dari dalam class itu sendiri, tidak bisa diakses langsung dari luar seperti `akun1.#saldo`.
