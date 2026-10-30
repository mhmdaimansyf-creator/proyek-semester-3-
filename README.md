# Sistem Persediaan Abadi Motor

Prototype frontend untuk pengelolaan persediaan spare part Bengkel Abadi Motor. Seluruh data bersifat dummy dan tersimpan di memori browser; data akan kembali ke contoh awal setelah halaman dimuat ulang.

## Menjalankan aplikasi

```bash
npm install
npm run dev
```

Buka URL lokal yang ditampilkan Vite. Login demo menerima isian email dan kata sandi apa pun yang tidak kosong. Tidak ada autentikasi backend pada tahap ini.

Di Windows PowerShell, jika kebijakan skrip memblokir `npm.ps1`, gunakan `npm.cmd install` dan `npm.cmd run dev`.

## Pemeriksaan produksi

```bash
npm run build
npm run preview
```

## Ruang lingkup

Mencakup Login, Dashboard, Data Spare Part, Transaksi Stok, dan Laporan sesuai dokumen PRD. Backend dan database tidak termasuk.
