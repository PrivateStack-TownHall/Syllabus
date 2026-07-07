# Assignment - Deep Clone Object (Hard)

## Tujuan Pembelajaran

- Memahami konsep _shallow copy_ dan _deep clone_ pada object.
- Mampu melakukan proses _deep clone_ secara manual tanpa menggunakan library eksternal.
- Mampu mengolah object yang memiliki nested object.
- Memahami pentingnya membuat salinan object tanpa memengaruhi data asli.

## Soal

Buatlah sebuah function berikut.

```javascript
const deepClone = (obj) => {
  // code here
};
```

Function menerima sebuah **object** yang memiliki **nested object**, kemudian mengembalikan **object baru** yang merupakan hasil **deep clone**.

Setelah object berhasil di-_clone_, ubahlah salah satu properti pada object hasil clone untuk membuktikan bahwa object asli **tidak ikut berubah**.

**Ketentuan:**

- Tidak diperbolehkan menggunakan library eksternal.
- Tidak diperbolehkan menggunakan `structuredClone()`.
- Tidak diperbolehkan menggunakan `JSON.parse(JSON.stringify())`.

### Validasi

- Jika parameter bukan object, tampilkan `"Input harus berupa object."`
- Jika parameter bernilai `null`, tampilkan `"Object tidak boleh null."`
- Jika object kosong, kembalikan object kosong.

---

## Result / Test Case

```javascript
// Test Case 1

const person = {
  name: "Vincent",
  address: {
    city: "Bekasi",
  },
};

const cloned = deepClone(person);

cloned.address.city = "Jakarta";

console.log(person.address.city);
console.log(cloned.address.city);

// Output
Bekasi;
Jakarta;

// Test Case 2

deepClone({});

// Output
{
}

// Test Case 3

deepClone(null);

// Output
("Object tidak boleh null.");

// Test Case 4

deepClone("Hello");

// Output
("Input harus berupa object.");
```
