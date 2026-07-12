# Enkapsulasi dengan Validasi (Medium)

## Tujuan Pembelajaran

- Memahami 4 pilar utama OOP: enkapsulasi, inheritance, polimorfisme, dan abstraksi
- Mampu menerapkan enkapsulasi menggunakan private field (`#`)
- Mampu membuat inheritance antar class menggunakan `extends` dan `super`
- Mampu menerapkan polimorfisme melalui method overriding

## Soal

Buat class `Akun` dengan private field saldo, dan method `tarikSaldo(jumlah)` yang menolak penarikan jika saldo tidak mencukupi.

## Tasks

### Task 1
Buat class `Akun` dengan private field `#saldo` yang diinisialisasi dengan nilai awal tertentu.

### Task 2
Buat method `tarikSaldo(jumlah)` yang memeriksa apakah `jumlah` lebih besar dari `#saldo`.

### Task 3
Jika tidak cukup, tampilkan pesan penolakan. Jika cukup, kurangi `#saldo` dan tampilkan sisa saldo.

## Results / Test Cases

### Test Case 1
```
Input:
let akun1 = new Akun();
akun1.tarikSaldo(150000);

Output: Saldo tidak cukup
```

### Test Case 2
```
Input:
let akun2 = new Akun();
akun2.tarikSaldo(50000);

Output: Penarikan berhasil, sisa saldo: 50000
```

## Tips dan Trik

- Validasi sebaiknya dilakukan di awal method (early return / early check) sebelum mengubah nilai property, agar logikanya lebih mudah dibaca.
