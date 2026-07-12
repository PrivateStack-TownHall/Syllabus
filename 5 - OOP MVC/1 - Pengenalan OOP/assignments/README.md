# Tujuan Pembelajaran
- Memahami konsep dasar Object-Oriented Programming (OOP)
- Mampu membuat class dan object di JavaScript
- Memahami constructor dan property dalam class
- Mampu membuat dan memanggil method di dalam class

---

# Assignment 1 - Membuat Class Sederhana (Easy)
Buat class `Mobil` dengan properti `merk` dan `warna`, lalu buat satu object dari class tersebut dan tampilkan propertinya.

```js
class Mobil {
  constructor(merk, warna) {
    this.merk = merk;
    this.warna = warna;
  }
}

let mobil1 = new Mobil("Toyota", "Merah");
console.log(mobil1.merk, mobil1.warna);
```

**Hasil yang diharapkan:**
```
Toyota Merah
```

---

# Assignment 2 - Property dan Constructor (Easy)
Buat class `Siswa` dengan constructor yang menerima `nama` dan `umur`, lalu tampilkan object yang terbentuk.

```js
class Siswa {
  constructor(nama, umur) {
    this.nama = nama;
    this.umur = umur;
  }
}

let siswa1 = new Siswa("Vincent", 25);
console.log(siswa1);
```

**Hasil yang diharapkan:**
```
Siswa { nama: 'Vincent', umur: 25 }
```

---

# Assignment 3 - Method dalam Class (Easy)
Tambahkan method `sapa()` pada class `Siswa` yang menampilkan salam menggunakan nama siswa tersebut.

```js
class Siswa {
  constructor(nama) {
    this.nama = nama;
  }

  sapa() {
    console.log(`Halo, nama saya ${this.nama}`);
  }
}

let siswa1 = new Siswa("Vincent");
siswa1.sapa();
```

**Hasil yang diharapkan:**
```
Halo, nama saya Vincent
```

---

# Assignment 4 - Multiple Object dari Class yang Sama (Easy)
Buat dua object berbeda dari class `Produk` yang sama, lalu tampilkan keduanya.

```js
class Produk {
  constructor(nama, harga) {
    this.nama = nama;
    this.harga = harga;
  }
}

let produk1 = new Produk("Mouse", 150000);
let produk2 = new Produk("Keyboard", 300000);

console.log(produk1, produk2);
```

**Hasil yang diharapkan:**
```
Produk { nama: 'Mouse', harga: 150000 } Produk { nama: 'Keyboard', harga: 300000 }
```

---

# Assignment 5 - Default Value pada Constructor (Easy)
Buat class `Akun` dengan constructor yang memberi nilai default `saldo = 0` jika tidak diisi.

```js
class Akun {
  constructor(nama, saldo = 0) {
    this.nama = nama;
    this.saldo = saldo;
  }
}

let akun1 = new Akun("Vincent");
console.log(akun1.saldo);
```

**Hasil yang diharapkan:**
```
0
```

---

# Assignment 6 - Method dengan Parameter (Easy)
Buat class `Kalkulator` dengan method `tambah(a, b)` yang mengembalikan hasil penjumlahan dua angka.

```js
class Kalkulator {
  tambah(a, b) {
    return a + b;
  }
}

let kalkulator1 = new Kalkulator();
console.log(kalkulator1.tambah(5, 10));
```

**Hasil yang diharapkan:**
```
15
```

---

# Assignment 7 - this Keyword dalam Method (Medium)
Buat class `Akun` dengan method `tambahSaldo(jumlah)` yang mengubah properti saldo menggunakan `this`, lalu panggil method tersebut beberapa kali.

```js
class Akun {
  constructor() {
    this.saldo = 0;
  }

  tambahSaldo(jumlah) {
    this.saldo += jumlah;
  }
}

let akun1 = new Akun();
akun1.tambahSaldo(50000);
akun1.tambahSaldo(25000);
console.log(akun1.saldo);
```

**Hasil yang diharapkan:**
```
75000
```

---

# Assignment 8 - Static Method (Medium)
Buat class `MathHelper` dengan static method `kuadrat(n)` yang bisa dipanggil langsung tanpa membuat object.

```js
class MathHelper {
  static kuadrat(n) {
    return n * n;
  }
}

console.log(MathHelper.kuadrat(5));
```

**Hasil yang diharapkan:**
```
25
```

---

# Assignment 9 - Getter dan Setter (Medium)
Buat class `Produk` dengan getter dan setter untuk properti harga. Setter harus menolak nilai negatif.

```js
class Produk {
  constructor(nama, harga) {
    this.nama = nama;
    this._harga = harga;
  }

  get harga() {
    return this._harga;
  }

  set harga(nilai) {
    if (nilai < 0) {
      console.log("Harga tidak boleh negatif");
    } else {
      this._harga = nilai;
    }
  }
}

let produk1 = new Produk("Mouse", 100000);
produk1.harga = -5000;
console.log(produk1.harga);
```

**Hasil yang diharapkan:**
```
Harga tidak boleh negatif
100000
```

---

# Assignment 10 - Class dengan Banyak Method Saling Terkait (Hard)
Buat class `KeranjangBelanja` yang memiliki method untuk menambah barang, menghitung total belanja, dan menampilkan daftar barang.

```js
class KeranjangBelanja {
  constructor() {
    this.barang = [];
  }

  tambahBarang(nama, harga, jumlah) {
    this.barang.push({ nama, harga, jumlah });
  }

  hitungTotal() {
    return this.barang.reduce((total, b) => total + b.harga * b.jumlah, 0);
  }

  tampilkanDaftar() {
    this.barang.forEach((b) =>
      console.log(`${b.nama} x${b.jumlah} = ${b.harga * b.jumlah}`)
    );
  }
}

let keranjang1 = new KeranjangBelanja();
keranjang1.tambahBarang("Kopi", 20000, 2);
keranjang1.tambahBarang("Roti", 15000, 3);
keranjang1.tampilkanDaftar();
console.log("Total:", keranjang1.hitungTotal());
```

**Hasil yang diharapkan:**
```
Kopi x2 = 40000
Roti x3 = 45000
Total: 85000
```
