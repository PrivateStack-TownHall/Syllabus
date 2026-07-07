# Assignment - Closure Counter (Hard)

## Tujuan Pembelajaran

- Memahami konsep **closure** dalam JavaScript.
- Memahami hubungan antara function dan lexical scope.
- Mampu membuat function yang menyimpan state menggunakan closure.
- Mampu mengimplementasikan closure untuk menyelesaikan permasalahan sederhana.

## Soal

Buatlah sebuah **function** yang memanfaatkan konsep **closure** untuk membuat sebuah **counter**.

Counter harus tetap menyimpan nilai terakhirnya setiap kali function dipanggil, sehingga nilai counter akan terus bertambah pada setiap pemanggilan berikutnya.

> **Catatan:** Fokus utama assignment ini adalah memahami bagaimana **closure** memungkinkan sebuah function tetap mengakses variabel dari scope luarnya, meskipun function tersebut telah selesai dieksekusi.

## Result / Test Case

**Input**

```javascript
counter();
counter();
counter();
```

**Output**

```text
1
2
3
```
