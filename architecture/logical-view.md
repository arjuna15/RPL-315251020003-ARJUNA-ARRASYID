# Logical View

Sistem Manajemen Perpustakaan ini dipecah menjadi beberapa komponen logis utama yang saling berinteraksi:

1. **Modul Autentikasi & Otorisasi:** Mengatur *login, logout*, dan hak akses pengguna (*Role-based access* antara Admin dan Anggota).
2. **Modul Katalog Buku:** Mengelola entitas buku, kategori, dan pencarian.
3. **Modul Transaksi:** Menangani logika peminjaman, batas waktu, dan pengembalian.
4. **Modul Denda:** Kalkulator logis yang menghitung nominal denda berdasarkan selisih tanggal pengembalian aktual dan tenggat waktu.

**Alur Interaksi Sederhana (MVC):**
- **User** (Anggota) melakukan pencarian buku melalui antarmuka web (**View**).
- Permintaan dikirim ke **Controller** Katalog.
- **Controller** meminta data buku yang relevan dari **Model** Buku.
- **Model** mengambil data dari basis data dan mengembalikannya ke **Controller**.
- **Controller** mengirimkan data tersebut ke **View** untuk ditampilkan kembali kepada **User**.