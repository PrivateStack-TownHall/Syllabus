# Assignment - Sistem Penilaian Mobil Bekas (Hard)

## Tujuan Pembelajaran

- Memahami penerapan percabangan bertingkat pada studi kasus.
- Mampu menganalisis aturan bisnis ke dalam bentuk algoritma.
- Mampu menyusun pseudocode sebelum membuat program.
- Mampu mengimplementasikan logika yang terdiri dari banyak kondisi.

## Soal

PT **Cartwright** merupakan perusahaan yang bergerak di bidang jual beli mobil bekas di wilayah Jabodetabek.

Buatlah **pseudocode** dan **program** untuk menentukan status kelayakan jual sebuah mobil berdasarkan aturan berikut.

### Tipe LCGC

- Pajak sudah dibayar → Layak Jual
- Pajak belum dibayar → Tidak Layak Jual

### Tipe MPV

- Pajak sudah dibayar + Plat Genap → Layak Jual
- Pajak sudah dibayar + Plat Ganjil → Layak Jual Bersyarat
- Pajak belum dibayar + Plat Genap → Layak Jual Bersyarat
- Pajak belum dibayar + Plat Ganjil → Layak Jual dengan Harga di Bawah Rata-rata

### Tipe SPV

- Pajak sudah dibayar → Layak Jual
- Pajak belum dibayar:
  - Honda atau Toyota → Layak Jual
  - Daihatsu → Layak Jual Bersyarat
  - Merek lainnya → Layak Jual dengan Harga di Bawah Rata-rata

> **Catatan:** Analisis terlebih dahulu seluruh aturan bisnis sebelum menyusun pseudocode dan program.

## Result / Test Case

**Input**

```text
Tipe Mobil : MPV
Pajak : Sudah Dibayar
Plat : Ganjil
```

**Output**

```text
Layak Jual Bersyarat
```
