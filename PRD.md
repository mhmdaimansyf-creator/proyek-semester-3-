# PRD — Sistem Informasi Pengelolaan Persediaan Spare Part Bengkel Abadi Motor

## 1. Gambaran Umum
Aplikasi berbasis web untuk membantu admin Bengkel Abadi Motor mencatat dan memantau persediaan spare part. Sistem dibuat agar pencatatan barang masuk dan keluar lebih rapi serta jumlah stok lebih mudah diketahui.

## 2. Tujuan
- Menyimpan data spare part dalam satu tempat.
- Memudahkan admin mencatat barang masuk dan barang keluar.
- Menampilkan jumlah stok yang tersedia.
- Membantu admin melihat dan mencetak laporan persediaan.

## 3. Pengguna dan Hak Akses
**Admin**
- Login dan logout.
- Melihat dashboard.
- Mengelola data spare part.
- Mencatat transaksi stok masuk dan keluar.
- Melihat serta mencetak laporan.

Untuk versi awal, cukup gunakan satu jenis pengguna yaitu admin. Pemilik bengkel tidak dibuat sebagai aktor terpisah agar ruang lingkup tetap sederhana. Pemilik dapat melihat laporan melalui admin jika diperlukan.

## 4. Modul dan Fitur

### Modul 1 — Login
- Admin masuk menggunakan username/email dan password.
- Sistem memeriksa data login.
- Admin dapat logout.
- Halaman aplikasi selain login hanya dapat dibuka setelah admin login.

### Modul 2 — Dashboard
- Menampilkan jumlah jenis spare part.
- Menampilkan ringkasan stok yang tersedia.
- Menampilkan daftar stok yang hampir habis.
- Menampilkan ringkasan transaksi stok terbaru.

### Modul 3 — Data Spare Part
- Melihat daftar spare part.
- Menambah data spare part.
- Mengubah data spare part.
- Menghapus data spare part setelah konfirmasi.
- Mencari spare part berdasarkan nama atau kode.
- Menyimpan informasi: kode, nama, kategori, satuan, harga beli (opsional), harga jual (opsional), stok, dan batas minimum stok.

### Modul 4 — Transaksi Stok
- Mencatat barang masuk.
- Mencatat barang keluar.
- Memilih spare part dan memasukkan jumlah.
- Menyimpan tanggal, jenis transaksi, jumlah, dan catatan.
- Stok bertambah saat barang masuk.
- Stok berkurang saat barang keluar.
- Sistem menolak transaksi keluar jika jumlahnya melebihi stok tersedia.
- Riwayat transaksi dapat dilihat dan dicari.

### Modul 5 — Laporan
- Melihat laporan persediaan saat ini.
- Melihat riwayat barang masuk dan keluar berdasarkan rentang tanggal.
- Memfilter laporan berdasarkan jenis transaksi atau spare part.
- Mencetak laporan melalui fitur print browser.

## 5. Ruang Lingkup Versi Awal
Termasuk:
- Satu bengkel, yaitu Bengkel Abadi Motor.
- Satu peran pengguna, yaitu admin.
- Pengelolaan data spare part.
- Pencatatan stok masuk dan keluar.
- Laporan persediaan dan transaksi.

Tidak termasuk:
- Pembelian online atau marketplace.
- Pembayaran dan kasir.
- Pemesanan/booking servis.
- Penggajian karyawan.
- Multi-cabang.
- Aplikasi Android/iOS.
- Integrasi barcode atau perangkat eksternal.
- Pengelolaan pemasok secara terpisah pada versi awal.

## 6. Aturan Bisnis
1. Setiap spare part memiliki kode yang unik.
2. Jumlah stok tidak boleh bernilai negatif.
3. Transaksi barang masuk menambah stok.
4. Transaksi barang keluar mengurangi stok.
5. Transaksi keluar tidak boleh melebihi stok tersedia.
6. Data transaksi menyimpan waktu pencatatan dan admin yang melakukan pencatatan.
7. Penghapusan spare part yang sudah memiliki riwayat transaksi sebaiknya dibatasi. Gunakan status aktif/nonaktif atau cegah penghapusan agar riwayat tetap utuh.
8. Batas minimum stok digunakan untuk menandai spare part yang perlu diperiksa atau diisi kembali.

## 7. Data Utama
- **Admin:** id, nama, username/email, password_hash.
- **Spare part:** id, kode, nama, kategori, satuan, harga_beli, harga_jual, stok, stok_minimum, status.
- **Transaksi stok:** id, spare_part_id, admin_id, jenis (masuk/keluar), jumlah, tanggal, catatan.

Catatan: stok saat ini harus konsisten dengan seluruh transaksi. Perubahan stok dan penyimpanan transaksi harus dilakukan dalam satu proses database yang aman.

## 8. Kebutuhan Nonfungsional
- Tampilan mudah dipahami dan responsif di desktop maupun ponsel.
- Password disimpan dalam bentuk hash, bukan teks biasa.
- Form memiliki validasi dan pesan kesalahan yang jelas.
- Halaman admin dilindungi autentikasi.
- Data transaksi tidak boleh hilang ketika halaman dimuat ulang.
- Gunakan struktur kode yang rapi dan mudah dikembangkan.

## 9. Kriteria Penerimaan
- Admin dapat login dan logout.
- Admin dapat menambah, melihat, mengubah, dan menghapus/nonaktifkan spare part.
- Dashboard menampilkan ringkasan berdasarkan data yang tersimpan.
- Barang masuk menambah stok dengan benar.
- Barang keluar mengurangi stok dengan benar dan tidak membuat stok negatif.
- Laporan dapat difilter dan dicetak.
- Fitur utama dapat digunakan melalui browser tanpa kesalahan yang menghalangi proses.

## 10. Asumsi Teknologi
- Frontend: React dengan Vite.
- Styling: Tailwind CSS.
- Backend yang diusulkan: Node.js dengan Express.
- Database: MySQL.
- Pengembangan lokal: VS Code.

**Catatan keputusan:** React-Vite adalah teknologi frontend, bukan pengganti database atau backend. Dokumen ini mengusulkan Node.js + Express untuk API dan MySQL untuk penyimpanan data. Pastikan pilihan backend ini disetujui sebelum implementasi backend dimulai.
