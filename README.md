# Chat App

This project is built with **Laravel Filament** + **Wirechat** - a powerful combination for creating modern chat applications with real-time messaging capabilities.

## About This Project

This chat application leverages the power of Laravel Filament for admin panel functionality and Wirechat for real-time chat features. Wirechat is a Laravel Livewire chat package that brings real-time private & group communication to your application.

## Wirechat Package

This project uses [Wirechat](https://github.com/namumakwembo/wirechat) - a powerful Laravel Livewire chat application package that brings real-time private & group communication to your application. With embeddable components, it seamlessly integrates into your project, providing a feature-rich chat experience for your users.

## 🚀 Installation

### 1. Clone the Repository
```bash
git clone https://github.com/SeptiawanAjiP/laravel-chat-app
cd laravel-chat-app
```

### 2. Install Dependencies
```bash
# Install PHP dependencies
composer install

# Install Node.js dependencies
npm install
```

### 3. Environment Setup
```bash
# Copy environment file
cp .env.example .env

# Generate application key
php artisan key:generate
```

### 4. Database Configuration
Update your `.env` file with database credentials:
```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=chat_app
DB_USERNAME=your_username
DB_PASSWORD=your_password
```

### 5. Run Migrations
```bash
php artisan migrate
```

### 6. Storage Setup
```bash
# Create storage link for file uploads
php artisan storage:link
```

### 7. Build Assets
```bash
# Development
npm run dev

# Production
npm run build
```

## 🏃‍♂️ Running the Application

### Development Mode
Use the convenient development script that runs all services concurrently:
```bash
composer run dev
```

This command starts:
- Laravel development server (port 8000)
- Queue worker for real-time messaging
- Log monitoring with Pail
- Vite development server for hot reloading

### Manual Setup
Alternatively, run each service separately:
```bash
# Terminal 1: Start Laravel server
php artisan serve

# Terminal 2: Start queue worker
php artisan queue:work

# Terminal 3: Start Vite dev server
npm run dev
```