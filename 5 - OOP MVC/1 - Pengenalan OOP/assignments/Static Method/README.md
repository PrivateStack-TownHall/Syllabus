# Static Method (Medium)

## Tujuan Pembelajaran

- Memahami konsep dasar Object-Oriented Programming (OOP)
- Mampu membuat class dan object di JavaScript
- Memahami constructor dan property dalam class
- Mampu membuat dan memanggil method di dalam class

## Soal

Buat class `MathHelper` dengan static method `kuadrat(n)` yang bisa dipanggil langsung tanpa membuat object.

## Tasks

### Task 1
Buat class `MathHelper` dengan sebuah method yang ditandai keyword `static`.

### Task 2
Method tersebut menerima satu parameter angka dan mengembalikan hasil kuadratnya.

### Task 3
Panggil method itu langsung dari nama class-nya, tanpa membuat object menggunakan `new`.

## Results / Test Cases

### Test Case 1
```
Input: MathHelper.kuadrat(5)
Output: 25
```

### Test Case 2
```
Input: MathHelper.kuadrat(9)
Output: 81
```

## Tips dan Trik

- Static method melekat pada class itu sendiri, bukan pada object hasil `new`, sehingga dipanggil dengan `NamaClass.namaMethod()`.
