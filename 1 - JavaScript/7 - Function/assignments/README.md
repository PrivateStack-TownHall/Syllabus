# Tujuan Pembelajaran
- Mampu membuat function declaration dan function expression
- Memahami arrow function
- Mampu menggunakan default parameter dan rest parameter
- Memahami konsep closure

---

# Assignment 1 - Function Declaration (Easy)
Buat function bernama `sapa` yang menerima parameter nama dan menampilkan salam.

```js
function sapa(nama) {
  console.log("Halo, " + nama + "!");
}

sapa("Vincent");
```

**Hasil yang diharapkan:**
```
Halo, Vincent!
```

---

# Assignment 2 - Parameter dan Argument (Easy)
Buat function dengan 2 parameter, lalu panggil function tersebut dengan argument yang sesuai. Jelaskan perbedaan keduanya dalam komentar.

```js
// parameter: nama1, nama2 (didefinisikan saat membuat function)
function tampilkanNama(nama1, nama2) {
  console.log(nama1, "&", nama2);
}

// argument: "Vincent", "Budi" (nilai yang dikirim saat memanggil function)
tampilkanNama("Vincent", "Budi");
```

**Hasil yang diharapkan:**
```
Vincent & Budi
```

---

# Assignment 3 - Function Penjumlahan (Easy)
Buat function untuk menjumlahkan dua angka dan mengembalikan hasilnya.

```js
function jumlahkan(a, b) {
  return a + b;
}

console.log(jumlahkan(5, 7));
```

**Hasil yang diharapkan:**
```
12
```

---

# Assignment 4 - Arrow Function (Easy)
Ubah function `jumlahkan` di atas menjadi bentuk arrow function.

```js
const jumlahkan = (a, b) => a + b;

console.log(jumlahkan(5, 7));
```

**Hasil yang diharapkan:**
```
12
```

---

# Assignment 5 - Default Parameter (Easy)
Buat function `sapa` dengan default parameter nama "Guest" jika tidak diisi.

```js
function sapa(nama = "Guest") {
  console.log("Halo, " + nama + "!");
}

sapa();
sapa("Vincent");
```

**Hasil yang diharapkan:**
```
Halo, Guest!
Halo, Vincent!
```

---

# Assignment 6 - Function Declaration vs Expression (Medium)
Buat satu contoh function declaration dan satu function expression, lalu jelaskan perbedaan keduanya dalam hal hoisting.

```js
// function declaration (bisa dipanggil sebelum dideklarasikan)
function declaration() {
  console.log("Ini function declaration");
}

// function expression (tidak bisa dipanggil sebelum dideklarasikan)
const expression = function () {
  console.log("Ini function expression");
};

declaration();
expression();
```

**Hasil yang diharapkan:**
```
Ini function declaration
Ini function expression
```

---

# Assignment 7 - Rest Parameter (Medium)
Buat function yang menerima jumlah argument tidak tetap menggunakan rest parameter, lalu jumlahkan semuanya.

```js
function jumlahkanSemua(...angka) {
  return angka.reduce((total, n) => total + n, 0);
}

console.log(jumlahkanSemua(1, 2, 3, 4, 5));
```

**Hasil yang diharapkan:**
```
15
```

---

# Assignment 8 - Closure Counter (Hard)
Buat function yang memanfaatkan closure untuk membuat counter yang nilainya tetap tersimpan antar pemanggilan.

```js
function buatCounter() {
  let count = 0;
  return function () {
    count++;
    return count;
  };
}

const counter = buatCounter();
console.log(counter());
console.log(counter());
console.log(counter());
```

**Hasil yang diharapkan:**
```
1
2
3
```
