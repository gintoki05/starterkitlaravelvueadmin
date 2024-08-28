# Laravel Vue Admin Dashboard Starter Kit

Sebuah starter kit modern untuk membangun admin dashboard menggunakan Laravel, Vue.js, dan shadcn/vue.

## Fitur

- 🛠️ Laravel 11.x
- ⚡ Vue 3 dengan Composition API
- 🎨 shadcn/vue untuk komponen UI yang konsisten dan mudah dikustomisasi
- 🔒 Autentikasi pengguna bawaan
- 📊 Layout dashboard yang responsif
- 🌓 Mode gelap/terang (Soon)
- 🚀 Vite untuk pengembangan yang cepat

## Prasyarat

- PHP 8.1+
- Composer
- Node.js 16+
- npm atau yarn

## Instalasi

1. Clone repositori ini:
git clone https://github.com/username/laravel-vue-admin-dashboard.git
Copy
2. Pindah ke direktori proyek:
cd laravel-vue-admin-dashboard
Copy
3. Instal dependensi PHP:
composer install
Copy
4. Instal dependensi JavaScript:
npm install
Copy
5. Salin file `.env.example` menjadi `.env` dan sesuaikan konfigurasi database:
cp .env.example .env
Copy
6. Generate kunci aplikasi:
php artisan key:generate
Copy
7. Jalankan migrasi database:
php artisan migrate
Copy
8. Kompilasi aset:
npm run dev
Copy
## Penggunaan

1. Jalankan server pengembangan Laravel:
php artisan serve
Copy
2. Dalam terminal terpisah, jalankan Vite untuk hot-reloading:
npm run dev
Copy
3. Buka browser dan akses `http://localhost:8000`

## Struktur Proyek

- `app/` - Logika backend Laravel
- `resources/js/` - Komponen Vue dan logika frontend
- `resources/views/` - Template Blade Laravel
- `routes/` - Definisi rute Laravel
- `public/` - Aset publik

## Kustomisasi

- Komponen shadcn/vue dapat dikustomisasi di `resources/js/components/ui/`
- Tema dapat diubah di `resources/js/lib/utils.ts`

## Kontribusi

Kontribusi selalu diterima! Silakan buka issue atau submit pull request.

## Lisensi

[MIT License](LICENSE.md)

## Kredit

Starter kit ini terinspirasi oleh komunitas Laravel dan Vue.js, serta proyek shadcn/ui.
