# Implementation Plan — Bengkel Abadi Motor

## Prinsip Pengerjaan
Gunakan pendekatan RAD (Rapid Application Development): kebutuhan dibahas, rancangan dibuat dan ditinjau, aplikasi dibangun dalam bagian kecil, lalu diuji bersama pengguna. Selesaikan satu tahap dan minta persetujuan sebelum melanjutkan ke tahap berikutnya.

## Tahap 1 — Perencanaan Kebutuhan
**Pekerjaan**
- Baca dan sepakati PRD.
- Pastikan aktor hanya admin untuk versi awal.
- Pastikan 5 modul: Login, Dashboard, Data Spare Part, Transaksi Stok, Laporan.
- Konfirmasi teknologi backend yang akan dipakai.

**Hasil**
- Kebutuhan dan batasan proyek disetujui.
- Daftar halaman dan alur penggunaan disepakati.

**Pemeriksaan**
- Tidak ada fitur tambahan di luar PRD.
- Aturan stok masuk/keluar dipahami.

## Tahap 2 — Desain Pengguna (User Design)
**Pekerjaan**
- Buat wireframe sederhana untuk Login, Dashboard, Data Spare Part, Transaksi Stok, dan Laporan.
- Tinjau navigasi, form, tabel, dan tampilan responsif.
- Revisi berdasarkan masukan.

**Hasil**
- Rancangan antarmuka yang disetujui.
- Komponen visual mengikuti UI-GUIDELINE.md.

**Pemeriksaan**
- Semua halaman sesuai lima modul.
- Alur admin dapat dipahami sebelum coding utama.

## Tahap 3 — Konstruksi
Kerjakan bertahap. Setelah setiap bagian selesai, jalankan aplikasi dan uji sebelum lanjut.

### 3A. Fondasi Frontend
- Buat proyek React-Vite.
- Atur Tailwind CSS sesuai versi dan panduan instalasi yang berlaku.
- Buat layout, sidebar, header, routing, dan halaman login.
- Gunakan data dummy sementara untuk preview.

**Selesai jika:** seluruh halaman utama dapat dibuka dan tampil konsisten.

### 3B. Modul Data Spare Part
- Buat form dan tabel spare part.
- Tambahkan validasi.
- Hubungkan CRUD ke API setelah backend tersedia.

**Selesai jika:** admin dapat mengelola data spare part dan data tetap tersimpan.

### 3C. Modul Transaksi Stok
- Buat form barang masuk dan keluar.
- Terapkan aturan stok tidak boleh negatif.
- Simpan riwayat transaksi.

**Selesai jika:** stok berubah sesuai transaksi dan riwayat tersimpan benar.

### 3D. Dashboard dan Laporan
- Hubungkan ringkasan dashboard ke data sebenarnya.
- Buat filter laporan dan fungsi cetak.

**Selesai jika:** angka dashboard dan laporan sesuai data database.

### 3E. Backend dan Database
Jika backend Node.js + Express disetujui:
- Buat API autentikasi, spare part, transaksi, dashboard, dan laporan.
- Buat skema MySQL dan relasi tabel.
- Hash password.
- Validasi data di server.
- Gunakan transaksi database saat menyimpan transaksi stok dan memperbarui jumlah stok.

**Selesai jika:** frontend menggunakan API dan data tersimpan di MySQL, bukan data dummy.

## Tahap 4 — Pengujian dan Implementasi
**Pekerjaan**
- Uji login benar dan salah.
- Uji tambah, edit, cari, dan nonaktifkan spare part.
- Uji barang masuk.
- Uji barang keluar dengan jumlah valid dan melebihi stok.
- Uji filter laporan dan cetak.
- Uji tampilan desktop dan ponsel.
- Perbaiki bug yang ditemukan.

**Hasil**
- Aplikasi siap didemonstrasikan.
- Catatan pengujian dan perbaikan.

## Aturan untuk AI Agent
1. Baca PRD.md, UI-GUIDELINE.md, IMPLEMENTATION_PLAN.md, dan AGENTS.md sebelum mengubah kode.
2. Kerjakan hanya satu tahap atau sub-tahap dalam satu waktu.
3. Sebelum berpindah tahap, jelaskan hasil dan minta persetujuan pengguna.
4. Jangan menambah fitur, aktor, halaman, atau teknologi tanpa persetujuan.
5. Jangan mengganti stack teknologi secara sepihak.
6. Jangan menghapus atau menimpa file penting tanpa izin.
7. Jelaskan perintah terminal sebelum menjalankannya jika memerlukan persetujuan.
8. Setelah perubahan, jalankan pemeriksaan yang relevan dan laporkan hasilnya.
9. Jika ada informasi yang belum jelas, tanyakan satu hal yang paling penting; jangan menebak keputusan besar.
10. Perbarui dokumen SOT jika kebutuhan proyek berubah dan telah disetujui.
