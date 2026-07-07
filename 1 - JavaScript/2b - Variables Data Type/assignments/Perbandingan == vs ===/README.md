# Assignment - Perbandingan `==` vs `===` (Hard)

## Tujuan Pembelajaran

- Memahami perbedaan antara operator `==` dan `===` di JavaScript.
- Memahami konsep _implicit type coercion_ saat melakukan perbandingan.
- Mampu menganalisis hasil perbandingan dari berbagai tipe data.
- Mampu menentukan kapan sebaiknya menggunakan `==` atau `===` dalam penulisan kode.

## Soal

Buatlah **minimal lima contoh perbandingan** menggunakan operator `==` dan `===` dengan kombinasi nilai yang berbeda. Tampilkan hasilnya menggunakan `console.log()`.

Setelah itu, jelaskan melalui komentar mengapa setiap perbandingan menghasilkan nilai tersebut, kemudian tuliskan kesimpulan mengapa operator `===` lebih disarankan dalam penulisan kode JavaScript.

> **Catatan:** Fokus utama assignment ini adalah memahami perbedaan cara kerja operator `==` dan `===`, serta memahami pengaruh _implicit type coercion_ terhadap hasil perbandingan.

## Result / Test Case

**Contoh Input**

```javascript
console.log(1 == "1");
console.log(1 === "1");
console.log(null == undefined);
console.log(null === undefined);
console.log(false == "0");
```

**Contoh Output**

```text
true
false
true
false
true
```

> Nilai di atas hanyalah contoh. Kamu dapat menggunakan kombinasi perbandingan lain selama tetap menunjukkan perbedaan perilaku antara operator `==` dan `===`, serta memberikan penjelasan yang benar.
