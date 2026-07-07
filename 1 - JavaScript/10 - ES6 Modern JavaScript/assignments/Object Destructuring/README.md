# Assignment - Object Destructuring (Medium)

## Tujuan Pembelajaran

- Memahami konsep object destructuring.
- Mampu mengambil properti tertentu dari object.
- Mampu menggunakan destructuring di dalam function.
- Mampu mengembalikan hasil menggunakan `return`.

## Soal

Buatlah sebuah function berikut.

```javascript
const showCourse = (course) => {
  // code here
};
```

Function menerima object berikut.

```javascript
{
  title: "",
  mentor: "",
  duration: 0
}
```

Gunakan **object destructuring** untuk mengambil `title` dan `duration`, kemudian kembalikan hasil dengan format:

```text
<title> - <duration> hari
```

### Validasi

- Jika parameter bukan object, tampilkan `"Course harus berupa object."`
- Jika `title` atau `duration` tidak tersedia, tampilkan `"Data course tidak lengkap."`

---

## Result / Test Case

```javascript
// Test Case 1
showCourse({
  title: "JavaScript Dasar",
  mentor: "Andi",
  duration: 5,
});

// Output
("JavaScript Dasar - 5 hari");

// Test Case 2
showCourse({
  title: "React",
  mentor: "Budi",
  duration: 7,
});

// Output
("React - 7 hari");

// Test Case 3
showCourse({
  title: "NodeJS",
});

// Output
("Data course tidak lengkap.");

// Test Case 4
showCourse("Hello");

// Output
("Course harus berupa object.");
```
