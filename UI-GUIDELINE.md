# UI Guideline — Bengkel Abadi Motor

## 1. Arah Desain
Buat antarmuka admin yang sederhana, rapi, modern, dan mudah digunakan. Utamakan kejelasan informasi stok daripada dekorasi yang berlebihan.

## 2. Gaya Visual
- Tema: light mode.
- Latar utama: abu-abu sangat muda.
- Area konten/kartu: putih.
- Warna utama: biru tua atau navy.
- Warna aksi: biru.
- Hijau untuk status stok aman atau transaksi masuk.
- Oranye untuk stok menipis.
- Merah untuk stok habis, transaksi keluar, atau pesan kesalahan.
- Gunakan warna status secara konsisten dan jangan mengandalkan warna saja; sertakan teks status.

## 3. Tata Letak
- Sidebar di sisi kiri untuk navigasi utama.
- Header bagian atas menampilkan nama halaman dan akun admin.
- Area konten menampilkan judul, deskripsi singkat, aksi utama, lalu isi halaman.
- Pada layar kecil, sidebar berubah menjadi menu yang dapat dibuka/tutup.
- Gunakan jarak antarbagian yang konsisten dan hindari tampilan terlalu padat.

## 4. Navigasi
Menu yang disarankan:
1. Dashboard
2. Data Spare Part
3. Transaksi Stok
4. Laporan
5. Logout

Login ditampilkan sebagai halaman tersendiri, bukan menu sidebar.

## 5. Panduan Tiap Halaman

### Login
- Tampilkan nama/logo teks Bengkel Abadi Motor.
- Sediakan input username/email dan password.
- Tombol masuk terlihat jelas.
- Tampilkan pesan jika data login salah.
- Jangan tampilkan password dalam teks biasa secara default.

### Dashboard
- Tampilkan kartu ringkasan: jumlah jenis spare part, total stok, stok menipis, dan transaksi terbaru.
- Tampilkan tabel stok yang hampir habis.
- Tampilkan daftar transaksi terbaru.
- Hindari grafik yang tidak dibutuhkan pada versi awal.

### Data Spare Part
- Tampilkan tabel dengan kolom kode, nama, kategori, stok, satuan, dan aksi.
- Sediakan pencarian dan tombol tambah spare part.
- Form tambah/edit menggunakan label yang jelas.
- Beri konfirmasi sebelum menghapus atau menonaktifkan data.

### Transaksi Stok
- Sediakan pilihan transaksi barang masuk atau barang keluar.
- Form memuat spare part, jumlah, tanggal, dan catatan.
- Tampilkan stok tersedia sebelum transaksi keluar disimpan.
- Berikan ringkasan/konfirmasi sebelum penyimpanan bila diperlukan.
- Tampilkan riwayat transaksi dalam tabel.

### Laporan
- Sediakan filter tanggal, jenis transaksi, dan spare part.
- Tampilkan tabel hasil filter dan ringkasan jumlah.
- Sediakan tombol Cetak.
- Tata letak cetak harus sederhana dan tidak menyertakan navigasi/sidebar.

## 6. Komponen dan Interaksi
- Tombol utama menggunakan label tindakan yang jelas, misalnya "Tambah Spare Part" atau "Simpan Transaksi".
- Tombol berbahaya seperti hapus menggunakan warna peringatan dan konfirmasi.
- Form menampilkan validasi dekat dengan input terkait.
- Tabel memiliki tampilan kosong yang informatif jika belum ada data.
- Tampilkan indikator loading saat data sedang dimuat.
- Tampilkan notifikasi berhasil/gagal setelah tindakan.
- Format tanggal dan angka harus konsisten.

## 7. Responsif dan Aksesibilitas
- Pastikan tabel dapat digulir horizontal di layar kecil.
- Input memiliki label, bukan hanya placeholder.
- Kontras teks dan latar cukup jelas.
- Tombol dan input dapat digunakan dengan keyboard.
- Ukuran teks nyaman dibaca.

## 8. Batasan Desain
- Jangan menambahkan halaman atau fitur di luar PRD.
- Jangan menggunakan data dummy setelah backend dan database sudah terhubung.
- Pertahankan pola warna, tombol, tabel, form, dan jarak yang konsisten di semua halaman.
