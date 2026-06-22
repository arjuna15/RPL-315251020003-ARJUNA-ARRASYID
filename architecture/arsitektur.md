# Arsitektur Perangkat Lunak

**Pola Arsitektur:** Layered Architecture dengan pola **MVC (Model-View-Controller)**.

**Alasan Pemilihan:**
Pola MVC sangat cocok untuk Sistem Manajemen Perpustakaan berbasis *web* (seperti pengembangan dengan *framework* Laravel). Pola ini memisahkan secara jelas antara tiga lapisan:
- **Model:** Menangani logika data dan interaksi langsung dengan *database* (misal: data Buku, data Anggota).
- **View:** Menangani antarmuka pengguna (UI) yang dirender ke *browser*.
- **Controller:** Bertindak sebagai penghubung (*middleware/logic handler*), menerima *request* dari *View*, memproses aturan bisnis perpustakaan, lalu mengambil/menyimpan data melalui *Model*.

Pemisahan ini membuat sistem memiliki tingkat *Maintainability* yang tinggi karena *developer* dapat mengubah tampilan UI (*View*) tanpa merusak logika data (*Model*).