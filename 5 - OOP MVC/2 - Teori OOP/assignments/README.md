# Tujuan Pembelajaran
- Memahami 4 pilar utama OOP: enkapsulasi, inheritance, polimorfisme, dan abstraksi
- Mampu menerapkan enkapsulasi menggunakan private field (`#`)
- Mampu membuat inheritance antar class menggunakan `extends` dan `super`
- Mampu menerapkan polimorfisme melalui method overriding

---

# Assignment 1 - Enkapsulasi dengan Private Field (Easy)
Buat class `Akun` dengan properti saldo bersifat private (`#saldo`), lalu buat method untuk menambah dan membaca nilainya.

```js
class Akun {
  #saldo = 0;

  tambahSaldo(jumlah) {
    this.#saldo += jumlah;
  }

  cekSaldo() {
    return this.#saldo;
  }
}

let akun1 = new Akun();
akun1.tambahSaldo(50000);
console.log(akun1.cekSaldo());
```

**Hasil yang diharapkan:**
```
50000
```

---

# Assignment 2 - Inheritance Sederhana (Easy)
Buat class `Hewan` dengan method `bersuara()`, lalu buat class `Kucing` yang extends dari `Hewan` tanpa mengubah apapun.

```js
class Hewan {
  bersuara() {
    console.log("Hewan mengeluarkan suara");
  }
}

class Kucing extends Hewan {}

let kucing1 = new Kucing();
kucing1.bersuara();
```

**Hasil yang diharapkan:**
```
Hewan mengeluarkan suara
```

---

# Assignment 3 - Constructor dengan super() (Easy)
Buat class `Karyawan` yang extends dari class `Manusia`, gunakan `super()` di dalam constructor-nya untuk memanggil constructor parent.

```js
class Manusia {
  constructor(nama) {
    this.nama = nama;
  }
}

class Karyawan extends Manusia {
  constructor(nama, jabatan) {
    super(nama);
    this.jabatan = jabatan;
  }
}

let karyawan1 = new Karyawan("Vincent", "Developer");
console.log(karyawan1);
```

**Hasil yang diharapkan:**
```
Karyawan { nama: 'Vincent', jabatan: 'Developer' }
```

---

# Assignment 4 - Method Overriding (Easy)
Buat class `Kucing` yang extends `Hewan` dan meng-override method `bersuara()` dengan suara yang berbeda.

```js
class Hewan {
  bersuara() {
    console.log("Hewan mengeluarkan suara");
  }
}

class Kucing extends Hewan {
  bersuara() {
    console.log("Meong!");
  }
}

let kucing1 = new Kucing();
kucing1.bersuara();
```

**Hasil yang diharapkan:**
```
Meong!
```

---

# Assignment 5 - Abstraksi Sederhana dengan Method Umum (Easy)
Buat class `Kendaraan` yang menyembunyikan detail teknis internal di dalam method privat, sehingga pengguna hanya perlu memanggil satu method publik tanpa tahu detailnya.

```js
class Kendaraan {
  nyalakan() {
    this._prosesInternal();
    console.log("Kendaraan menyala");
  }

  _prosesInternal() {
    // detail teknis disembunyikan dari pengguna
  }
}

let mobil1 = new Kendaraan();
mobil1.nyalakan();
```

**Hasil yang diharapkan:**
```
Kendaraan menyala
```

---

# Assignment 6 - Getter/Setter untuk Enkapsulasi (Easy)
Buat class `Suhu` dengan private field derajat Celsius, sediakan getter untuk mengonversinya ke Fahrenheit.

```js
class Suhu {
  #celsius;

  constructor(celsius) {
    this.#celsius = celsius;
  }

  get fahrenheit() {
    return (this.#celsius * 9) / 5 + 32;
  }
}

let suhu1 = new Suhu(30);
console.log(suhu1.fahrenheit);
```

**Hasil yang diharapkan:**
```
86
```

---

# Assignment 7 - Inheritance Bertingkat (Medium)
Buat 3 tingkat inheritance: `Hewan` → `Mamalia` → `Kucing`, lalu buktikan `Kucing` bisa mengakses method dari seluruh parent-nya.

```js
class Hewan {
  bernafas() {
    console.log("Bernafas");
  }
}

class Mamalia extends Hewan {
  menyusui() {
    console.log("Menyusui anaknya");
  }
}

class Kucing extends Mamalia {
  bersuara() {
    console.log("Meong!");
  }
}

let kucing1 = new Kucing();
kucing1.bernafas();
kucing1.menyusui();
kucing1.bersuara();
```

**Hasil yang diharapkan:**
```
Bernafas
Menyusui anaknya
Meong!
```

---

# Assignment 8 - Polimorfisme dengan Banyak Class (Medium)
Buat beberapa class turunan dari `Bentuk` yang masing-masing meng-override method `luas()`, lalu panggil method yang sama untuk tiap object dalam sebuah array (polimorfisme).

```js
class Bentuk {
  luas() {
    return 0;
  }
}

class Lingkaran extends Bentuk {
  constructor(jariJari) {
    super();
    this.jariJari = jariJari;
  }

  luas() {
    return Math.PI * this.jariJari * this.jariJari;
  }
}

class Persegi extends Bentuk {
  constructor(sisi) {
    super();
    this.sisi = sisi;
  }

  luas() {
    return this.sisi * this.sisi;
  }
}

let bentukList = [new Lingkaran(7), new Persegi(5)];
bentukList.forEach((b) => console.log(b.luas().toFixed(2)));
```

**Hasil yang diharapkan:**
```
153.94
25.00
```

---

# Assignment 9 - Enkapsulasi dengan Validasi (Medium)
Buat class `Akun` dengan private field saldo, dan method `tarikSaldo(jumlah)` yang menolak penarikan jika saldo tidak mencukupi.

```js
class Akun {
  #saldo = 100000;

  tarikSaldo(jumlah) {
    if (jumlah > this.#saldo) {
      console.log("Saldo tidak cukup");
    } else {
      this.#saldo -= jumlah;
      console.log("Penarikan berhasil, sisa saldo:", this.#saldo);
    }
  }
}

let akun1 = new Akun();
akun1.tarikSaldo(150000);
akun1.tarikSaldo(50000);
```

**Hasil yang diharapkan:**
```
Saldo tidak cukup
Penarikan berhasil, sisa saldo: 50000
```

---

# Assignment 10 - Kombinasi 4 Pilar OOP (Hard)
Buat sistem kepegawaian sederhana: class `Karyawan` (enkapsulasi dengan private gaji), class `Manager` yang extends `Karyawan` (inheritance) dan meng-override method `hitungBonus()` (polimorfisme), dengan detail perhitungan bonus disembunyikan di dalam method (abstraksi).

```js
class Karyawan {
  #gaji;

  constructor(nama, gaji) {
    this.nama = nama;
    this.#gaji = gaji;
  }

  getGaji() {
    return this.#gaji;
  }

  hitungBonus() {
    return this.#gaji * 0.05;
  }
}

class Manager extends Karyawan {
  hitungBonus() {
    return this.getGaji() * 0.15;
  }
}

let karyawan1 = new Karyawan("Budi", 5000000);
let manager1 = new Manager("Vincent", 10000000);

console.log(karyawan1.hitungBonus());
console.log(manager1.hitungBonus());
```

**Hasil yang diharapkan:**
```
250000
1500000
```
