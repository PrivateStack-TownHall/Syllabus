# this Keyword dalam Method (Medium)

## Tujuan Pembelajaran

- Memahami konsep dasar Object-Oriented Programming (OOP)
- Mampu membuat class dan object di JavaScript
- Memahami constructor dan property dalam class
- Mampu membuat dan memanggil method di dalam class

## Soal

Buat class `Akun` dengan method `tambahSaldo(jumlah)` yang mengubah properti saldo menggunakan `this`, lalu panggil method tersebut beberapa kali.

## Tasks

### Task 1
Buat class `Akun` dengan constructor yang menginisialisasi `saldo` bernilai `0`.

### Task 2
Tambahkan method `tambahSaldo(jumlah)` yang menambahkan `jumlah` ke `this.saldo`.

### Task 3
Buat satu object, lalu panggil method `tambahSaldo()` lebih dari sekali dengan nilai berbeda.

### Task 4
Tampilkan nilai `saldo` akhir setelah seluruh pemanggilan method.

## Results / Test Cases

### Test Case 1
```
Input:
let akun1 = new Akun();
akun1.tambahSaldo(50000);
akun1.tambahSaldo(25000);
akun1.saldo

Output: 75000
```

### Test Case 2
```
Input:
let akun2 = new Akun();
akun2.tambahSaldo(10000);
akun2.saldo

Output: 10000
```

## Tips dan Trik

- `this` selalu merujuk ke object yang sedang memanggil method tersebut, jadi perubahan lewat `this.saldo` akan tersimpan di object itu sendiri.
