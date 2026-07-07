# Assignment - Block Scope dalam Perulangan (Hard)

## Tujuan Pembelajaran

- Memahami perbedaan scope pada `var` dan `let`.
- Memahami konsep block scope dalam JavaScript.
- Mampu menganalisis perilaku variabel di dalam perulangan (`loop`).
- Memahami hubungan antara closure dan scope pada function.

## Soal

Buatlah dua buah perulangan `for` dengan ketentuan berikut:

1. Perulangan pertama menggunakan `var`.
2. Perulangan kedua menggunakan `let`.

Pada setiap iterasi, simpan sebuah **function** ke dalam sebuah array. Setelah seluruh proses perulangan selesai, panggil setiap function yang telah disimpan, kemudian amati hasil yang ditampilkan.

Selanjutnya, jelaskan mengapa hasil yang diperoleh dari penggunaan `var` dan `let` berbeda.

> **Catatan:** Fokus utama assignment ini adalah memahami perbedaan **function scope** dan **block scope**, serta bagaimana keduanya memengaruhi nilai variabel yang diakses oleh sebuah function (closure).

## Result / Test Case

**Contoh Output**

```text
var: 3
var: 3
var: 3

let: 0
let: 1
let: 2
```
