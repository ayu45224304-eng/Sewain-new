# Panduan Proyek Sewain

## Gambaran Umum

Sewain adalah aplikasi admin berbasis Streamlit untuk mengelola inventaris,
peminjaman, pengembalian, riwayat, dan laporan UKM.

## Struktur dan Pola

- `app.py` mengatur konfigurasi Streamlit dan navigasi halaman.
- `core/` berisi akses database, migrasi skema, gaya, dan utilitas bersama.
- `views/` berisi tampilan dan alur fitur aplikasi.
- `sqlite/invenukm.db` adalah database SQLite yang digunakan aplikasi.
- Jika database lama ada di `data/invenukm.db`, aplikasi menyalinnya ke lokasi
  baru saat pertama kali dijalankan; database lama tidak dihapus.
- Gunakan fungsi dan pola yang sudah ada di `core/db.py` saat mengakses data.
- Gunakan query berparameter untuk nilai dinamis SQL.
- Jangan menghapus atau mengganti database pengguna saat mengubah skema.

## Menjalankan Aplikasi

Instal dependensi dengan `python -m pip install -r requirements.txt`, lalu
jalankan `streamlit run app.py`.

## Validasi

Setelah mengubah kode, jalankan pemeriksaan atau pengujian yang relevan.
Pastikan alur inventaris, peminjaman, pengembalian, dan laporan tetap berjalan.
