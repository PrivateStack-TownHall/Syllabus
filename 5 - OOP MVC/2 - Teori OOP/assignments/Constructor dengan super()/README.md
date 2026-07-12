# Constructor dengan super() (Easy)

## Tujuan Pembelajaran

- Memahami 4 pilar utama OOP: enkapsulasi, inheritance, polimorfisme, dan abstraksi
- Mampu menerapkan enkapsulasi menggunakan private field (`#`)
- Mampu membuat inheritance antar class menggunakan `extends` dan `super`
- Mampu menerapkan polimorfisme melalui method overriding

## Soal

Buat class `Karyawan` yang extends dari class `Manusia`, gunakan `super()` di dalam constructor-nya untuk memanggil constructor parent.

## Tasks

### Task 1
Buat class `Manusia` dengan constructor yang menyimpan `nama`.

### Task 2
Buat class `Karyawan` yang extends `Manusia`, dengan constructor tambahan menerima `jabatan`.

### Task 3
Di dalam constructor `Karyawan`, panggil `super(nama)` sebelum menyimpan property `jabatan`.

## Results / Test Cases

### Test Case 1
```
Input: new Karyawan("Vincent", "Developer")
Output: Karyawan { nama: 'Vincent', jabatan: 'Developer' }
```

## Tips dan Trik

- `super(...)` wajib dipanggil sebelum menggunakan `this` di dalam constructor class turunan.
