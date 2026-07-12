# Polimorfisme dengan Banyak Class (Medium)

## Tujuan Pembelajaran

- Memahami 4 pilar utama OOP: enkapsulasi, inheritance, polimorfisme, dan abstraksi
- Mampu menerapkan enkapsulasi menggunakan private field (`#`)
- Mampu membuat inheritance antar class menggunakan `extends` dan `super`
- Mampu menerapkan polimorfisme melalui method overriding

## Soal

Buat beberapa class turunan dari `Bentuk` yang masing-masing meng-override method `luas()`, lalu panggil method yang sama untuk tiap object dalam sebuah array (polimorfisme).

## Tasks

### Task 1
Buat class `Bentuk` dengan method `luas()` yang mengembalikan `0` sebagai default.

### Task 2
Buat class `Lingkaran` dan `Persegi` yang masing-masing extends `Bentuk` dan meng-override method `luas()` sesuai rumusnya masing-masing.

### Task 3
Masukkan beberapa object dari class berbeda ke dalam satu array, lalu looping array tersebut dan panggil `luas()` untuk tiap object tanpa mempedulikan class aslinya.

## Results / Test Cases

### Test Case 1
```
Input:
let bentukList = [new Lingkaran(7), new Persegi(5)];
bentukList.forEach(b => console.log(b.luas().toFixed(2)));

Output:
153.94
25.00
```

## Tips dan Trik

- Inti polimorfisme adalah memanggil method yang sama (`luas()`) pada object berbeda, dan tiap object menjalankan versinya masing-masing secara otomatis.
