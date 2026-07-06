# Tujuan Pembelajaran
- Mampu mendeklarasikan variabel dengan type annotation
- Memahami perbedaan type annotation dan type inference
- Mampu menggunakan const assertion
- Memahami literal type

---

# Assignment 1 - Type Annotation Dasar (Easy)
Deklarasikan variabel `nama`, `umur`, dan `isMember` dengan type annotation eksplisit.

```ts
let nama: string = "Vincent";
let umur: number = 25;
let isMember: boolean = true;

console.log(nama, umur, isMember);
```

**Hasil yang diharapkan:**
```
Vincent 25 true
```

---

# Assignment 2 - Type Inference (Easy)
Deklarasikan variabel tanpa type annotation, lalu buktikan TypeScript tetap bisa mendeteksi tipenya secara otomatis.

```ts
let kota = "Bekasi"; // inferred sebagai string
console.log(typeof kota);
```

**Hasil yang diharapkan:**
```
string
```

---

# Assignment 3 - Multiple Variable dengan Tipe Berbeda (Easy)
Deklarasikan beberapa variabel dengan tipe berbeda dalam satu blok kode.

```ts
let a: number = 10;
let b: string = "sepuluh";
let c: boolean = false;

console.log(a, b, c);
```

**Hasil yang diharapkan:**
```
10 sepuluh false
```

---

# Assignment 4 - Literal Type (Easy)
Buat variabel dengan literal type yang hanya bisa diisi nilai tertentu, misalnya "small" | "medium" | "large".

```ts
let ukuran: "small" | "medium" | "large";
ukuran = "medium";
console.log(ukuran);

ukuran = "extra-large"; // coba jalankan baris ini
```

**Hasil yang diharapkan:**
```
medium
error TS2322: Type '"extra-large"' is not assignable to type '"small" | "medium" | "large"'.
```

---

# Assignment 5 - Deklarasi Tanpa Nilai Awal (Easy)
Deklarasikan variabel dengan type annotation tanpa nilai awal, lalu isi nilainya kemudian.

```ts
let skor: number;
skor = 90;

console.log(skor);
```

**Hasil yang diharapkan:**
```
90
```

---

# Assignment 6 - const Assertion (Medium)
Gunakan `as const` untuk membuat array menjadi readonly tuple dengan literal type.

```ts
const warna = ["merah", "hijau", "biru"] as const;
// warna.push("kuning"); // akan error karena readonly

console.log(warna);
```

**Hasil yang diharapkan:**
```
[ 'merah', 'hijau', 'biru' ]
```

---

# Assignment 7 - Type Annotation pada Object (Medium)
Deklarasikan variabel object dengan type annotation manual (tanpa interface/type alias).

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

# Assignment 8 - Kombinasi Literal Type dan Union (Hard)
Buat function yang menerima parameter bertipe literal union untuk status pesanan ("pending" | "diproses" | "selesai"), lalu tampilkan pesan berbeda untuk tiap status.

```ts
function cekStatus(status: "pending" | "diproses" | "selesai"): string {
  switch (status) {
    case "pending":
      return "Pesanan menunggu diproses";
    case "diproses":
      return "Pesanan sedang diproses";
    case "selesai":
      return "Pesanan sudah selesai";
  }
}

console.log(cekStatus("diproses"));
```

**Hasil yang diharapkan:**
```
Pesanan sedang diproses
```
