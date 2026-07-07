# Assignment - Temporal Dead Zone (Medium)

## Tujuan Pembelajaran

- Memahami konsep _Temporal Dead Zone_ (TDZ) pada JavaScript.
- Memahami perilaku variabel yang dideklarasikan menggunakan `let` dan `const`.
- Mampu membedakan hoisting pada `var` dengan `let` dan `const`.
- Mampu menjelaskan penyebab terjadinya `ReferenceError` akibat TDZ.

## Soal

Buatlah sebuah program yang membuktikan konsep **Temporal Dead Zone (TDZ)** dengan mencoba mengakses sebuah variabel yang dideklarasikan menggunakan `let` **sebelum** variabel tersebut dideklarasikan.

Jalankan program tersebut, amati error yang muncul, kemudian jelaskan mengapa error tersebut dapat terjadi.

> **Catatan:** Fokus utama assignment ini adalah memahami bahwa variabel yang dideklarasikan menggunakan `let` dan `const` memang mengalami _hoisting_, tetapi tidak dapat diakses sebelum proses deklarasi selesai karena berada di dalam **Temporal Dead Zone (TDZ)**.

## Result / Test Case

**Contoh Output**

```text
ReferenceError: Cannot access 'skor' before initialization
```
