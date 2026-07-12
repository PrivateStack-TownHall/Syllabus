# Tujuan Pembelajaran
- Mampu membangun aplikasi CLI interaktif menggunakan package eksternal prompt-sync
- Mampu menggabungkan OOP dan MVC dalam studi kasus yang bervariasi dan kompleks
- Mampu merancang alur program dengan banyak validasi, percabangan, dan perulangan
- Mampu mengelola state aplikasi yang berubah secara dinamis berdasarkan input pengguna

# Cara Install
Sebelum mengerjakan soal-soal di folder ini, install package `prompt-sync` terlebih dahulu:
```bash
npm init -y
npm i prompt-sync
```
Lalu import di bagian paling atas file kamu:
```js
const prompt = require("prompt-sync")();
```

---

# Assignment 1 - Booking Tiket Bioskop Interaktif (Hard)
Buat program CLI pemesanan tiket bioskop. Program menampilkan daftar film beserta harga dan sisa kursi, lalu pengguna memilih film dan jumlah tiket yang diinginkan.

```js
const prompt = require("prompt-sync")();

const FilmModel = [
  { judul: "Petualangan Luar Angkasa", harga: 35000, kursiTersedia: 5 },
  { judul: "Misteri Kota Tua", harga: 40000, kursiTersedia: 2 },
];

function FilmView(daftarFilm) {
  console.log("=== Daftar Film ===");
  daftarFilm.forEach((f, i) =>
    console.log(`${i + 1}. ${f.judul} - Rp${f.harga} (sisa kursi: ${f.kursiTersedia})`)
  );
}

function BookingController() {
  FilmView(FilmModel);
  const nomor = Number(prompt("Pilih nomor film: ")) - 1;

  if (nomor < 0 || nomor >= FilmModel.length) {
    console.log("Nomor film tidak valid");
    return;
  }

  const film = FilmModel[nomor];
  const jumlahTiket = Number(prompt("Jumlah tiket: "));

  if (jumlahTiket > film.kursiTersedia) {
    console.log("Kursi tidak cukup");
    return;
  }

  film.kursiTersedia -= jumlahTiket;
  const total = film.harga * jumlahTiket;

  console.log("=== Tiket Berhasil Dipesan ===");
  console.log(`Film: ${film.judul}`);
  console.log(`Jumlah: ${jumlahTiket}`);
  console.log(`Total Bayar: Rp${total}`);
}

BookingController();
```

**Hasil yang diharapkan:**
```
Input: pilih film 1, jumlah tiket 2
Output:
=== Tiket Berhasil Dipesan ===
Film: Petualangan Luar Angkasa
Jumlah: 2
Total Bayar: Rp70000

Input: pilih film 5 (tidak ada)
Output: Nomor film tidak valid

Input: pilih film 2, jumlah tiket 5 (kursi cuma 2)
Output: Kursi tidak cukup
```

---

# Assignment 2 - Sistem Antrian Rumah Sakit dengan Prioritas (Hard)
Buat program CLI yang menerima data pasien (nama dan kategori) secara berulang, lalu mengurutkan antrian berdasarkan prioritas kategori sebelum ditampilkan.

```js
const prompt = require("prompt-sync")();

class Pasien {
  constructor(nama) {
    this.nama = nama;
    this.kategori = "umum";
  }
  getPrioritas() {
    return 3;
  }
}

class PasienBPJS extends Pasien {
  constructor(nama) {
    super(nama);
    this.kategori = "bpjs";
  }
  getPrioritas() {
    return 2;
  }
}

class PasienDarurat extends Pasien {
  constructor(nama) {
    super(nama);
    this.kategori = "darurat";
  }
  getPrioritas() {
    return 1;
  }
}

function AntrianView(daftarPasien) {
  console.log("=== Urutan Antrian ===");
  daftarPasien.forEach((p, i) => console.log(`${i + 1}. ${p.nama} (${p.kategori})`));
}

function AntrianController() {
  const daftarPasien = [];

  while (true) {
    const nama = prompt('Nama pasien (atau ketik "selesai"): ');
    if (nama === "selesai") break;

    let kategori = prompt("Kategori (umum/bpjs/darurat): ");
    while (!["umum", "bpjs", "darurat"].includes(kategori)) {
      console.log("Kategori tidak valid");
      kategori = prompt("Kategori (umum/bpjs/darurat): ");
    }

    let pasien;
    if (kategori === "bpjs") pasien = new PasienBPJS(nama);
    else if (kategori === "darurat") pasien = new PasienDarurat(nama);
    else pasien = new Pasien(nama);

    daftarPasien.push(pasien);
  }

  daftarPasien.sort((a, b) => a.getPrioritas() - b.getPrioritas());
  AntrianView(daftarPasien);
}

AntrianController();
```

**Hasil yang diharapkan:**
```
Input: Budi/umum, Ani/darurat, Cici/bpjs, lalu "selesai"
Output:
=== Urutan Antrian ===
1. Ani (darurat)
2. Cici (bpjs)
3. Budi (umum)
```

---

# Assignment 3 - Manajemen Perpustakaan dengan Denda Keterlambatan (Hard)
Buat program CLI yang menerima data buku yang dipinjam (judul dan jumlah hari peminjaman) secara berulang, menghitung denda jika melewati batas peminjaman, lalu menampilkan ringkasan beserta total denda.

```js
const prompt = require("prompt-sync")();

class PeminjamanModel {
  constructor() {
    this.data = [];
    this.batasHari = 7;
    this.tarifDendaPerHari = 2000;
  }

  tambah(judul, jumlahHari) {
    const hariTelat = Math.max(0, jumlahHari - this.batasHari);
    const denda = hariTelat * this.tarifDendaPerHari;
    this.data.push({ judul, jumlahHari, denda });
  }

  totalDenda() {
    return this.data.reduce((total, b) => total + b.denda, 0);
  }
}

function RingkasanView(data, total) {
  console.log("=== Ringkasan Peminjaman ===");
  data.forEach((b) => {
    const status = b.denda > 0 ? `Telat, denda Rp${b.denda}` : "Tepat waktu";
    console.log(`${b.judul} (${b.jumlahHari} hari): ${status}`);
  });
  console.log(`Total Denda: Rp${total}`);
}

function PerpustakaanController() {
  const model = new PeminjamanModel();

  while (true) {
    const judul = prompt('Judul buku (atau ketik "selesai"): ');
    if (judul === "selesai") break;

    let jumlahHari = Number(prompt("Jumlah hari peminjaman: "));
    while (isNaN(jumlahHari) || jumlahHari <= 0) {
      console.log("Jumlah hari harus angka positif");
      jumlahHari = Number(prompt("Jumlah hari peminjaman: "));
    }

    model.tambah(judul, jumlahHari);
  }

  RingkasanView(model.data, model.totalDenda());
}

PerpustakaanController();
```

**Hasil yang diharapkan:**
```
Input: "Laskar Pelangi"/5 hari, "Bumi Manusia"/10 hari, lalu "selesai"
Output:
=== Ringkasan Peminjaman ===
Laskar Pelangi (5 hari): Tepat waktu
Bumi Manusia (10 hari): Telat, denda Rp6000
Total Denda: Rp6000
```

---

# Assignment 4 - Kuis Interaktif dengan Skor dan Level (Hard)
Buat program kuis pilihan ganda interaktif. Program menampilkan beberapa soal satu per satu, mencocokkan jawaban pengguna, lalu menampilkan skor akhir dan level berdasarkan skor tersebut.

```js
const prompt = require("prompt-sync")();

const SoalModel = [
  { pertanyaan: "Ibu kota Indonesia?", pilihan: ["A. Bandung", "B. Jakarta", "C. Surabaya"], jawabanBenar: "B" },
  { pertanyaan: "2 + 2 x 2 = ?", pilihan: ["A. 6", "B. 8", "C. 4"], jawabanBenar: "A" },
  { pertanyaan: "HTML adalah singkatan dari?", pilihan: ["A. HyperText Markup Language", "B. High Text Machine Language", "C. Home Tool Markup Language"], jawabanBenar: "A" },
];

function tentukanLevel(skor) {
  if (skor >= 80) return "Mahir";
  if (skor >= 50) return "Menengah";
  return "Pemula";
}

function HasilView(skor, level) {
  console.log("=== Hasil Kuis ===");
  console.log(`Skor: ${skor}`);
  console.log(`Level: ${level}`);
}

function KuisController() {
  let skor = 0;
  const poinPerSoal = Math.round(100 / SoalModel.length);

  SoalModel.forEach((soal, i) => {
    console.log(`Soal ${i + 1}: ${soal.pertanyaan}`);
    soal.pilihan.forEach((p) => console.log(p));
    const jawaban = prompt("Jawaban: ").toUpperCase();

    if (jawaban === soal.jawabanBenar) {
      skor += poinPerSoal;
    }
  });

  HasilView(skor, tentukanLevel(skor));
}

KuisController();
```

**Hasil yang diharapkan:**
```
Input: jawab semua benar (B, A, A)
Output:
=== Hasil Kuis ===
Skor: 99
Level: Mahir

Input: jawab 1 benar dari 3 soal
Output:
=== Hasil Kuis ===
Skor: 33
Level: Pemula
```

---

# Assignment 5 - Sistem Parkir dengan Tarif Bertingkat (Hard)
Buat program CLI sistem parkir yang menerima data kendaraan (jenis dan durasi parkir dalam jam) secara berulang, menghitung tarif berdasarkan jenis kendaraan menggunakan inheritance dan polimorfisme, lalu menampilkan struk dan total pendapatan.

```js
const prompt = require("prompt-sync")();

class Kendaraan {
  constructor(durasiJam) {
    this.durasiJam = durasiJam;
  }
  hitungTarif() {
    return 0;
  }
}

class Mobil extends Kendaraan {
  hitungTarif() {
    return this.durasiJam * 5000;
  }
}

class Motor extends Kendaraan {
  hitungTarif() {
    return this.durasiJam * 2000;
  }
}

function StrukView(jenis, durasiJam, tarif) {
  console.log(`${jenis} (${durasiJam} jam): Rp${tarif}`);
}

function ParkirController() {
  let totalPendapatan = 0;

  while (true) {
    let jenis = prompt('Jenis kendaraan (mobil/motor/selesai): ');
    if (jenis === "selesai") break;

    while (jenis !== "mobil" && jenis !== "motor") {
      console.log("Jenis tidak valid");
      jenis = prompt("Jenis kendaraan (mobil/motor/selesai): ");
      if (jenis === "selesai") return;
    }

    let durasiJam = Number(prompt("Durasi parkir (jam): "));
    while (isNaN(durasiJam) || durasiJam <= 0) {
      console.log("Durasi harus angka positif");
      durasiJam = Number(prompt("Durasi parkir (jam): "));
    }

    const kendaraan = jenis === "mobil" ? new Mobil(durasiJam) : new Motor(durasiJam);
    const tarif = kendaraan.hitungTarif();

    StrukView(jenis, durasiJam, tarif);
    totalPendapatan += tarif;
  }

  console.log(`Total Pendapatan Parkir: Rp${totalPendapatan}`);
}

ParkirController();
```

**Hasil yang diharapkan:**
```
Input: mobil/3 jam, motor/2 jam, lalu "selesai"
Output:
mobil (3 jam): Rp15000
motor (2 jam): Rp4000
Total Pendapatan Parkir: Rp19000
```
