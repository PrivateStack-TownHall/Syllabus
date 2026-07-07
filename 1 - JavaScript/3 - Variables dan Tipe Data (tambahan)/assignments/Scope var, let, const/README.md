# Assignment - Scope `var`, `let`, dan `const` (Medium)

## Tujuan Pembelajaran

- Memahami konsep scope dalam JavaScript.
- Memahami perbedaan scope pada `var`, `let`, dan `const`.
- Mampu mengidentifikasi variabel yang dapat diakses di dalam maupun di luar block.
- Mampu menjelaskan pengaruh block scope terhadap penggunaan variabel.

## Soal

Buatlah sebuah program yang menunjukkan perbedaan **scope** antara `var`, `let`, dan `const` di dalam sebuah block `if`.

Deklarasikan masing-masing variabel di dalam block, kemudian coba akses variabel tersebut dari luar block. Amati hasil yang diperoleh, lalu jelaskan mengapa setiap variabel memiliki perilaku yang berbeda.

> **Catatan:** Fokus utama assignment ini adalah memahami bahwa `var` memiliki **function scope**, sedangkan `let` dan `const` memiliki **block scope**.

## Result / Test Case

**Contoh Output**

```text
var di dalam block

ReferenceError: b is not defined
ReferenceError: c is not defined
```
