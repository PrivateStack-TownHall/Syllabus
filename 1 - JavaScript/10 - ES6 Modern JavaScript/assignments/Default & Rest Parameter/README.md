# Assignment - Default Parameter dan Rest Parameter (Medium)

## Tujuan Pembelajaran

- Memahami penggunaan **default parameter** pada function.
- Memahami penggunaan **rest parameter** untuk menerima jumlah argument yang tidak tetap.
- Mampu menggabungkan **default parameter** dan **rest parameter** dalam satu function.
- Mampu mengolah data menggunakan parameter modern pada ES6.

## Soal

Buatlah sebuah function berikut.

```javascript
const createAnnouncement = (title = "Pengumuman", ...messages) => {
  // code here
};
```

Function menerima:

- Satu **default parameter** `title` dengan nilai default `"Pengumuman"`.
- Sejumlah **rest parameter** `messages`.

Function harus mengembalikan string dengan format berikut.

```text
<title>: <pesan1>, <pesan2>, <pesan3>
```

Gunakan `join(", ")` untuk menggabungkan seluruh isi `messages`.

> **Catatan:** Fokus utama assignment ini adalah memahami cara menggabungkan **default parameter** dan **rest parameter** dalam satu function.

### Validasi

- Jika `title` bukan string, tampilkan `"Title harus berupa string."`
- Jika tidak ada pesan yang diberikan, tampilkan `"Minimal satu pesan harus diberikan."`

---

## Result / Test Case

```javascript
// Test Case 1
createAnnouncement(undefined, "Libur", "Besok", "Ujian");

// Output
("Pengumuman: Libur, Besok, Ujian");

// Test Case 2
createAnnouncement("Info", "Meeting", "Jam 09.00");

// Output
("Info: Meeting, Jam 09.00");

// Test Case 3
createAnnouncement();

// Output
("Minimal satu pesan harus diberikan.");

// Test Case 4
createAnnouncement(123, "Libur");

// Output
("Title harus berupa string.");

// Test Case 5
createAnnouncement("Reminder", "Bawa Laptop");

// Output
("Reminder: Bawa Laptop");
```
