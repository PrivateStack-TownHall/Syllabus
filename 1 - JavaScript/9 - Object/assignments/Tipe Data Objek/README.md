# Assignment - Tipe Data Reference (Easy)

## Tujuan Pembelajaran

- Memahami perbedaan antara tipe data primitif dan tipe data reference.
- Mengenal tipe data `Object`, `Array`, dan `Function` di JavaScript.
- Mampu membuat contoh dari setiap tipe data reference.
- Mampu mengidentifikasi tipe data menggunakan operator `typeof`.

## Soal

Buatlah sebuah function berikut.

```javascript
const checkReferenceType = (data) => {
  // code here
};
```

Function menerima sebuah parameter `data`, kemudian mengembalikan hasil dari operator `typeof`.

Gunakan function tersebut untuk mengecek tipe data dari:

- Object
- Array
- Function

> **Catatan:** Fokus utama assignment ini adalah memahami bahwa `Object`, `Array`, dan `Function` merupakan tipe data **reference**, serta mengetahui hasil yang dikembalikan oleh operator `typeof`.

### Validasi

- Jika parameter tidak diberikan, tampilkan `"Parameter wajib diisi."`

---

## Result / Test Case

```javascript
// Test Case 1
checkReferenceType({
  nama: "Vincent",
});

// Output
("object");

// Test Case 2
checkReferenceType([1, 2, 3]);

// Output
("object");

// Test Case 3
checkReferenceType(() => {});

// Output
("function");

// Test Case 4
checkReferenceType();

// Output
("Parameter wajib diisi.");
```
