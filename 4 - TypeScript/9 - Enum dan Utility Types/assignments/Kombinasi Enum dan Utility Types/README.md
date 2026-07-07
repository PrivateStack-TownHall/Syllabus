# Assignment 8 - Kombinasi Enum dan Utility Types (Hard)

## Tujuan Pembelajaran

- Memahami konsep enum dan kegunaannya
- Mampu membuat numeric enum dan string enum
- Memahami utility types dasar (Partial, Pick, Omit, Readonly)
- Mampu mengombinasikan enum dengan utility types

## Soal

Buat interface `Pesanan` yang memiliki properti bertipe enum `StatusPesanan`, lalu gunakan kombinasi `Partial` dan `Pick` untuk membuat tipe update pesanan yang hanya bisa mengubah status dan catatan.

Soal ini membutuhkan pemahaman yang lebih mendalam. Coba pecah masalah menjadi beberapa langkah kecil, selesaikan satu per satu, baru kemudian gabungkan menjadi solusi yang utuh.

**Hasil yang diharapkan:**

```
{ status: 'SELESAI' }
```
