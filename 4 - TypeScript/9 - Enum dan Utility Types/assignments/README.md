# Tujuan Pembelajaran
- Memahami konsep enum dan kegunaannya
- Mampu membuat numeric enum dan string enum
- Memahami utility types dasar (Partial, Pick, Omit, Readonly)
- Mampu mengombinasikan enum dengan utility types

---

# Assignment 1 - Numeric Enum (Easy)
Buat enum `Hari` untuk merepresentasikan hari dalam seminggu.

```ts
enum Hari {
  Senin,
  Selasa,
  Rabu,
  Kamis,
  Jumat,
}

console.log(Hari.Rabu);
```

**Hasil yang diharapkan:**
```
2
```

---

# Assignment 2 - String Enum (Easy)
Buat enum `StatusPesanan` menggunakan string enum.

```ts
enum StatusPesanan {
  Pending = "PENDING",
  Diproses = "DIPROSES",
  Selesai = "SELESAI",
}

console.log(StatusPesanan.Diproses);
```

**Hasil yang diharapkan:**
```
DIPROSES
```

---

# Assignment 3 - Partial Utility Type (Easy)
Gunakan `Partial<T>` untuk membuat semua properti pada interface `Produk` menjadi optional.

```ts
interface Produk {
  nama: string;
  harga: number;
  stok: number;
}

let updateProduk: Partial<Produk> = { harga: 200000 };

console.log(updateProduk);
```

**Hasil yang diharapkan:**
```
{ harga: 200000 }
```

---

# Assignment 4 - Readonly Utility Type (Easy)
Gunakan `Readonly<T>` untuk membuat semua properti object menjadi readonly.

```ts
interface User {
  nama: string;
  email: string;
}

let user1: Readonly<User> = { nama: "Vincent", email: "vincent@email.com" };
// user1.nama = "Budi"; // akan error

console.log(user1);
```

**Hasil yang diharapkan:**
```
{ nama: 'Vincent', email: 'vincent@email.com' }
```

---

# Assignment 5 - Pick Utility Type (Easy)
Gunakan `Pick<T, K>` untuk mengambil sebagian properti dari interface `Produk`.

```ts
interface Produk {
  nama: string;
  harga: number;
  stok: number;
}

let ringkasanProduk: Pick<Produk, "nama" | "harga"> = {
  nama: "Mouse",
  harga: 150000,
};

console.log(ringkasanProduk);
```

**Hasil yang diharapkan:**
```
{ nama: 'Mouse', harga: 150000 }
```

---

# Assignment 6 - Omit Utility Type (Medium)
Gunakan `Omit<T, K>` untuk membuat tipe baru tanpa properti `stok` dari interface `Produk`.

```ts
interface Produk {
  nama: string;
  harga: number;
  stok: number;
}

let produkTanpaStok: Omit<Produk, "stok"> = {
  nama: "Keyboard",
  harga: 300000,
};

console.log(produkTanpaStok);
```

**Hasil yang diharapkan:**
```
{ nama: 'Keyboard', harga: 300000 }
```

---

# Assignment 7 - Enum dengan Function (Medium)
Buat function yang menerima parameter bertipe enum `StatusPesanan` dan menampilkan pesan berbeda untuk tiap status.

```ts
enum StatusPesanan {
  Pending = "PENDING",
  Diproses = "DIPROSES",
  Selesai = "SELESAI",
}

function cekStatus(status: StatusPesanan): string {
  switch (status) {
    case StatusPesanan.Pending:
      return "Pesanan menunggu diproses";
    case StatusPesanan.Diproses:
      return "Pesanan sedang diproses";
    case StatusPesanan.Selesai:
      return "Pesanan sudah selesai";
  }
}

console.log(cekStatus(StatusPesanan.Diproses));
```

**Hasil yang diharapkan:**
```
Pesanan sedang diproses
```

---

# Assignment 8 - Kombinasi Enum dan Utility Types (Hard)
Buat interface `Pesanan` yang memiliki properti bertipe enum `StatusPesanan`, lalu gunakan kombinasi `Partial` dan `Pick` untuk membuat tipe update pesanan yang hanya bisa mengubah status dan catatan.

```ts
enum StatusPesanan {
  Pending = "PENDING",
  Diproses = "DIPROSES",
  Selesai = "SELESAI",
}

interface Pesanan {
  id: number;
  status: StatusPesanan;
  catatan: string;
  total: number;
}

type UpdatePesanan = Partial<Pick<Pesanan, "status" | "catatan">>;

let update1: UpdatePesanan = { status: StatusPesanan.Selesai };

console.log(update1);
```

**Hasil yang diharapkan:**
```
{ status: 'SELESAI' }
```
