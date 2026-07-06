# Tujuan Pembelajaran
- Mampu menggabungkan konsep type, interface, class, dan generic dalam satu program
- Mampu membangun program CRUD sederhana dengan type-safety
- Mampu menerapkan enum dan utility types dalam kasus nyata
- Mampu membangun mini project akhir yang mengintegrasikan seluruh materi TypeScript

---

# Assignment 1 - Konversi Suhu dengan Tipe (Easy)
Buat function konversi suhu Celsius ke Fahrenheit dengan type annotation lengkap.

```ts
function celciusKeFahrenheit(celcius: number): number {
  return (celcius * 9) / 5 + 32;
}

console.log(celciusKeFahrenheit(30));
```

**Hasil yang diharapkan:**
```
86
```

---

# Assignment 2 - Interface Produk (Easy)
Buat interface `Produk`, lalu buat array of Produk beserta function untuk menampilkan semuanya.

```ts
interface Produk {
  nama: string;
  harga: number;
}

let produkList: Produk[] = [
  { nama: "Mouse", harga: 150000 },
  { nama: "Keyboard", harga: 300000 },
];

function tampilkanProduk(produk: Produk[]): void {
  produk.forEach((p) => console.log(`${p.nama}: Rp${p.harga}`));
}

tampilkanProduk(produkList);
```

**Hasil yang diharapkan:**
```
Mouse: Rp150000
Keyboard: Rp300000
```

---

# Assignment 3 - Enum Status Pesanan (Easy)
Gunakan enum `StatusPesanan` pada sebuah interface `Pesanan`, lalu tampilkan datanya.

```ts
enum StatusPesanan {
  Pending = "PENDING",
  Selesai = "SELESAI",
}

interface Pesanan {
  id: number;
  status: StatusPesanan;
}

let pesanan1: Pesanan = { id: 1, status: StatusPesanan.Pending };

console.log(pesanan1);
```

**Hasil yang diharapkan:**
```
{ id: 1, status: 'PENDING' }
```

---

# Assignment 4 - Function Generic untuk Filter (Easy)
Buat function generic untuk memfilter array berdasarkan kondisi tertentu.

```ts
function filterData<T>(data: T[], kondisi: (item: T) => boolean): T[] {
  return data.filter(kondisi);
}

let angka = [1, 2, 3, 4, 5, 6];
let genap = filterData(angka, (n) => n % 2 === 0);

console.log(genap);
```

**Hasil yang diharapkan:**
```
[ 2, 4, 6 ]
```

---

# Assignment 5 - Class Produk dengan Method (Easy)
Buat class `Produk` dengan constructor dan method untuk menghitung harga setelah diskon.

```ts
class Produk {
  constructor(public nama: string, public harga: number) {}

  hargaSetelahDiskon(persen: number): number {
    return this.harga - (this.harga * persen) / 100;
  }
}

let produk1 = new Produk("Laptop", 10000000);
console.log(produk1.hargaSetelahDiskon(10));
```

**Hasil yang diharapkan:**
```
9000000
```

---

# Assignment 6 - CRUD Data Buku dengan Interface (Medium)
Buat program manajemen data buku (tambah, edit, hapus) menggunakan interface dan array of objects yang type-safe.

```ts
interface Buku {
  judul: string;
  penulis: string;
  tahun: number;
}

let bukuList: Buku[] = [];

function tambahBuku(buku: Buku): void {
  bukuList.push(buku);
}

function editBuku(judul: string, dataBaru: Partial<Buku>): void {
  let buku = bukuList.find((b) => b.judul === judul);
  if (buku) Object.assign(buku, dataBaru);
}

tambahBuku({ judul: "Laskar Pelangi", penulis: "Andrea Hirata", tahun: 2005 });
editBuku("Laskar Pelangi", { tahun: 2006 });

console.log(bukuList);
```

**Hasil yang diharapkan:**
```
[ { judul: 'Laskar Pelangi', penulis: 'Andrea Hirata', tahun: 2006 } ]
```

---

# Assignment 7 - Generic Repository Sederhana (Medium)
Buat class generic `Repository<T>` yang bisa menyimpan, mencari, dan menghapus data apapun.

```ts
class Repository<T> {
  private data: T[] = [];

  tambah(item: T): void {
    this.data.push(item);
  }

  semua(): T[] {
    return this.data;
  }

  hapus(predicate: (item: T) => boolean): void {
    this.data = this.data.filter((item) => !predicate(item));
  }
}

interface Siswa {
  nama: string;
}

let repoSiswa = new Repository<Siswa>();
repoSiswa.tambah({ nama: "Vincent" });
repoSiswa.tambah({ nama: "Budi" });
repoSiswa.hapus((s) => s.nama === "Budi");

console.log(repoSiswa.semua());
```

**Hasil yang diharapkan:**
```
[ { nama: 'Vincent' } ]
```

---

# Assignment 8 - Mini Project Kasir Type-Safe (Hard)
Buat mini project kalkulator kasir menggunakan interface, enum, dan class agar seluruh alur transaksi type-safe: menerima barang, menghitung total, menerapkan diskon, dan mencetak struk.

```ts
interface Barang {
  nama: string;
  harga: number;
  jumlah: number;
}

enum TipeDiskon {
  Tidak = 0,
  Sepuluh = 10,
  DuaPuluh = 20,
}

class Kasir {
  private keranjang: Barang[] = [];

  tambahBarang(barang: Barang): void {
    this.keranjang.push(barang);
  }

  hitungTotal(diskon: TipeDiskon = TipeDiskon.Tidak): number {
    let total = this.keranjang.reduce(
      (acc, item) => acc + item.harga * item.jumlah,
      0
    );
    return total - (total * diskon) / 100;
  }

  cetakStruk(diskon: TipeDiskon = TipeDiskon.Tidak): void {
    console.log("=== STRUK BELANJA ===");
    this.keranjang.forEach((item) =>
      console.log(`${item.nama} x${item.jumlah} = ${item.harga * item.jumlah}`)
    );
    console.log("Total Akhir:", this.hitungTotal(diskon));
  }
}

let kasir1 = new Kasir();
kasir1.tambahBarang({ nama: "Kopi", harga: 20000, jumlah: 2 });
kasir1.tambahBarang({ nama: "Roti", harga: 15000, jumlah: 3 });
kasir1.cetakStruk(TipeDiskon.Sepuluh);
```

**Hasil yang diharapkan:**
```
=== STRUK BELANJA ===
Kopi x2 = 40000
Roti x3 = 45000
Total Akhir: 76500
```
