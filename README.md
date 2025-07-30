# 💬 Laravel Chat App

Aplikasi chat real-time yang dibangun dengan **Laravel Filament** + **[Wirechat](https://github.com/namumakwembo/wirechat)** - kombinasi yang powerful untuk membuat aplikasi chat modern dengan kemampuan messaging real-time. [Wirechat](https://github.com/namumakwembo/wirechat) adalah package Laravel Livewire yang membawa komunikasi private & group real-time ke aplikasi Anda.

## 🛠️ Teknologi yang Digunakan

- **Laravel 12** - PHP Framework
- **Laravel Filament 3.3** - Admin Panel
- **Wirechat 0.2.10** - Chat Package
- **Laravel Reverb** - WebSocket Server
- **Laravel Livewire** - Dynamic UI Components
- **MySQL** - Database

## 📋 Persyaratan Sistem

- **PHP** >= 8.2
- **Composer** >= 2.0
- **Node.js** >= 18.0
- **NPM** >= 9.0
- **MySQL** >= 8.0 atau **PostgreSQL** >= 13

## 🚀 Instalasi

### 1. Clone Repository
```bash
git clone https://github.com/SeptiawanAjiP/laravel-chat-app
cd laravel-chat-app
```

### 2. Install Laravel
```bash
# Copy file environment
cp .env.example .env

# Install dependencies PHP
composer install

# Generate application key
php artisan key:generate

# Buat symbolic link untuk storage
php artisan storage:link

# Atur database dulu di .env (lihat konfigurasi database di bawah)

# Jalankan migrasi database
php artisan migrate

# Seed database dengan data sample
php artisan db:seed
```

### 3. Install Dependencies Frontend
```bash
# Install Node.js dependencies
npm install
```

### 4. Config Wirechat
```bash
# Install broadcasting
php artisan install:broadcasting

# Start Reverb server
php artisan reverb:start

# Start queue worker
php artisan queue:work --queue=messages,default

# Build assets
npm run dev
```

## 🏃‍♂️ Cara Menjalankan

### 1. Start Laravel Server
```bash
php artisan serve
```

### 2. Akses Admin Panel
- Buka browser dan akses: **http://127.0.0.1:8000/admin**
- Login dengan salah satu user yang ada di database
- **Email**: Lihat data email di database (tabel users)
- **Password**: `password` (default untuk semua user)

### 3. Akses Chat Interface
Setelah login ke admin panel:
- Akses: **http://127.0.0.1:8000/chats**
- Sekarang Anda sudah bisa melakukan chat!