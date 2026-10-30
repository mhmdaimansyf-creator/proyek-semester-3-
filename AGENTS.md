# AGENTS.md — Aturan AI Agent

## Identitas Proyek
Nama: Sistem Informasi Pengelolaan Persediaan Spare Part Berbasis Web pada Bengkel Abadi Motor.

## Sumber Acuan
Sebelum mulai bekerja, baca:
- `PRD.md` untuk kebutuhan dan ruang lingkup.
- `UI-GUIDELINE.md` untuk aturan antarmuka.
- `IMPLEMENTATION_PLAN.md` untuk urutan pengerjaan.

Jika instruksi chat bertentangan dengan dokumen, berhenti dan minta klarifikasi. Jangan memilih sendiri.

## Stack
- Frontend: React + Vite.
- Styling: Tailwind CSS.
- Backend usulan: Node.js + Express (jangan mulai implementasi backend sebelum dikonfirmasi).
- Database: MySQL.

## Aturan Utama
- Ikuti dokumen SOT sebagai acuan utama.
- Versi awal hanya memiliki satu aktor: admin.
- Pertahankan lima modul utama: Login, Dashboard, Data Spare Part, Transaksi Stok, dan Laporan.
- Jangan membuat fitur tambahan di luar PRD.
- Jangan mengganti teknologi atau menambah dependensi besar tanpa persetujuan.
- Gunakan komponen yang konsisten dan kode yang mudah dibaca.
- Jangan menaruh password atau kredensial database di kode frontend atau repository.
- Jangan menyimpan password dalam bentuk teks biasa.
- Validasi input di frontend dan backend.
- Pastikan transaksi barang keluar tidak membuat stok negatif.
- Jangan menghapus riwayat transaksi.

## Cara Bekerja
1. Periksa isi folder dan file yang sudah ada sebelum membuat perubahan.
2. Sebutkan rencana singkat sebelum mengerjakan.
3. Kerjakan hanya tahap yang diminta dari IMPLEMENTATION_PLAN.md.
4. Jangan lanjut ke tahap berikutnya sebelum pengguna menyetujui.
5. Jangan menimpa file yang sudah berisi pekerjaan tanpa memeriksa dan meminta izin.
6. Setelah coding, jalankan pemeriksaan yang sesuai, misalnya lint/build atau pengujian.
7. Laporkan file yang dibuat/diubah, perintah yang dijalankan, hasil pemeriksaan, dan hal yang belum selesai.
8. Jika terjadi error, jelaskan penyebab yang diketahui dan perbaiki tanpa mengubah ruang lingkup.
9. Jika ada keputusan yang belum ditentukan, tanyakan sebelum menerapkan asumsi.

## Batasan Tahap Awal
Tahap awal hanya menyiapkan fondasi frontend dan tampilan menggunakan data dummy jika pengguna menyetujuinya. Jangan membuat backend, database, atau fitur tambahan sebelum tahap tersebut diminta dan stack backend dikonfirmasi.
