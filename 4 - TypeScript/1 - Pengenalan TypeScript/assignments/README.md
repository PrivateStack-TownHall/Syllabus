# Tujuan Pembelajaran
- Memahami apa itu TypeScript dan kelebihannya dibanding JavaScript
- Mampu menginstall dan menjalankan TypeScript compiler (tsc)
- Memahami konsep static typing
- Mampu mengonversi kode JavaScript sederhana menjadi TypeScript

---

# Assignment 1 - Instalasi TypeScript (Easy)
Install TypeScript secara global menggunakan npm, lalu cek versinya.

```bash
npm install -g typescript
tsc --version
```

**Hasil yang diharapkan:**
```
Version 5.x.x
```

---

# Assignment 2 - Hello World TypeScript (Easy)
Buat file `hello.ts` yang menampilkan teks ke console, lalu compile menjadi JavaScript.

```ts
let pesan: string = "Hello, TypeScript!";
console.log(pesan);
```

```bash
tsc hello.ts
node hello.js
```

**Hasil yang diharapkan:**
```
Hello, TypeScript!
```

---

# Assignment 3 - Static Typing Sederhana (Easy)
Buktikan static typing dengan mendeklarasikan variabel bertipe number, lalu coba isi dengan string.

```ts
let umur: number = 25;
umur = "dua puluh lima"; // coba jalankan baris ini
```

**Hasil yang diharapkan:**
```
error TS2322: Type 'string' is not assignable to type 'number'.
```

---

# Assignment 4 - Konversi JS ke TS (Easy)
Ubah kode JavaScript berikut menjadi TypeScript dengan menambahkan tipe data pada parameter dan return value.

```ts
// sebelumnya JavaScript: function tambah(a, b) { return a + b; }
function tambah(a: number, b: number): number {
  return a + b;
}

console.log(tambah(5, 10));
```

**Hasil yang diharapkan:**
```
15
```

---

# Assignment 5 - Konfigurasi tsconfig.json (Easy)
Generate file `tsconfig.json` menggunakan perintah tsc, lalu jelaskan fungsi dari opsi `strict`.

```bash
tsc --init
```

**Hasil yang diharapkan:**
```
message TS6071: Successfully created a tsconfig.json file.
```

---

# Assignment 6 - Compile Otomatis (Medium)
Jalankan TypeScript compiler dalam mode watch agar otomatis compile setiap ada perubahan file.

```bash
tsc --watch
```

**Hasil yang diharapkan:**
```
[HH:MM:SS] Starting compilation in watch mode...
Found 0 errors. Watching for file changes.
```

---

# Assignment 7 - Type Inference (Medium)
Buktikan bahwa TypeScript bisa menebak tipe data secara otomatis (type inference) tanpa anotasi eksplisit.

```ts
let kota = "Bekasi"; // TypeScript otomatis menganggap ini string
kota = 123; // coba jalankan baris ini
```

**Hasil yang diharapkan:**
```
error TS2322: Type 'number' is not assignable to type 'string'.
```

---

# Assignment 8 - any vs unknown (Hard)
Jelaskan perbedaan antara tipe `any` dan `unknown` dengan membuat contoh kode yang menunjukkan `unknown` lebih aman digunakan.

```ts
let dataAny: any = "teks";
dataAny.toUpperCase(); // aman, tapi tidak type-safe

let dataUnknown: unknown = "teks";
// dataUnknown.toUpperCase(); // error, harus dicek dulu
if (typeof dataUnknown === "string") {
  console.log(dataUnknown.toUpperCase());
}
```

**Hasil yang diharapkan:**
```
TEKS
```
