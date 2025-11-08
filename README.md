# 🚀 Laravel, PHP & GitHub Full Web App Development Command Cheat Sheet

> **Note:** Lahat ng commands na may kinalaman sa pag-develop ng web app gamit ang Laravel at PHP, kasama ang version control sa Git/GitHub. May kasamang usage notes at placeholders kung saan papalitan.

## 🧱 1. Installation & Setup

```bash
# Install Laravel globally
composer global require laravel/installer

# Create new Laravel project (replace 'project_name')
laravel new project_name

# OR without installer
composer create-project --prefer-dist laravel/laravel project_name

# Run local development server (default port 8000)
php artisan serve

# Check Laravel version
php artisan --version

# Check PHP version
php -v
```

**Usage:** Installation at initial setup ng project.

---

## ⚙️ 2. Environment Setup

```bash
# Copy environment file
cp .env.example .env

# Generate new application key (encryption)
php artisan key:generate

# Optimize application for production
php artisan optimize
php artisan config:cache
php artisan route:cache
php artisan view:cache
php artisan event:cache

# Clear all caches (use while debugging)
php artisan cache:clear
php artisan config:clear
php artisan route:clear
php artisan view:clear
php artisan event:clear
```

**Usage:** Prepares environment, clears or caches config and routes.

---

## 🗃️ 3. Database & Migrations

```bash
# Create migration (replace table name)
php artisan make:migration create_users_table

# Run all migrations
php artisan migrate

# Rollback last batch
php artisan migrate:rollback

# Reset all migrations
php artisan migrate:reset

# Refresh migrations
php artisan migrate:refresh

# Re-run all migrations with seeders
php artisan migrate:fresh --seed

# Seed database (change seeder name)
php artisan db:seed --class=UserSeeder
```

**Usage:** Database schema management at development and production.

---

## 🧩 4. Models, Controllers, Factories, Seeders

```bash
# Create model (replace 'Product')
php artisan make:model Product

# Create model with migration
php artisan make:model Product -m

# Create model, controller, migration, factory, seeder
php artisan make:model Product -mcrsf

# Create controller (replace name)
php artisan make:controller ProductController

# Create resource controller (CRUD)
php artisan make:controller ProductController --resource

# Create factory (replace name)
php artisan make:factory ProductFactory

# Create seeder (replace name)
php artisan make:seeder ProductSeeder
```

**Usage:** Generates backend classes for data management.

---

## 🧾 5. Requests, Middleware, Policies, Providers

```bash
# Form request (replace name)
php artisan make:request StoreProductRequest

# Middleware (replace name)
php artisan make:middleware CheckUserRole

# Policy (replace name)
php artisan make:policy ProductPolicy

# Service provider (replace name)
php artisan make:provider CustomServiceProvider
```

**Usage:** Handles input validation, authorization, and custom services.

---

## 🌐 6. Routes & API

```bash
# Show all routes
php artisan route:list

# Cache routes
php artisan route:cache

# Clear route cache
php artisan route:clear
```

**Usage:** API and web route management.

---

## 🔐 7. Authentication (Breeze / Jetstream / Fortify / UI)

```bash
# Laravel Breeze (Blade auth)
composer require laravel/breeze --dev
php artisan breeze:install
npm install && npm run dev

# Jetstream (Livewire/Inertia)
composer require laravel/jetstream
php artisan jetstream:install livewire
npm install && npm run build

# Fortify (backend auth)
composer require laravel/fortify
php artisan vendor:publish --provider="Laravel\Fortify\FortifyServiceProvider"

# Laravel UI (Bootstrap/Vue/React auth)
composer require laravel/ui
php artisan ui bootstrap --auth
npm install && npm run dev
```

**Usage:** Setup authentication scaffolding for web apps.

---

## 🧪 8. PHP & Artisan Helpers

```bash
# PHP built-in server (replace port if needed)
php -S localhost:8000 -t public

# Interactive shell (Tinker)
php artisan tinker

# Run all tests
php artisan test
```

**Usage:** PHP dev tools and Laravel testing.

---

## 🧰 9. Git & GitHub

```bash
# Initialize git repository
git init

# Check status
git status

# Stage changes
git add .

# Commit changes
git commit -m "Your commit message"

# Add remote repository (replace URL)
git remote add origin https://github.com/username/repo.git

# Push changes
git push -u origin main

# Pull updates
git pull origin main

# Create and switch branch (replace name)
git checkout -b feature-branch

# Switch branch
git checkout main

# Merge branch
git merge feature-branch

# View git log
git log

# Fetch updates
git fetch origin

# Reset branch to remote state
git reset --hard origin/main
```

**Usage:** Version control, collaboration, GitHub sync.

---

## ✅ Quick Start Workflow (Web App Dev + GitHub)

```bash
composer create-project laravel/laravel myapp
cd myapp
cp .env.example .env
php artisan key:generate
php artisan migrate
php -v
php artisan serve
git init
git add .
git commit -m "Initial Laravel setup"
git remote add origin https://github.com/username/repo.git
git push -u origin main
```

**Usage:** Setup Laravel web app, run server, push to GitHub.

---

🧾 *Updated: 2025 — Complete Laravel + PHP + GitHub Web App Development Command Reference with Usage Notes*
