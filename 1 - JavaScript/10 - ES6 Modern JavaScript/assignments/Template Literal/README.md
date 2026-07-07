# Assignment - Template Literal (Easy)

## Tujuan Pembelajaran

- Memahami penggunaan template literal.
- Mampu menggabungkan beberapa variabel menjadi satu string.
- Memahami sintaks `${}` pada template literal.
- Mampu mengembalikan string menggunakan function.

## Soal

Buatlah sebuah function berikut.

```javascript
const createCompanyInfo = (brand, service) => {
  // code here
};
```

Function menerima dua parameter:

- `brand`
- `service`

Kemudian kembalikan kalimat berikut menggunakan **template literal**.

```text
<brand> menyediakan layanan <service>.
```

### Validasi

- Jika salah satu parameter bukan string, tampilkan `"Semua parameter harus berupa string."`
- Jika salah satu parameter kosong, tampilkan `"Parameter tidak boleh kosong."`

---

## Result / Test Case

```javascript
// Test Case 1
createCompanyInfo("Sekolah Stack", "Web Development");

// Output
("Sekolah Stack menyediakan layanan Web Development.");

// Test Case 2
createCompanyInfo("OpenAI", "Artificial Intelligence");

// Output
("OpenAI menyediakan layanan Artificial Intelligence.");

// Test Case 3
createCompanyInfo("", "Web");

// Output
("Parameter tidak boleh kosong.");

// Test Case 4
createCompanyInfo("Admin", 123);

// Output
("Semua parameter harus berupa string.");
```
