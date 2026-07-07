# Assignment - Enhanced Object Literal (Easy)

## Tujuan Pembelajaran

- Memahami konsep **Enhanced Object Literal** pada ES6.
- Mampu membuat object menggunakan shorthand property.
- Mampu membuat method menggunakan shorthand method.
- Mampu memanfaatkan sintaks ES6 untuk membuat object yang lebih ringkas.

## Soal

Buatlah sebuah function berikut.

```javascript
const createStudent = (name, age, studentClass) => {
  // code here
};
```

Function menerima tiga parameter:

- `name`
- `age`
- `studentClass`

Kemudian kembalikan sebuah object menggunakan **Enhanced Object Literal** dengan struktur berikut.

```javascript
{
  name,
  age,
  studentClass,
  introduce() {
    // code here
  }
}
```

Method `introduce()` harus mengembalikan string dengan format:

```text
Halo, saya Vincent dari kelas 12A.
```

> **Catatan:** Fokus utama assignment ini adalah memahami penggunaan **shorthand property** dan **shorthand method** pada Enhanced Object Literal.

### Validasi

- Jika `name` bukan string atau string kosong, tampilkan `"Name harus berupa string."`
- Jika `age` bukan number atau kurang dari 0, tampilkan `"Age tidak valid."`
- Jika `studentClass` bukan string atau string kosong, tampilkan `"Class harus berupa string."`

---

## Result / Test Case

```javascript
// Test Case 1
const student = createStudent("Vincent", 17, "12A");

student.introduce();

// Output
("Halo, saya Vincent dari kelas 12A.");

// Test Case 2
const student = createStudent("Budi", 16, "11B");

student.introduce();

// Output
("Halo, saya Budi dari kelas 11B.");

// Test Case 3
createStudent("", 17, "12A");

// Output
("Name harus berupa string.");

// Test Case 4
createStudent("Vincent", -1, "12A");

// Output
("Age tidak valid.");

// Test Case 5
createStudent("Vincent", 17, "");

// Output
("Class harus berupa string.");
```
