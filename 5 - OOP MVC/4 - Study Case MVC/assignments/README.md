# Tujuan Pembelajaran
- Mampu menerapkan pola MVC dalam studi kasus yang lebih kompleks
- Mampu membangun aplikasi CLI sederhana dengan pola command & params (process.argv)
- Mampu mengintegrasikan OOP (class, method) ke dalam arsitektur MVC
- Mampu membangun mini project akhir yang membaca input dari command line

---

# Assignment 1 - Model Transaksi dari Argument CLI (Easy)
Buat program yang membaca command beserta params (jenis, jumlah, keterangan transaksi) dari command line, simpan ke dalam Model, dan tampilkan hasilnya.

```js
class TransaksiModel {
  constructor(jenis, jumlah, keterangan) {
    this.jenis = jenis;
    this.jumlah = jumlah;
    this.keterangan = keterangan;
  }
}

const command = process.argv[2];
const params = process.argv.slice(3);

const transaksi1 = new TransaksiModel(params[0], params[1], params[2]);
console.log(transaksi1);
```

**Hasil yang diharapkan:**
```
Command: node index.js tambah Pemasukan 500000 Gaji
Output: TransaksiModel { jenis: 'Pemasukan', jumlah: '500000', keterangan: 'Gaji' }
```

---

# Assignment 2 - View Transaksi dari Argument (Easy)
Tampilkan data transaksi dari params menggunakan format `[jenis] keterangan: Rp jumlah`, dengan jumlah yang sudah dikonversi menjadi angka.

```js
function TransaksiView(jenis, jumlah, keterangan) {
  console.log(`[${jenis}] ${keterangan}: Rp${jumlah}`);
}

const command = process.argv[2];
const params = process.argv.slice(3);

const jenis = params[0];
const jumlah = Number(params[1]);
const keterangan = params[2];

TransaksiView(jenis, jumlah, keterangan);
```

**Hasil yang diharapkan:**
```
Command: node index.js tambah Pengeluaran 20000 "Makan siang"
Output: [Pengeluaran] Makan siang: Rp20000
```

---

# Assignment 3 - Controller Menambah Transaksi via Argument (Medium)
Buat Controller yang membaca command dan params, membuat data transaksi lewat Model, lalu menampilkannya lewat View.

```js
class TransaksiModel {
  constructor(jenis, jumlah, keterangan) {
    this.jenis = jenis;
    this.jumlah = jumlah;
    this.keterangan = keterangan;
  }
}

function TransaksiView(jenis, jumlah, keterangan) {
  console.log(`[${jenis}] ${keterangan}: Rp${jumlah}`);
}

function TransaksiController() {
  const command = process.argv[2];
  const params = process.argv.slice(3);

  const transaksi = new TransaksiModel(params[0], Number(params[1]), params[2]);
  TransaksiView(transaksi.jenis, transaksi.jumlah, transaksi.keterangan);
}

TransaksiController();
```

**Hasil yang diharapkan:**
```
Command: node index.js tambah Pemasukan 500000 Gaji
Output: [Pemasukan] Gaji: Rp500000
```

---

# Assignment 4 - Validasi Command dan Params untuk Hitung Saldo (Medium)
Program menerima command "hitung-saldo" beserta params (saldo awal, jenis, jumlah), validasi command dan jumlah harus angka positif, lalu hitung saldo akhir.

```js
function hitungSaldoAkhir(saldoAwal, jenis, jumlah) {
  return jenis === "Pemasukan" ? saldoAwal + jumlah : saldoAwal - jumlah;
}

function SaldoController() {
  const command = process.argv[2];
  const params = process.argv.slice(3);

  if (command !== "hitung-saldo") {
    console.log("Command tidak dikenali");
    return;
  }

  const [saldoAwalRaw, jenis, jumlahRaw] = params;
  const saldoAwal = Number(saldoAwalRaw);
  const jumlah = Number(jumlahRaw);

  if (isNaN(jumlah) || jumlah <= 0) {
    console.log("Jumlah harus berupa angka positif");
    return;
  }

  const saldoAkhir = hitungSaldoAkhir(saldoAwal, jenis, jumlah);
  console.log(`Saldo akhir: Rp${saldoAkhir}`);
}

SaldoController();
```

**Hasil yang diharapkan:**
```
Command: node index.js hitung-saldo 1000000 Pengeluaran 250000
Output: Saldo akhir: Rp750000

Command: node index.js hitung-saldo 500000 Pemasukan -200000
Output: Jumlah harus berupa angka positif

Command: node index.js cek 500000 Pemasukan 200000
Output: Command tidak dikenali
```

---

# Assignment 5 - Mini CLI Aplikasi Keuangan dengan Validasi Lengkap (Hard)
Bangun program CLI dengan command "tambah-transaksi" yang menerima params (jenis, jumlah, keterangan), melakukan validasi lengkap, lalu menampilkan hasil transaksi beserta saldo akhir dari saldo awal tetap yang sudah ditentukan di dalam program.

```js
function TransaksiView(jenis, jumlah, keterangan) {
  console.log(`[${jenis}] ${keterangan}: Rp${jumlah}`);
}

function KeuanganController() {
  const saldoAwal = 1000000;
  const command = process.argv[2];
  const params = process.argv.slice(3);

  if (command !== "tambah-transaksi") {
    console.log("Command tidak dikenali");
    return;
  }

  const [jenis, jumlahRaw, keterangan] = params;

  if (jenis !== "Pemasukan" && jenis !== "Pengeluaran") {
    console.log("Jenis transaksi tidak valid");
    return;
  }

  const jumlah = Number(jumlahRaw);
  if (isNaN(jumlah) || jumlah <= 0) {
    console.log("Jumlah harus berupa angka positif");
    return;
  }

  const saldoAkhir = jenis === "Pemasukan" ? saldoAwal + jumlah : saldoAwal - jumlah;

  TransaksiView(jenis, jumlah, keterangan);
  console.log(`Saldo akhir: Rp${saldoAkhir}`);
}

KeuanganController();
```

**Hasil yang diharapkan:**
```
Command: node index.js tambah-transaksi Pengeluaran 250000 Belanja
Output:
[Pengeluaran] Belanja: Rp250000
Saldo akhir: Rp750000

Command: node index.js cek Pengeluaran 250000 Belanja
Output: Command tidak dikenali

Command: node index.js tambah-transaksi Investasi 100000 Saham
Output: Jenis transaksi tidak valid

Command: node index.js tambah-transaksi Pemasukan -50000 Bonus
Output: Jumlah harus berupa angka positif
```
