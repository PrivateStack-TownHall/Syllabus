# Property dan Constructor (Easy)

## Tujuan Pembelajaran

- Memahami konsep dasar Object-Oriented Programming (OOP)
- Mampu membuat class dan object di JavaScript
- Memahami constructor dan property dalam class
- Mampu membuat dan memanggil method di dalam class

## Soal

Buat class `Siswa` dengan constructor yang menerima `nama` dan `umur`, lalu tampilkan object yang terbentuk.

## Tasks

### Task 1
Buat class `Siswa` dengan constructor yang menerima parameter `nama` dan `umur`.

### Task 2
Simpan kedua parameter tersebut sebagai property object menggunakan `this`, lalu buat satu object dan tampilkan hasilnya dengan `console.log`.

## Results / Test Cases

### Test Case 1
```
Input: new Siswa("Vincent", 25)
Output: Siswa { nama: 'Vincent', umur: 25 }
```

### Test Case 2
```
Input: new Siswa("Budi", 22)
Output: Siswa { nama: 'Budi', umur: 22 }
```

## Tips dan Trik

- Saat sebuah object di-`console.log`, JavaScript otomatis menampilkan nama class beserta seluruh property-nya.
