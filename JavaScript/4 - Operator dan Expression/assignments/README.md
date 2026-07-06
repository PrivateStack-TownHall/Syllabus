# Tujuan Pembelajaran
- Memahami macam-macam operator di JavaScript (aritmatika, perbandingan, logika)
- Mampu menggunakan operator ternary
- Memahami operator precedence
- Mampu membuat expression kompleks

---

# Assignment 1 - Operator Aritmatika (Easy)
Buat operasi tambah, kurang, kali, bagi, dan modulus dari dua angka.

```js
let a = 10, b = 3;

console.log(a + b, a - b, a * b, a / b, a % b);
```

**Hasil yang diharapkan:**
```
13 7 30 3.3333333333333335 1
```

---

# Assignment 2 - Modulus (Easy)
Hitung hasil dari `10 % 3` dan jelaskan kegunaannya.

```js
console.log(10 % 3);
```

**Hasil yang diharapkan:**
```
1
```

---

# Assignment 3 - Increment Prefix vs Postfix (Easy)
Buktikan perbedaan `++x` dan `x++` menggunakan console.log.

```js
let x = 5;
console.log(x++); // postfix
console.log(x);

let y = 5;
console.log(++y); // prefix
console.log(y);
```

**Hasil yang diharapkan:**
```
5
6
6
6
```

---

# Assignment 4 - Operator Logika (Easy)
Buat contoh penggunaan `&&` dan `||` untuk mengecek dua kondisi sekaligus.

```js
let umur = 20;
let punyaKTP = true;

console.log(umur >= 17 && punyaKTP);
console.log(umur < 17 || punyaKTP);
```

**Hasil yang diharapkan:**
```
true
true
```

---

# Assignment 5 - Operator Ternary (Easy)
Gunakan operator ternary untuk mengecek apakah sebuah angka positif atau negatif.

```js
let angka = -5;
let hasil = angka >= 0 ? "Positif" : "Negatif";

console.log(hasil);
```

**Hasil yang diharapkan:**
```
Negatif
```

---

# Assignment 6 - == vs === (Medium)
Bandingkan hasil `5 == "5"` dan `5 === "5"`, lalu jelaskan kenapa hasilnya berbeda.

```js
console.log(5 == "5");
console.log(5 === "5");
```

**Hasil yang diharapkan:**
```
true
false
```

---

# Assignment 7 - Ternary untuk Cek Dewasa (Medium)
Buat expression ternary untuk menentukan apakah seseorang sudah dewasa (umur >= 18) atau belum.

```js
let umur = 17;
let status = umur >= 18 ? "Dewasa" : "Belum Dewasa";

console.log(status);
```

**Hasil yang diharapkan:**
```
Belum Dewasa
```

---

# Assignment 8 - Operator Precedence (Hard)
Tentukan hasil dari expression berikut tanpa menjalankannya terlebih dahulu, lalu buktikan dengan console.log: `3 + 4 * 2 > 10 && 5 < 6 || false`.

```js
console.log(3 + 4 * 2 > 10 && 5 < 6 || false);
```

**Hasil yang diharapkan:**
```
false
```
