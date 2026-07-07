# Assignment - Operasi Campuran Tipe Data (Medium)

## Tujuan Pembelajaran

- Memahami konsep _implicit type coercion_ pada JavaScript.
- Memahami perbedaan perilaku operator aritmatika terhadap tipe data yang berbeda.
- Mampu menganalisis hasil operasi yang melibatkan tipe data `string` dan `number`.
- Mampu menjelaskan alasan di balik hasil yang diperoleh dari suatu operasi.

## Soal

Prediksikan terlebih dahulu hasil dari operasi berikut tanpa menjalankan program.

```javascript
"5" + 3;
"5" - 3;
```

Setelah itu, buktikan prediksimu menggunakan `console.log()`, kemudian jelaskan melalui komentar mengapa kedua operasi tersebut menghasilkan nilai yang berbeda.

> **Catatan:** Fokus utama assignment ini adalah memahami bagaimana JavaScript melakukan _implicit type coercion_ saat melakukan operasi dengan tipe data yang berbeda.

## Result / Test Case

**Input**

```javascript
console.log("5" + 3);
console.log("5" - 3);
```

**Output**

```text
53
2
```
