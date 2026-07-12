# Tujuan Pembelajaran
- Memahami konsep arsitektur MVC (Model-View-Controller)
- Mampu membedakan tanggung jawab Model, View, dan Controller
- Mampu membaca input dari command line menggunakan pola command & params (process.argv)
- Mampu membuat Controller yang menghubungkan Model, View, dan input CLI

---

# Assignment 1 - Model Produk dari Argument CLI (Easy)
Buat program yang membaca command beserta params (nama dan harga produk) dari command line, lalu gunakan Model untuk menyimpan datanya dan tampilkan hasilnya.

```js
class ProdukModel {
  constructor(nama, harga) {
    this.nama = nama;
    this.harga = harga;
  }
}

const command = process.argv[2];
const params = process.argv.slice(3);

const produk1 = new ProdukModel(params[0], params[1]);
console.log(produk1);
```

**Hasil yang diharapkan:**
```
Command: node index.js tambah Mouse 150000
Output: ProdukModel { nama: 'Mouse', harga: '150000' }
```

---

# Assignment 2 - View untuk Menampilkan Data dari Argument (Easy)
Gunakan data dari params untuk ditampilkan lewat function View dengan format yang rapi dan harga yang sudah dikonversi ke angka.

```js
function ProdukView(nama, harga) {
  console.log(`Nama: ${nama}, Harga: Rp${harga}`);
}

const command = process.argv[2];
const params = process.argv.slice(3);

const nama = params[0];
const harga = Number(params[1]);

ProdukView(nama, harga);
```

**Hasil yang diharapkan:**
```
Command: node index.js tambah Monitor 2500000
Output: Nama: Monitor, Harga: Rp2500000
```

---

# Assignment 3 - Controller Penghubung dengan Argument CLI (Medium)
Buat Controller yang membaca command dan params, membuat Model, lalu menampilkannya lewat View.

```js
class ProdukModel {
  constructor(nama, harga) {
    this.nama = nama;
    this.harga = harga;
  }
}

function ProdukView(nama, harga) {
  console.log(`Nama: ${nama}, Harga: Rp${harga}`);
}

function ProdukController() {
  const command = process.argv[2];
  const params = process.argv.slice(3);

  const produk = new ProdukModel(params[0], Number(params[1]));
  ProdukView(produk.nama, produk.harga);
}

ProdukController();
```

**Hasil yang diharapkan:**
```
Command: node index.js tambah Headset 450000
Output: Nama: Headset, Harga: Rp450000
```

---

# Assignment 4 - Validasi Command dan Params di Controller (Medium)
Tambahkan validasi: command harus "tambah", params harus lengkap, dan harga harus berupa angka positif, sebelum data diteruskan ke Model.

```js
class ProdukModel {
  constructor(nama, harga) {
    this.nama = nama;
    this.harga = harga;
  }
}

function ProdukView(nama, harga) {
  console.log(`Nama: ${nama}, Harga: Rp${harga}`);
}

function ProdukController() {
  const command = process.argv[2];
  const params = process.argv.slice(3);

  if (command !== "tambah") {
    console.log("Command tidak dikenali");
    return;
  }

  const [nama, hargaRaw] = params;
  if (!nama || !hargaRaw) {
    console.log("Params tidak lengkap. Contoh: node index.js tambah <nama> <harga>");
    return;
  }

  const harga = Number(hargaRaw);
  if (isNaN(harga) || harga <= 0) {
    console.log("Harga tidak valid");
    return;
  }

  const produk = new ProdukModel(nama, harga);
  ProdukView(produk.nama, produk.harga);
}

ProdukController();
```

**Hasil yang diharapkan:**
```
Command: node index.js hapus Mouse 150000
Output: Command tidak dikenali

Command: node index.js tambah Mouse
Output: Params tidak lengkap. Contoh: node index.js tambah <nama> <harga>

Command: node index.js tambah Mouse -1000
Output: Harga tidak valid

Command: node index.js tambah Mouse 150000
Output: Nama: Mouse, Harga: Rp150000
```

---

# Assignment 5 - Mini CLI Manajemen Produk dengan Multiple Command (Hard)
Bangun program CLI yang mendukung dua command berbeda, "tambah" dan "diskon", masing-masing dengan params-nya sendiri.

```js
class ProdukModel {
  constructor(nama, harga) {
    this.nama = nama;
    this.harga = harga;
  }

  hitungDiskon(persen) {
    return this.harga - (this.harga * persen) / 100;
  }
}

function ProdukView(nama, harga, label = "Harga") {
  console.log(`Nama: ${nama}, ${label}: Rp${harga}`);
}

function ProdukController() {
  const command = process.argv[2];
  const params = process.argv.slice(3);

  if (command === "tambah") {
    const [nama, hargaRaw] = params;
    const produk = new ProdukModel(nama, Number(hargaRaw));
    ProdukView(produk.nama, produk.harga);
  } else if (command === "diskon") {
    const [nama, hargaRaw, persenRaw] = params;
    const produk = new ProdukModel(nama, Number(hargaRaw));
    const hargaAkhir = produk.hitungDiskon(Number(persenRaw));
    ProdukView(produk.nama, hargaAkhir, "Harga Setelah Diskon");
  } else {
    console.log("Command tidak dikenali");
  }
}

ProdukController();
```

**Hasil yang diharapkan:**
```
Command: node index.js tambah Mouse 150000
Output: Nama: Mouse, Harga: Rp150000

Command: node index.js diskon Laptop 10000000 10
Output: Nama: Laptop, Harga Setelah Diskon: Rp9000000

Command: node index.js hapus Mouse
Output: Command tidak dikenali
```
