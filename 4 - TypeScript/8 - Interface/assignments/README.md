# Tujuan Pembelajaran
- Memahami konsep interface dan kegunaannya
- Mampu membuat interface untuk object dan function
- Memahami extends pada interface
- Mampu menggabungkan interface menggunakan declaration merging

---

# Assignment 1 - Interface Sederhana (Easy)
Buat interface `Siswa` untuk mendeskripsikan object siswa (nama, umur).

```ts
interface Siswa {
  nama: string;
  umur: number;
}

let siswa1: Siswa = { nama: "Vincent", umur: 25 };

console.log(siswa1);
```

**Hasil yang diharapkan:**
```
{ nama: 'Vincent', umur: 25 }
```

---

# Assignment 2 - Optional Property pada Interface (Easy)
Buat interface `Produk` dengan properti `deskripsi` bersifat optional.

```ts
interface Produk {
  nama: string;
  harga: number;
  deskripsi?: string;
}

let produk1: Produk = { nama: "Mouse", harga: 150000 };

console.log(produk1);
```

**Hasil yang diharapkan:**
```
{ nama: 'Mouse', harga: 150000 }
```

---

# Assignment 3 - Readonly Property pada Interface (Easy)
Buat interface dengan properti `id` bersifat readonly.

```ts
interface User {
  readonly id: number;
  nama: string;
}

let user1: User = { id: 1, nama: "Vincent" };
// user1.id = 2; // akan error

console.log(user1);
```

**Hasil yang diharapkan:**
```
{ id: 1, nama: 'Vincent' }
```

---

# Assignment 4 - Interface untuk Function (Easy)
Buat interface untuk mendeskripsikan tipe function.

```ts
interface OperasiMatematika {
  (a: number, b: number): number;
}

const tambah: OperasiMatematika = (a, b) => a + b;

console.log(tambah(5, 10));
```

**Hasil yang diharapkan:**
```
15
```

---

# Assignment 5 - Interface untuk Array of Object (Easy)
Buat interface `Siswa`, lalu gunakan untuk membuat array of Siswa.

```ts
interface Siswa {
  nama: string;
  umur: number;
}

let daftarSiswa: Siswa[] = [
  { nama: "Vincent", umur: 25 },
  { nama: "Budi", umur: 22 },
];

console.log(daftarSiswa);
```

**Hasil yang diharapkan:**
```
[ { nama: 'Vincent', umur: 25 }, { nama: 'Budi', umur: 22 } ]
```

---

# Assignment 6 - Extends pada Interface (Medium)
Buat interface `Karyawan` yang extends dari interface `Manusia`.

```ts
interface Manusia {
  nama: string;
  umur: number;
}

interface Karyawan extends Manusia {
  jabatan: string;
  gaji: number;
}

let karyawan1: Karyawan = {
  nama: "Vincent",
  umur: 25,
  jabatan: "Frontend Developer",
  gaji: 8000000,
};

console.log(karyawan1);
```

**Hasil yang diharapkan:**
```
{ nama: 'Vincent', umur: 25, jabatan: 'Frontend Developer', gaji: 8000000 }
```

---

# Assignment 7 - Interface dengan Method (Medium)
Buat interface `Kendaraan` yang memiliki method `nyalakanMesin()`, lalu implementasikan pada sebuah object.

```ts
interface Kendaraan {
  merk: string;
  nyalakanMesin(): void;
}

let mobil: Kendaraan = {
  merk: "Toyota",
  nyalakanMesin() {
    console.log(this.merk + ": Mesin menyala!");
  },
};

mobil.nyalakanMesin();
```

**Hasil yang diharapkan:**
```
Toyota: Mesin menyala!
```

---

# Assignment 8 - Declaration Merging (Hard)
Buktikan bahwa dua interface dengan nama yang sama akan otomatis digabung (declaration merging) oleh TypeScript.

```ts
interface Produk {
  nama: string;
}

interface Produk {
  harga: number;
}

let produk1: Produk = { nama: "Mouse", harga: 150000 };

console.log(produk1);
```

**Hasil yang diharapkan:**
```
{ nama: 'Mouse', harga: 150000 }
```
