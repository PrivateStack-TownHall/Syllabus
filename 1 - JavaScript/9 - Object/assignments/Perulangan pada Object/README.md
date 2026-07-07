# Assignment - Perulangan pada Object dengan `for...in` (Easy)

## Tujuan Pembelajaran

- Memahami cara melakukan iterasi pada object menggunakan `for...in`.
- Mampu mengakses nama properti (key) dan nilai (value) dari sebuah object.
- Mampu membuat function yang menerima object sebagai parameter.
- Mampu menampilkan seluruh isi object menggunakan perulangan.

## Soal

Buatlah sebuah function berikut.

```javascript
const showPerson = (person) => {
  // code here
};
```

Function menerima sebuah object `person`, kemudian tampilkan seluruh **key** beserta **value** menggunakan perulangan **`for...in`**.

Format output:

```text
nama: Vincent
umur: 25
pekerjaan: Frontend Developer
```

> **Catatan:** Fokus utama assignment ini adalah memahami penggunaan `for...in` untuk melakukan iterasi pada seluruh properti object.

### Validasi

- Jika `person` bukan object, tampilkan `"Person harus berupa object."`
- Jika `person` bernilai `null`, tampilkan `"Object tidak boleh null."`
- Jika object tidak memiliki properti, tampilkan `"Object kosong."`

---

## Result / Test Case

```javascript
// Test Case 1
showPerson({
  nama: "Vincent",
  umur: 25,
  pekerjaan: "Frontend Developer",
});

// Output
nama: Vincent
umur: 25
pekerjaan: Frontend Developer


// Test Case 2
showPerson({
  nama: "Budi",
  umur: 30,
});

// Output
nama: Budi
umur: 30


// Test Case 3
showPerson({});

// Output
"Object kosong."


// Test Case 4
showPerson(null);

// Output
"Object tidak boleh null."


// Test Case 5
showPerson("Hello");

// Output
"Person harus berupa object."
```
