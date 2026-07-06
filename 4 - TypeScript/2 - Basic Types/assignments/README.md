# Tujuan Pembelajaran
- Memahami tipe data dasar di TypeScript (string, number, boolean, null, undefined)
- Mampu menggunakan tipe array dan tuple sederhana
- Memahami tipe any, unknown, dan void
- Mampu menggunakan union type dasar

---

# Assignment 1 - Tipe String, Number, Boolean (Easy)
Buat variabel dengan tipe string, number, dan boolean.

```ts
let nama: string = "Vincent";
let umur: number = 25;
let isAktif: boolean = true;

console.log(nama, umur, isAktif);
```

**Hasil yang diharapkan:**
```
Vincent 25 true
```

---

# Assignment 2 - Tipe Array (Easy)
Buat array bertipe number dan array bertipe string.

```ts
let angka: number[] = [1, 2, 3];
let nama: string[] = ["Ani", "Budi"];

console.log(angka, nama);
```

**Hasil yang diharapkan:**
```
[ 1, 2, 3 ] [ 'Ani', 'Budi' ]
```

---

# Assignment 3 - void pada Function (Easy)
Buat function yang tidak mengembalikan nilai apapun menggunakan tipe `void`.

```ts
function tampilkanPesan(pesan: string): void {
  console.log(pesan);
}

tampilkanPesan("Selamat belajar TypeScript!");
```

**Hasil yang diharapkan:**
```
Selamat belajar TypeScript!
```

---

# Assignment 4 - null dan undefined (Easy)
Buat variabel dengan tipe `null` dan `undefined` secara eksplisit.

```ts
let kosong: null = null;
let belumDiisi: undefined = undefined;

console.log(kosong, belumDiisi);
```

**Hasil yang diharapkan:**
```
null undefined
```

---

# Assignment 5 - Union Type Dasar (Easy)
Buat variabel yang bisa menerima tipe `string` atau `number` menggunakan union type.

```ts
let id: string | number;
id = 101;
console.log(id);

id = "A101";
console.log(id);
```

**Hasil yang diharapkan:**
```
101
A101
```

---

# Assignment 6 - any vs unknown (Medium)
Buat contoh kode yang membedakan penggunaan `any` dan `unknown` saat menerima data dari luar (misalnya hasil JSON.parse).

```ts
let dataAny: any = JSON.parse('{"nama":"Vincent"}');
console.log(dataAny.nama);

let dataUnknown: unknown = JSON.parse('{"nama":"Vincent"}');
if (typeof dataUnknown === "object" && dataUnknown !== null && "nama" in dataUnknown) {
  console.log((dataUnknown as { nama: string }).nama);
}
```

**Hasil yang diharapkan:**
```
Vincent
Vincent
```

---

# Assignment 7 - Tuple (Medium)
Buat tuple untuk menyimpan data koordinat (x, y) dengan tipe number.

```ts
let koordinat: [number, number] = [10, 20];

console.log(koordinat);
```

**Hasil yang diharapkan:**
```
[ 10, 20 ]
```

---

# Assignment 8 - Union Type Kompleks (Hard)
Buat function yang menerima parameter bertipe union (`string | number`) dan menampilkan tipe data yang diterima menggunakan type narrowing.

```ts
function cekTipe(value: string | number): void {
  if (typeof value === "string") {
    console.log(`Ini string: ${value.toUpperCase()}`);
  } else {
    console.log(`Ini number: ${value.toFixed(2)}`);
  }
}

cekTipe("hello");
cekTipe(3.14159);
```

**Hasil yang diharapkan:**
```
Ini string: HELLO
Ini number: 3.14
```
