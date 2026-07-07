# Assignment - Operator Precedence (Hard)

## Tujuan Pembelajaran

- Memahami konsep _operator precedence_ pada JavaScript.
- Memahami urutan evaluasi operator dalam sebuah expression.
- Mampu menganalisis expression yang terdiri dari beberapa jenis operator.
- Mampu memprediksi hasil evaluasi sebuah expression sebelum program dijalankan.

## Soal

Perhatikan expression berikut.

```javascript
(3 + 4 * 2 > 10 && 5 < 6) || false;
```

Sebelum menjalankan program, **prediksikan terlebih dahulu** hasil dari expression tersebut beserta urutan proses evaluasinya.

Setelah itu, buktikan jawabanmu menggunakan `console.log()`, lalu jelaskan mengapa expression tersebut menghasilkan nilai tersebut berdasarkan aturan **operator precedence** di JavaScript.

> **Catatan:** Fokus utama assignment ini adalah memahami urutan prioritas operator (_operator precedence_) saat JavaScript mengevaluasi sebuah expression yang terdiri dari operator aritmatika, perbandingan, dan logika.

## Result / Test Case

**Input**

```javascript
console.log((3 + 4 * 2 > 10 && 5 < 6) || false);
```

**Output**

```text
true
```
