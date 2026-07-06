# Tujuan Pembelajaran
- Mampu menggunakan for, while, dan do-while
- Memahami penggunaan break dan continue
- Mampu membuat nested loop
- Mampu menyusun pola menggunakan loop

---

# Assignment 1 - Cetak Angka 1-10 (Easy)
Cetak angka 1 sampai 10 menggunakan loop `for`.

```js
for (let i = 1; i <= 10; i++) {
  console.log(i);
}
```

**Hasil yang diharapkan:**
```
1
2
3
...
10
```

---

# Assignment 2 - While vs Do-While (Easy)
Buat contoh loop `while` dan `do-while` yang mencetak angka 1 sampai 5.

```js
let i = 1;
while (i <= 5) {
  console.log(i);
  i++;
}

let j = 1;
do {
  console.log(j);
  j++;
} while (j <= 5);
```

**Hasil yang diharapkan:**
```
1
2
3
4
5
```

---

# Assignment 3 - Break Loop (Easy)
Hentikan loop ketika menemukan angka 5 menggunakan `break`.

```js
for (let i = 1; i <= 10; i++) {
  if (i === 5) break;
  console.log(i);
}
```

**Hasil yang diharapkan:**
```
1
2
3
4
```

---

# Assignment 4 - Continue Loop (Easy)
Lewati angka kelipatan 3 menggunakan `continue`.

```js
for (let i = 1; i <= 10; i++) {
  if (i % 3 === 0) continue;
  console.log(i);
}
```

**Hasil yang diharapkan:**
```
1
2
4
5
7
8
10
```

---

# Assignment 5 - Angka Genap 1-20 (Easy)
Cetak semua angka genap dari 1 sampai 20.

```js
for (let i = 1; i <= 20; i++) {
  if (i % 2 === 0) console.log(i);
}
```

**Hasil yang diharapkan:**
```
2
4
6
...
20
```

---

# Assignment 6 - Pola Segitiga Bintang (Medium)
Cetak pola segitiga bintang (*) sebanyak 5 baris menggunakan nested loop.

```js
for (let i = 1; i <= 5; i++) {
  let baris = "";
  for (let j = 1; j <= i; j++) {
    baris += "*";
  }
  console.log(baris);
}
```

**Hasil yang diharapkan:**
```
*
**
***
****
*****
```

---

# Assignment 7 - Total Kelipatan 3 (Medium)
Hitung total penjumlahan semua angka kelipatan 3 antara 1 sampai 100.

```js
let total = 0;
for (let i = 1; i <= 100; i++) {
  if (i % 3 === 0) total += i;
}

console.log(total);
```

**Hasil yang diharapkan:**
```
1683
```

---

# Assignment 8 - Piramida Angka (Hard)
Cetak pola piramida angka sampai baris ke-5 menggunakan nested loop.

```js
for (let i = 1; i <= 5; i++) {
  let baris = "";
  for (let j = 1; j <= i; j++) {
    baris += j + " ";
  }
  console.log(baris.trim());
}
```

**Hasil yang diharapkan:**
```
1
1 2
1 2 3
1 2 3 4
1 2 3 4 5
```
