# Assignment - Default Parameter (Easy)

## Tujuan Pembelajaran

- Memahami konsep _default parameter_ pada JavaScript.
- Mampu membuat function dengan parameter default.
- Mampu menangani parameter yang tidak diberikan saat function dipanggil.
- Mampu menggunakan _default parameter_ untuk membuat function yang lebih fleksibel.

## Soal

Buatlah sebuah **function** bernama `sapa` yang menerima satu parameter, yaitu `nama`.

Gunakan **default parameter** dengan nilai **`"Guest"`** apabila parameter `nama` tidak diberikan saat function dipanggil.

Function harus menampilkan sapaan sesuai dengan nama yang diterima.

> **Catatan:** Fokus utama assignment ini adalah memahami cara kerja _default parameter_ untuk memberikan nilai bawaan ketika sebuah parameter tidak diisi.

## Result / Test Case

**Input**

```javascript
sapa();
sapa("Vincent");
```

**Output**

```text
Halo, Guest!
Halo, Vincent!
```
