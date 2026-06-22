# Maintenance Plan: Sistem Manajemen Perpustakaan

## Corrective
1. Memperbaiki *bug* pada fitur pengembalian buku di mana denda keterlambatan tidak terkalkulasi otomatis.
2. Memperbaiki *error 500* saat admin mengunggah sampul buku dengan format gambar yang tidak didukung sistem.
3. Memperbaiki kegagalan *login* pada anggota saat sesi *token* kedaluwarsa tanpa melakukan *redirect* kembali ke halaman *login*.

## Adaptive
4. Menyesuaikan integrasi *Payment Gateway* (untuk pembayaran denda online) karena adanya pembaruan versi *endpoint* API dari pihak penyedia.
5. Melakukan *upgrade* versi *framework* (misal: ke versi Laravel terbaru) dan *library* pendukung untuk menyesuaikan dengan rilis PHP versi terbaru di *server*.

## Perfective
6. Menambahkan fitur pencarian buku menggunakan filter lanjutan (berdasarkan nama penulis, tahun terbit, dan kategori) agar anggota lebih mudah menemukan buku.
7. Mengoptimalkan *query database* pada halaman *dashboard* admin agar waktu muat (*loading*) data statistik bulanan menjadi lebih cepat.
8. Menambahkan fitur notifikasi email atau WhatsApp otomatis pada H-1 sebelum masa peminjaman buku anggota berakhir.

## Preventive
9. Melakukan *refactoring* pada kode *Controller* untuk transaksi peminjaman agar fungsi-fungsinya lebih modular, tidak menumpuk di satu *class*, dan lebih mudah dikembangkan.
10. Menambahkan *unit testing* (*White-box testing*) secara komprehensif pada modul perhitungan denda untuk mencegah regresi atau *error* logika di pembaruan sistem masa depan.