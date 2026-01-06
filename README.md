PROJECT PENGEMBANGAN BACKEND 
Nama anggota:
    - I Gusti Agung Ayu Eka Santri (230030474)
    - Komang Wanda Dewanti Putri (240030326)

# Kalkulator Online
Kelompok kami membuat kalkulator berbasis web dengan tampilan yang terinspirasi dari desain iOS. 
Aplikasi ini dibuat untuk menangani perhitungan matematika dasar hingga lanjutan, sekaligus menyimpan riwayat perhitungan ke dalam database MySQL agar bisa dilihat kembali kapan saja.

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
     


