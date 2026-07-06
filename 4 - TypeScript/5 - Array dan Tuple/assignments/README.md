# Tujuan Pembelajaran
- Mampu mendeklarasikan array dengan tipe data spesifik
- Memahami readonly array
- Mampu menggunakan tuple untuk data terstruktur
- Memahami tuple dengan optional dan rest element

---

# Assignment 1 - Array bertipe Number (Easy)
Buat array bertipe number, lalu tambahkan elemen baru menggunakan push.

```ts
let angka: number[] = [1, 2, 3];
angka.push(4);

console.log(angka);
```

**Hasil yang diharapkan:**
```
[ 1, 2, 3, 4 ]
```

---

# Assignment 2 - Array bertipe String (Easy)
Buat array bertipe string berisi nama-nama buah.

```ts
let buah: string[] = ["Apel", "Jeruk", "Mangga"];

console.log(buah);
```

**Hasil yang diharapkan:**
```
[ 'Apel', 'Jeruk', 'Mangga' ]
```

---

# Assignment 3 - Array dengan Generic Array<T> (Easy)
Buat array bertipe number menggunakan sintaks `Array<number>`.

```ts
let nilai: Array<number> = [80, 90, 100];

console.log(nilai);
```

**Hasil yang diharapkan:**
```
[ 80, 90, 100 ]
```

---

# Assignment 4 - Tuple Sederhana (Easy)
Buat tuple untuk menyimpan data (nama: string, umur: number).

```ts
let siswa: [string, number] = ["Vincent", 25];

console.log(siswa);
```

**Hasil yang diharapkan:**
```
[ 'Vincent', 25 ]
```

---

# Assignment 5 - Readonly Array (Easy)
Buat array readonly agar tidak bisa diubah setelah dideklarasikan.

```ts
let warna: readonly string[] = ["merah", "hijau", "biru"];
// warna.push("kuning"); // akan error

console.log(warna);
```

**Hasil yang diharapkan:**
```
[ 'merah', 'hijau', 'biru' ]
```

---

# Assignment 6 - Tuple dengan Optional Element (Medium)
Buat tuple dengan elemen ketiga bersifat optional untuk menyimpan data (nama, umur, email?).

```ts
let siswa: [string, number, string?] = ["Vincent", 25];
let siswa2: [string, number, string?] = ["Budi", 22, "budi@email.com"];

console.log(siswa);
console.log(siswa2);
```

**Hasil yang diharapkan:**
```
[ 'Vincent', 25 ]
[ 'Budi', 22, 'budi@email.com' ]
```

---

# Assignment 7 - Array of Tuple (Medium)
Buat array yang berisi beberapa tuple (nama, nilai) untuk beberapa siswa.

```ts
let daftarNilai: [string, number][] = [
  ["Vincent", 90],
  ["Budi", 85],
];

console.log(daftarNilai);
```

**Hasil yang diharapkan:**
```
[ [ 'Vincent', 90 ], [ 'Budi', 85 ] ]
```

---

# Assignment 8 - Tuple dengan Rest Element (Hard)
Buat tuple yang memiliki elemen tetap di awal dan rest element bertipe number di akhir untuk menyimpan (nama, ...nilai-nilai ujian).

```ts
type HasilUjian = [string, ...number[]];

let hasil: HasilUjian = ["Vincent", 90, 85, 88];

console.log(hasil);
```

**Hasil yang diharapkan:**
```
[ 'Vincent', 90, 85, 88 ]
```
