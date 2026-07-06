# Tujuan Pembelajaran
- Memahami konsep class, constructor, dan property
- Mampu menggunakan access modifier (public, private, protected)
- Memahami inheritance (extends) dan konsep OOP dasar lainnya
- Mampu menggunakan abstract class dan implements interface

---

# Assignment 1 - Class Sederhana (Easy)
Buat class `Siswa` dengan properti nama dan umur, beserta constructor-nya.

```ts
class Siswa {
  nama: string;
  umur: number;

  constructor(nama: string, umur: number) {
    this.nama = nama;
    this.umur = umur;
  }
}

let siswa1 = new Siswa("Vincent", 25);
console.log(siswa1.nama, siswa1.umur);
```

**Hasil yang diharapkan:**
```
Vincent 25
```

---

# Assignment 2 - Method pada Class (Easy)
Tambahkan method `sapa()` pada class `Siswa` yang menampilkan salam.

```ts
class Siswa {
  constructor(public nama: string, public umur: number) {}

  sapa(): void {
    console.log(`Halo, nama saya ${this.nama}`);
  }
}

let siswa1 = new Siswa("Vincent", 25);
siswa1.sapa();
```

**Hasil yang diharapkan:**
```
Halo, nama saya Vincent
```

---

# Assignment 3 - Access Modifier private (Easy)
Buat class `Akun` dengan properti `saldo` bersifat private.

```ts
class Akun {
  private saldo: number = 0;

  tambahSaldo(jumlah: number): void {
    this.saldo += jumlah;
  }

  cekSaldo(): number {
    return this.saldo;
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

# Assignment 4 - Access Modifier protected (Easy)
Buat class `Kendaraan` dengan properti `merk` bersifat protected, lalu akses dari class turunan.

```ts
class Kendaraan {
  protected merk: string;

  constructor(merk: string) {
    this.merk = merk;
  }
}

class Mobil extends Kendaraan {
  tampilkanMerk(): void {
    console.log(this.merk);
  }
}

let mobil1 = new Mobil("Toyota");
mobil1.tampilkanMerk();
```

**Hasil yang diharapkan:**
```
Toyota
```

---

# Assignment 5 - Static Property dan Method (Easy)
Buat class dengan static property untuk menghitung jumlah object yang sudah dibuat.

```ts
class Siswa {
  static jumlahSiswa: number = 0;

  constructor(public nama: string) {
    Siswa.jumlahSiswa++;
  }
}

new Siswa("Vincent");
new Siswa("Budi");

console.log(Siswa.jumlahSiswa);
```

**Hasil yang diharapkan:**
```
2
```

---

# Assignment 6 - Inheritance dengan super (Medium)
Buat class `Karyawan` yang extends dari class `Manusia`, lalu gunakan `super()` untuk memanggil constructor parent.

```ts
class Manusia {
  constructor(public nama: string, public umur: number) {}
}

class Karyawan extends Manusia {
  constructor(nama: string, umur: number, public jabatan: string) {
    super(nama, umur);
  }
}

let karyawan1 = new Karyawan("Vincent", 25, "Frontend Developer");
console.log(karyawan1);
```

**Hasil yang diharapkan:**
```
Karyawan { nama: 'Vincent', umur: 25, jabatan: 'Frontend Developer' }
```

---

# Assignment 7 - Implements Interface (Medium)
Buat class yang mengimplementasikan sebuah interface `Kendaraan`.

```ts
interface Kendaraan {
  merk: string;
  nyalakanMesin(): void;
}

class Mobil implements Kendaraan {
  constructor(public merk: string) {}

  nyalakanMesin(): void {
    console.log(this.merk + ": Mesin menyala!");
  }
}

let mobil1 = new Mobil("Honda");
mobil1.nyalakanMesin();
```

**Hasil yang diharapkan:**
```
Honda: Mesin menyala!
```

---

# Assignment 8 - Abstract Class (Hard)
Buat abstract class `Bentuk` dengan method abstract `hitungLuas()`, lalu implementasikan pada class `Lingkaran` dan `Persegi`.

```ts
abstract class Bentuk {
  abstract hitungLuas(): number;
}

class Lingkaran extends Bentuk {
  constructor(private jariJari: number) {
    super();
  }

  hitungLuas(): number {
    return Math.PI * this.jariJari * this.jariJari;
  }
}

class Persegi extends Bentuk {
  constructor(private sisi: number) {
    super();
  }

  hitungLuas(): number {
    return this.sisi * this.sisi;
  }
}

let lingkaran1 = new Lingkaran(7);
let persegi1 = new Persegi(5);

console.log(lingkaran1.hitungLuas().toFixed(2));
console.log(persegi1.hitungLuas());
```

**Hasil yang diharapkan:**
```
153.94
25
```
