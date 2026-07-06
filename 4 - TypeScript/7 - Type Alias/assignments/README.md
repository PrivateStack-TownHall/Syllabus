# Tujuan Pembelajaran
- Memahami konsep type alias dan kegunaannya
- Mampu membuat type alias untuk object, union, dan function
- Memahami perbedaan type alias dengan interface
- Mampu menggabungkan beberapa type alias menggunakan intersection

---

# Assignment 1 - Type Alias Sederhana (Easy)
Buat type alias `ID` yang merupakan union dari `string` dan `number`.

```ts
type ID = string | number;

let userId: ID = 101;
let orderId: ID = "ORD-101";

console.log(userId, orderId);
```

**Hasil yang diharapkan:**
```
101 ORD-101
```

---

# Assignment 2 - Type Alias untuk Object (Easy)
Buat type alias `Siswa` untuk mendeskripsikan object siswa (nama, umur).

```ts
type Siswa = {
  nama: string;
  umur: number;
};

let siswa1: Siswa = { nama: "Vincent", umur: 25 };

console.log(siswa1);
```

**Hasil yang diharapkan:**
```
{ nama: 'Vincent', umur: 25 }
```

---

# Assignment 3 - Type Alias untuk Function (Easy)
Buat type alias untuk tipe function yang menerima dua number dan mengembalikan number.

```ts
type OperasiMatematika = (a: number, b: number) => number;

const tambah: OperasiMatematika = (a, b) => a + b;

console.log(tambah(5, 10));
```

**Hasil yang diharapkan:**
```
15
```

---

# Assignment 4 - Type Alias Union Literal (Easy)
Buat type alias `StatusPesanan` menggunakan union literal type.

```ts
type StatusPesanan = "pending" | "diproses" | "selesai";

let status: StatusPesanan = "diproses";

console.log(status);
```

**Hasil yang diharapkan:**
```
diproses
```

---

# Assignment 5 - Menggunakan Type Alias pada Array (Easy)
Buat type alias `Siswa` lalu gunakan untuk membuat array of Siswa.

```ts
type Siswa = { nama: string; umur: number };

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

# Assignment 6 - Intersection Type (Medium)
Gabungkan dua type alias menggunakan intersection (`&`) untuk membuat tipe `Karyawan` dari `Manusia` dan `Pekerjaan`.

```ts
type Manusia = { nama: string; umur: number };
type Pekerjaan = { jabatan: string; gaji: number };

type Karyawan = Manusia & Pekerjaan;

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

# Assignment 7 - Type Alias vs Interface (Medium)
Buat satu type alias dan satu interface yang mendeskripsikan struktur yang sama, lalu jelaskan perbedaan keduanya dalam komentar.

```ts
// menggunakan type alias
type ProdukType = { nama: string; harga: number };

// menggunakan interface
interface ProdukInterface {
  nama: string;
  harga: number;
}

let produk1: ProdukType = { nama: "Mouse", harga: 150000 };
let produk2: ProdukInterface = { nama: "Keyboard", harga: 300000 };

console.log(produk1, produk2);
```

**Hasil yang diharapkan:**
```
{ nama: 'Mouse', harga: 150000 } { nama: 'Keyboard', harga: 300000 }
```

---

# Assignment 8 - Kombinasi Union dan Intersection (Hard)
Buat type alias kompleks yang menggabungkan union dan intersection untuk mendeskripsikan dua jenis metode pembayaran (Transfer dan CreditCard) yang masing-masing punya properti tambahan berbeda.

```ts
type MetodeDasar = { totalBayar: number };
type Transfer = MetodeDasar & { tipe: "transfer"; bank: string };
type CreditCard = MetodeDasar & { tipe: "credit_card"; nomorKartu: string };

type Pembayaran = Transfer | CreditCard;

function prosesBayar(pembayaran: Pembayaran): void {
  if (pembayaran.tipe === "transfer") {
    console.log(`Transfer via ${pembayaran.bank} sebesar ${pembayaran.totalBayar}`);
  } else {
    console.log(`Kartu ${pembayaran.nomorKartu} sebesar ${pembayaran.totalBayar}`);
  }
}

prosesBayar({ tipe: "transfer", bank: "BCA", totalBayar: 100000 });
```

**Hasil yang diharapkan:**
```
Transfer via BCA sebesar 100000
```
