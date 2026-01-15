**PROJECT PENGEMBANGAN BACKEND** 
Nama anggota:
    - I Gusti Agung Ayu Eka Santri (230030474)
    - Komang Wanda Dewanti Putri (240030326)

# Kalkulator Online
Proyek ini adalah aplikasi Kalkulator Online berbasis web yang terinpirasi dari desain iOS dengan fungsionalitas sistem manajemen database. 
Aplikasi ini dirancang untuk melakukan perhitungan matematika harian sekaligus mendokumentasikan setiap aktivitas perhitungan secara otomatis ke dalam sistem penyimpanan.

## Fitur Utama
- **Tampilan iPhone Style**  
  Desain modern dengan tombol bulat dan warna yang menyerupai kalkulator iOS.

- **Mode Terang & Gelap**  
  Pengguna dapat mengganti tema Light/Dark melalui menu dropdown.

- **Riwayat Perhitungan**  
  Setiap operasi yang dilakukan akan otomatis tersimpan ke database.

- **Histori dalam Modal**  
  Menampilkan hingga 10 riwayat perhitungan terakhir langsung di dalam aplikasi.

- **Pengolahan Input Lebih Rapi**  
  Logika input angka, nol, dan tanda kurung diatur agar hasil perhitungan lebih konsisten dan nyaman digunakan.

## Teknologi yang Digunakan
- **Frontend**: HTML5, CSS3 (Flexbox & Grid), JavaScript (Vanilla)
- **Backend**: PHP
- **Database**: MySQL
- **Ikon**: Font Awesome 6

## Struktur Folder
Projek kalkulator online/
├── actions/
    ├── calculate.php      # Proses perhitungan di sisi server
   └── get_history.php    # Mengambil data riwayat dari database
├── assets/
  ├── css/
│   │   └── style.css      # Styling untuk UI & pengaturan tema
│   └── js/
│       └── script.js      # Logika kalkulator dan interaksi pengguna
├── config/
│   └── database.php       # Konfigurasi koneksi database
├── index.php              # Halaman utama aplikasi
└── process.php            # Proses penyimpanan data ke database


## Cara Instalasi
1. **Membuat Database**
   * Buka phpMyAdmin.
   * Buat database baru dengan nama `db_kalkulator`.
   * Menjalankan query berikut untuk membuat tabel riwayat:

   sql:
   CREATE TABLE history (
       id INT AUTO_INCREMENT PRIMARY KEY,
       operation VARCHAR(255) NOT NULL,
       result VARCHAR(255) NOT NULL,
       created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
   );

2. **Konfigurasi Database**
   * Buka file `config/database.php`.
   * Sesuaikan username, password, dan nama database dengan server lokal (XAMPP atau Laragon).

3. **Menjalankan Aplikasi**
   * Pindahkan folder proyek ke dalam folder `htdocs` (XAMPP) atau `www` (Laragon).
   * Jalankan aplikasi melalui browser:
     http://localhost/Projek_kalkulator_online/
     
4. **Instruksi Penggunaan**
   Agar aplikasi berjalan optimal dan hasil perhitungan akurat secara matematis, harap diperhatikan panduan berikut:
    * Input Angka: Masukkan angka secara langsung tanpa tanda titik sebagai pemisah ribuan (Contoh: tulis 700000, bukan 700.000).
    * Fungsi Titik: Tombol titik pada kalkulator ini berfungsi murni sebagai Pemisah Desimal (Koma) sesuai standar bahasa pemrograman JavaScript.
    * Urutan Operasi: Gunakan tanda kurung ( ) untuk memprioritaskan operasi matematika tertentu.
  
**Karena berbarengan dengan tenggat mata kuliah lain, tim kami memilih fokus pada pengembangan fungsionalitas teknis aplikasi. Seluruh koordinasi dilakukan secara daring, dan dokumentasi ini berisi ringkasan poin penting dari hasil kerja tim agar proyek tetap selesai tepat waktu**


