# 📊 Implementasi Human-Computer Interaction & Data Visualization

Aplikasi web berbasis **Laravel** yang menerapkan prinsip *Human-Computer Interaction* (HCI) dan visualisasi data. Proyek ini memiliki fitur autentikasi serta pengelolaan data (misalnya data keuangan, gaji, dan karyawan) yang disajikan melalui antarmuka yang mudah digunakan.

## ✨ Fitur

- Autentikasi pengguna (login, registrasi, logout).
- Pengelolaan data (CRUD) untuk berbagai modul.
- Visualisasi data dalam bentuk grafik dan tabel.
- Antarmuka responsif dengan Vite dan Tailwind CSS.

> Sesuaikan daftar fitur di atas dengan modul yang benar-benar ada di aplikasi.

## 🛠️ Teknologi

- [Laravel](https://laravel.com/) (PHP 8.2+)
- MySQL
- [Vite](https://vitejs.dev/)
- [Tailwind CSS](https://tailwindcss.com/)
- Node.js & npm
- Composer

## ✅ Prasyarat

Pastikan sudah terpasang:

- PHP 8.2 atau lebih baru
- Composer
- Node.js 18 atau lebih baru dan npm
- MySQL (XAMPP atau Laragon)

Cek versi dengan:

```bash
php -v
composer -V
node -v
npm -v
```

## 🚀 Instalasi

1. **Clone repositori**

   ```bash
   git clone https://github.com/<username>/Implementasi-Human-Computer-Interaction-Data-Visualization.git
   cd Implementasi-Human-Computer-Interaction-Data-Visualization
   ```

2. **Install dependensi PHP**

   ```bash
   composer install
   ```

3. **Install dependensi frontend**

   ```bash
   npm install
   ```

4. **Siapkan file environment**

   Windows (PowerShell):

   ```powershell
   copy .env.example .env
   ```

   Linux / macOS:

   ```bash
   cp .env.example .env
   ```

5. **Generate application key**

   ```bash
   php artisan key:generate
   ```

6. **Atur database**

   Buat database baru di MySQL, misalnya `implementasi_ai`, lalu sesuaikan di file `.env`:

   ```env
   DB_CONNECTION=mysql
   DB_HOST=127.0.0.1
   DB_PORT=3306
   DB_DATABASE=implementasi_ai
   DB_USERNAME=root
   DB_PASSWORD=
   ```

7. **Jalankan migrasi dan seeder**

   ```bash
   php artisan migrate --seed
   ```

   Untuk mengulang dari awal (semua data akan terhapus):

   ```bash
   php artisan migrate:fresh --seed
   ```

## ▶️ Menjalankan Aplikasi

Buka dua terminal:

```bash
# Terminal 1 - server Laravel
php artisan serve
```

```bash
# Terminal 2 - frontend (Vite)
npm run dev
```

Lalu buka `http://127.0.0.1:8000` di browser.

Untuk build produksi:

```bash
npm run build
```

## 📁 Struktur Folder

```
.
├── app/            # Logika aplikasi (controller, model, dll.)
├── bootstrap/      # Bootstrap framework
├── config/         # Konfigurasi aplikasi
├── database/       # Migrasi, factory, dan seeder
├── public/         # Entry point dan aset publik
├── resources/      # View, CSS, dan JavaScript
├── routes/         # Definisi route (web, auth, console)
├── storage/        # Log, cache, dan file upload
├── artisan         # CLI Laravel
├── composer.json   # Dependensi PHP
└── package.json    # Dependensi frontend
```

## 🔧 Troubleshooting

| Masalah | Solusi |
|---|---|
| `Could not open input file: artisan` | Pastikan terminal berada di folder yang berisi file `artisan`. |
| `bootstrap/cache directory must be present and writable` | Buat folder `bootstrap/cache` dan pastikan bisa ditulis. |
| `No application encryption key has been specified` | Jalankan `php artisan key:generate`. |
| `Table ... already exists` | Jalankan `php artisan migrate:fresh --seed`. |
| Tampilan tanpa CSS | Pastikan `npm run dev` sedang berjalan. |
| Perubahan `.env` tidak terbaca | Jalankan `php artisan config:clear`. |

## 🔒 Catatan Keamanan

- File `.env` **tidak** disertakan di repositori. Gunakan `.env.example` sebagai acuan.
- Jangan membagikan `APP_KEY`, password database, atau kredensial lain ke publik.

## 👤 Penulis

- Nama: _isi nama kamu_
- GitHub: [@Gellael](https://github.com/gellael)

## 📄 Lisensi

Proyek ini dibuat untuk keperluan pembelajaran.