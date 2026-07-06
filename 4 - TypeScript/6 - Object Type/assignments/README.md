# Tujuan Pembelajaran
- Mampu mendeklarasikan object type secara inline
- Memahami optional property dan readonly property
- Mampu menggunakan nested object type
- Memahami index signature pada object type

---

# Assignment 1 - Object Type Inline (Easy)
Deklarasikan object dengan tipe inline untuk properti nama dan umur.

```ts
let siswa: { nama: string; umur: number } = {
  nama: "Vincent",
  umur: 25,
};

console.log(siswa);
```

**Hasil yang diharapkan:**
```
{ nama: 'Vincent', umur: 25 }
```

---

# Assignment 2 - Optional Property (Easy)
Buat object type dengan properti `email` yang bersifat optional.

```ts
let siswa: { nama: string; email?: string } = { nama: "Vincent" };

console.log(siswa);
```

**Hasil yang diharapkan:**
```
{ nama: 'Vincent' }
```

---

# Assignment 3 - Readonly Property (Easy)
Buat object type dengan properti `id` bersifat readonly.

```ts
let produk: { readonly id: number; nama: string } = { id: 1, nama: "Mouse" };
// produk.id = 2; // akan error

console.log(produk);
```

**Hasil yang diharapkan:**
```
{ id: 1, nama: 'Mouse' }
```

---

# Assignment 4 - Function sebagai Properti Object (Easy)
Buat object dengan properti berupa function di dalamnya.

```ts
let kalkulator: { tambah: (a: number, b: number) => number } = {
  tambah: (a, b) => a + b,
};

console.log(kalkulator.tambah(5, 3));
```

**Hasil yang diharapkan:**
```
8
```

---

# Assignment 5 - Nested Object Type (Easy)
Buat object type dengan properti bertipe object di dalamnya (nested).

```ts
let siswa: { nama: string; alamat: { kota: string; provinsi: string } } = {
  nama: "Vincent",
  alamat: { kota: "Bekasi", provinsi: "Jawa Barat" },
};

console.log(siswa);
```

**Hasil yang diharapkan:**
```
{ nama: 'Vincent', alamat: { kota: 'Bekasi', provinsi: 'Jawa Barat' } }
```

---

# Assignment 6 - Index Signature (Medium)
Buat object type dengan index signature untuk menyimpan data harga produk dengan key berupa nama produk.

```ts
let hargaProduk: { [namaProduk: string]: number } = {
  Mouse: 150000,
  Keyboard: 300000,
};

console.log(hargaProduk["Mouse"]);
```

**Hasil yang diharapkan:**
```
150000
```

---

# Assignment 7 - Kombinasi Optional dan Readonly (Medium)
Buat object type untuk data produk dengan `id` readonly dan `deskripsi` optional.

```ts
let produk: { readonly id: number; nama: string; deskripsi?: string } = {
  id: 1,
  nama: "Laptop",
};

console.log(produk);
```

**Hasil yang diharapkan:**
```
{ id: 1, nama: 'Laptop' }
```

---

# Assignment 8 - Object Type Kompleks (Hard)
Buat object type untuk data pesanan yang memiliki nested array of object di dalamnya (misalnya daftar item pesanan).

```ts
let pesanan: {
  idPesanan: number;
  items: { nama: string; jumlah: number; harga: number }[];
} = {
  idPesanan: 1,
  items: [
    { nama: "Kopi", jumlah: 2, harga: 20000 },
    { nama: "Roti", jumlah: 1, harga: 15000 },
  ],
};

console.log(pesanan);
```

**Hasil yang diharapkan:**
```
{
  idPesanan: 1,
  items: [
    { nama: 'Kopi', jumlah: 2, harga: 20000 },
    { nama: 'Roti', jumlah: 1, harga: 15000 }
  ]
}
```
