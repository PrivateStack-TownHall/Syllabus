# Tujuan Pembelajaran
- Mampu membuat dan mengakses elemen array
- Memahami method dasar array (push, pop, shift, unshift)
- Mampu memanipulasi array menggunakan looping
- Mampu menghilangkan duplikat dalam array secara manual

---

# Assignment 1 - Membuat Array (Easy)
Buat array kosong dan array berisi 5 buah angka.

```js
let arrKosong = [];
let arrAngka = [10, 20, 30, 40, 50];

console.log(arrKosong, arrAngka);
```

**Hasil yang diharapkan:**
```
[] [ 10, 20, 30, 40, 50 ]
```

---

# Assignment 2 - Akses Elemen Array (Easy)
Akses elemen pertama dan elemen terakhir dari sebuah array.

```js
let buah = ["Apel", "Jeruk", "Mangga", "Anggur"];

console.log(buah[0]);
console.log(buah[buah.length - 1]);
```

**Hasil yang diharapkan:**
```
Apel
Anggur
```

---

# Assignment 3 - Push dan Pop (Easy)
Tambahkan elemen baru ke akhir array menggunakan `push()`, lalu hapus elemen terakhir menggunakan `pop()`.

```js
let angka = [1, 2, 3];
angka.push(4);
console.log(angka);

angka.pop();
console.log(angka);
```

**Hasil yang diharapkan:**
```
[ 1, 2, 3, 4 ]
[ 1, 2, 3 ]
```

---

# Assignment 4 - Panjang Array (Easy)
Tampilkan panjang (length) dari sebuah array.

```js
let hewan = ["Kucing", "Anjing", "Burung"];

console.log(hewan.length);
```

**Hasil yang diharapkan:**
```
3
```

---

# Assignment 5 - Shift dan Unshift (Easy)
Tambahkan elemen di awal array menggunakan `unshift()`, lalu hapus elemen pertama menggunakan `shift()`.

```js
let angka = [2, 3, 4];
angka.unshift(1);
console.log(angka);

angka.shift();
console.log(angka);
```

**Hasil yang diharapkan:**
```
[ 1, 2, 3, 4 ]
[ 2, 3, 4 ]
```

---

# Assignment 6 - Membalik Array Manual (Medium)
Balik urutan elemen array tanpa menggunakan method `reverse()`.

```js
let arr = [1, 2, 3, 4, 5];
let hasil = [];

for (let i = arr.length - 1; i >= 0; i--) {
  hasil.push(arr[i]);
}

console.log(hasil);
```

**Hasil yang diharapkan:**
```
[ 5, 4, 3, 2, 1 ]
```

---

# Assignment 7 - Nilai Terbesar dan Terkecil (Medium)
Cari nilai terbesar dan terkecil dalam sebuah array menggunakan looping (tanpa Math.max/Math.min).

```js
let angka = [12, 45, 3, 67, 21];
let terbesar = angka[0];
let terkecil = angka[0];

for (let i = 1; i < angka.length; i++) {
  if (angka[i] > terbesar) terbesar = angka[i];
  if (angka[i] < terkecil) terkecil = angka[i];
}

console.log("Terbesar:", terbesar, "Terkecil:", terkecil);
```

**Hasil yang diharapkan:**
```
Terbesar: 67 Terkecil: 3
```

---

# Assignment 8 - Hapus Duplikat Manual (Hard)
Hapus elemen duplikat dalam sebuah array tanpa menggunakan `Set`, hanya menggunakan looping dan array biasa.

```js
let angka = [1, 2, 2, 3, 4, 4, 5];
let hasil = [];

for (let i = 0; i < angka.length; i++) {
  if (!hasil.includes(angka[i])) {
    hasil.push(angka[i]);
  }
}

console.log(hasil);
```

**Hasil yang diharapkan:**
```
[ 1, 2, 3, 4, 5 ]
```
