# Physical View

Infrastruktur dari Sistem Manajemen Perpustakaan ini dirancang dengan pendekatan *Client-Server* sederhana yang di-*deploy* dalam lingkungan *cloud/VPS*:

1. **Client Node:**
   - Perangkat yang digunakan pengguna (Laptop, PC, Smartphone).
   - Menjalankan *Web Browser* (Chrome, Firefox) untuk mengakses antarmuka sistem via protokol HTTPS.

2. **Web & Application Server (Server Aplikasi):**
   - Menggunakan Nginx atau Apache.
   - Menjalankan *environment* bahasa pemrograman (misalnya PHP/Node.js) yang memproses *source code* aplikasi (*framework* MVC).

3. **Database Server (Server Basis Data):**
   - Menjalankan Relational Database Management System (RDBMS) seperti MySQL atau PostgreSQL.
   - Menyimpan seluruh tabel relasional (*Users, Books, Borrowings, Fines*).
   - Berada di jaringan privat yang hanya bisa diakses oleh *Application Server* demi keamanan.