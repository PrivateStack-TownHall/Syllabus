# Tujuan Pembelajaran
- Mampu menambahkan type annotation pada parameter dan return value function
- Memahami optional parameter dan default parameter
- Mampu menggunakan function overload
- Memahami tipe function sebagai variabel (function type)

---

# Assignment 1 - Function dengan Tipe Parameter (Easy)
Buat function untuk menjumlahkan dua angka dengan tipe parameter dan return value number.

```ts
function jumlahkan(a: number, b: number): number {
  return a + b;
}

console.log(jumlahkan(5, 7));
```

**Hasil yang diharapkan:**
```
12
```

---

# Assignment 2 - Optional Parameter (Easy)
Buat function `sapa` dengan parameter kedua bersifat optional.

```ts
function sapa(nama: string, sapaan?: string): string {
  return `${sapaan ?? "Halo"}, ${nama}!`;
}

console.log(sapa("Vincent"));
console.log(sapa("Vincent", "Selamat pagi"));
```

**Hasil yang diharapkan:**
```
Halo, Vincent!
Selamat pagi, Vincent!
```

---

# Assignment 3 - Default Parameter (Easy)
Buat function dengan default parameter bertipe number.

```ts
function hitungDiskon(harga: number, persen: number = 10): number {
  return harga - (harga * persen) / 100;
}

console.log(hitungDiskon(100000));
console.log(hitungDiskon(100000, 20));
```

**Hasil yang diharapkan:**
```
90000
80000
```

---

# Assignment 4 - Arrow Function dengan Tipe (Easy)
Ubah function biasa menjadi arrow function dengan type annotation.

```ts
const kali = (a: number, b: number): number => a * b;

console.log(kali(4, 5));
```

**Hasil yang diharapkan:**
```
20
```

---

# Assignment 5 - Function Type sebagai Variabel (Easy)
Buat tipe function menggunakan type alias, lalu gunakan pada sebuah variabel function.

```ts
type OperasiMatematika = (a: number, b: number) => number;

const kurang: OperasiMatematika = (a, b) => a - b;

console.log(kurang(10, 4));
```

**Hasil yang diharapkan:**
```
6
```

---

# Assignment 6 - Rest Parameter dengan Tipe (Medium)
Buat function yang menerima jumlah argument tidak tetap bertipe number menggunakan rest parameter.

```ts
function jumlahkanSemua(...angka: number[]): number {
  return angka.reduce((total, n) => total + n, 0);
}

console.log(jumlahkanSemua(1, 2, 3, 4, 5));
```

**Hasil yang diharapkan:**
```
15
```

---

# Assignment 7 - Void vs Never (Medium)
Buat satu function bertipe `void` dan satu function bertipe `never`, lalu jelaskan perbedaannya.

```ts
function logPesan(pesan: string): void {
  console.log(pesan);
}

function lemparError(pesan: string): never {
  throw new Error(pesan);
}

logPesan("Ini function void");
```

**Hasil yang diharapkan:**
```
Ini function void
```

---

# Assignment 8 - Function Overload (Hard)
Buat function overload untuk `gabungkan` yang bisa menerima dua number (dijumlahkan) atau dua string (digabung).

```ts
function gabungkan(a: number, b: number): number;
function gabungkan(a: string, b: string): string;
function gabungkan(a: any, b: any): any {
  return a + b;
}

console.log(gabungkan(5, 10));
console.log(gabungkan("Halo, ", "Vincent!"));
```

**Hasil yang diharapkan:**
```
15
Halo, Vincent!
```
