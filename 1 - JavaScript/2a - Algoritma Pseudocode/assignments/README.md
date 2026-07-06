# Tujuan Pembelajaran
- Memahami konsep algoritma dan pseudocode
- Mampu menerjemahkan logika pemecahan masalah ke dalam pseudocode
- Mampu menyusun pseudocode untuk percabangan dan perulangan
- Mampu menyusun pseudocode untuk algoritma sorting sederhana

---

# Assignment 1 - Apa itu Algoritma (Easy)
Tuliskan definisi algoritma dengan bahasamu sendiri, beserta satu contoh algoritma dalam kehidupan sehari-hari.

```
Contoh pseudocode: "Cara membuat mie instan"
MULAI
  Didihkan air
  Masukkan mie
  Tunggu 3 menit
  Tiriskan
  Tambahkan bumbu
SELESAI
```

**Hasil yang diharapkan:**
```
(tidak ada output kode, berupa penjelasan tertulis + contoh pseudocode)
```

---

# Assignment 2 - Cek Ganjil Genap (Easy)
Buat pseudocode untuk menentukan apakah sebuah angka ganjil atau genap.

```
MULAI
  INPUT angka
  JIKA angka MOD 2 = 0 MAKA
    TULIS "Genap"
  SEBALIKNYA
    TULIS "Ganjil"
  AKHIR JIKA
SELESAI
```

**Hasil yang diharapkan:**
```
Input: 7 -> Output: Ganjil
Input: 10 -> Output: Genap
```

---

# Assignment 3 - Flowchart vs Pseudocode (Easy)
Jelaskan perbedaan flowchart dan pseudocode, lalu ubah pseudocode soal nomor 2 menjadi penjelasan alur flowchart (dalam bentuk daftar langkah).

```
Flowchart (dalam bentuk teks):
1. Start (Oval)
2. Input angka (Parallelogram)
3. Decision: angka MOD 2 = 0? (Diamond)
4. Ya -> Cetak "Genap" (Rectangle)
5. Tidak -> Cetak "Ganjil" (Rectangle)
6. End (Oval)
```

**Hasil yang diharapkan:**
```
(tidak ada output kode, berupa penjelasan alur)
```

---

# Assignment 4 - Penjumlahan Dua Angka (Easy)
Buat pseudocode untuk menjumlahkan dua buah angka yang diinput user.

```
MULAI
  INPUT angka1
  INPUT angka2
  total = angka1 + angka2
  TULIS total
SELESAI
```

**Hasil yang diharapkan:**
```
Input: 5, 10 -> Output: 15
```

---

# Assignment 5 - Struktur Percabangan (Easy)
Buat pseudocode untuk menentukan kelulusan siswa berdasarkan nilai (lulus jika nilai >= 75).

```
MULAI
  INPUT nilai
  JIKA nilai >= 75 MAKA
    TULIS "Lulus"
  SEBALIKNYA
    TULIS "Tidak Lulus"
  AKHIR JIKA
SELESAI
```

**Hasil yang diharapkan:**
```
Input: 80 -> Output: Lulus
Input: 60 -> Output: Tidak Lulus
```

---

# Assignment 6 - Nilai Terbesar dari 3 Angka (Medium)
Buat pseudocode untuk mencari nilai terbesar dari 3 buah angka yang diinput user.

```
MULAI
  INPUT a, b, c
  JIKA a > b DAN a > c MAKA
    TULIS a, "adalah yang terbesar"
  SEBALIKNYA JIKA b > c MAKA
    TULIS b, "adalah yang terbesar"
  SEBALIKNYA
    TULIS c, "adalah yang terbesar"
  AKHIR JIKA
SELESAI
```

**Hasil yang diharapkan:**
```
Input: 5, 9, 3 -> Output: 9 adalah yang terbesar
```

---

# Assignment 7 - Total dari 1 hingga N (Medium)
Buat pseudocode untuk menghitung total penjumlahan angka dari 1 hingga N menggunakan perulangan.

```
MULAI
  INPUT n
  total = 0
  UNTUK i = 1 SAMPAI n
    total = total + i
  AKHIR UNTUK
  TULIS total
SELESAI
```

**Hasil yang diharapkan:**
```
Input: 5 -> Output: 15 (1+2+3+4+5)
```

---

# Assignment 8 - Bubble Sort (Hard)
Buat pseudocode untuk mengurutkan array angka dari terkecil ke terbesar menggunakan algoritma bubble sort.

```
MULAI
  INPUT array[n]
  UNTUK i = 0 SAMPAI n-1
    UNTUK j = 0 SAMPAI n-i-2
      JIKA array[j] > array[j+1] MAKA
        TUKAR array[j] DENGAN array[j+1]
      AKHIR JIKA
    AKHIR UNTUK
  AKHIR UNTUK
  TULIS array
SELESAI
```

**Hasil yang diharapkan:**
```
Input: [5, 2, 9, 1, 5] -> Output: [1, 2, 5, 5, 9]
```
