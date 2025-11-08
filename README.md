# 🚀 Laravel & GitHub Complete Command Cheat Sheet (All-in-One)

## 🧱 1. Installation & Setup

```bash
# Install Laravel globally
composer global require laravel/installer

# Create new Laravel project
laravel new project_name

# OR without installer
composer create-project --prefer-dist laravel/laravel project_name

# Run local development server
php artisan serve

# Check Laravel version
php artisan --version
```

---

## ⚙️ 2. Environment Setup

```bash
# Copy .env file
cp .env.example .env

# Generate new app key
php artisan key:generate

# Clear and rebuild caches
php artisan optimize
php artisan config:cache
php artisan route:cache
php artisan view:cache
php artisan event:cache

# Clear caches
php artisan cache:clear
php artisan config:clear
php artisan route:clear
php artisan view:clear
php artisan event:clear

# Clear compiled classes
php artisan clear-compiled
```

---

## 🗃️ 3. Database & Migrations

```bash
# Create migration
php artisan make:migration create_users_table

# Run all migrations
php artisan migrate

# Rollback last batch
php artisan migrate:rollback

# Reset all migrations
php artisan migrate:reset

# Refresh migrations (reset + re-run)
php artisan migrate:refresh

# Re-run all with seeders
php artisan migrate:fresh --seed

# Seed database
php artisan db:seed

# Run specific seeder
php artisan db:seed --class=UserSeeder

# Check database connection
php artisan db
```

---

## 🧩 4. Models, Controllers, Factories, Seeders

```bash
# Create model
php artisan make:model Product

# Create model + migration
php artisan make:model Product -m

# Create model + controller + migration + factory + seeder
php artisan make:model Product -mcrsf

# Create controller
php artisan make:controller ProductController

# Create resource controller (CRUD)
php artisan make:controller ProductController --resource

# Create factory
php artisan make:factory ProductFactory

# Create seeder
php artisan make:seeder ProductSeeder
```

---

## 🧾 5. Requests, Middleware, Policies, Providers

```bash
# Create form request
php artisan make:request StoreProductRequest

# Create middleware
php artisan make:middleware CheckUserRole

# Create policy
php artisan make:policy ProductPolicy

# Create service provider
php artisan make:provider CustomServiceProvider
```

---

## 🌐 6. Routes & API

```bash
# Show all routes
php artisan route:list

# Cache routes for speed
php artisan route:cache

# Clear route cache
php artisan route:clear
```

---

## 🎨 7. Views (Blade)

```bash
# Laravel doesn't generate views via artisan
# Just create files under: resources/views/
# Example: resources/views/home.blade.php
```

---

## 🔐 8. Authentication (Breeze / Jetstream / Fortify / UI)

```bash
# Install Laravel Breeze (simple auth + blade)
composer require laravel/breeze --dev
php artisan breeze:install
npm install && npm run dev

# Install Jetstream (Livewire or Inertia)
composer require laravel/jetstream
php artisan jetstream:install livewire
npm install && npm run build

# Install Fortify (backend auth only)
composer require laravel/fortify
php artisan vendor:publish --provider="Laravel\Fortify\FortifyServiceProvider"

# Laravel UI (Bootstrap / Vue / React auth)
composer require laravel/ui
php artisan ui bootstrap --auth
npm install && npm run dev
```

---

## 🧠 9. Artisan Generators

```bash
# Create event
php artisan make:event UserRegistered

# Create listener
php artisan make:listener SendWelcomeEmail

# Create notification
php artisan make:notification OrderShipped

# Create mail
php artisan make:mail WelcomeMail

# Create job
php artisan make:job ProcessOrder

# Create command (console command)
php artisan make:command ImportUsers

# Create observer
php artisan make:observer ProductObserver

# Create component (for Livewire/Blade)
php artisan make:component Alert
```

---

## 🧩 10. Queues & Jobs

```bash
# Create job
php artisan make:job SendEmailJob

# Run queue worker
php artisan queue:work

# Stop queue worker
php artisan queue:restart

# Flush failed jobs
php artisan queue:flush

# Retry failed job
php artisan queue:retry all
```

---

## 🗓️ 11. Scheduling

```bash
# Run all scheduled commands
php artisan schedule:run

# Test if scheduler works
php artisan schedule:list
```

---

## 🧰 12. Events & Notifications

```bash
# Create event
php artisan make:event UserRegistered

# Create listener
php artisan make:listener SendWelcomeEmail

# Create notification
php artisan make:notification InvoicePaid
```

---

## 🧪 13. Testing

```bash
# Create test class
php artisan make:test ProductTest

# Create feature test
php artisan make:test ProductFeatureTest --unit

# Run all tests
php artisan test
```

---

## 📦 14. Composer & NPM

```bash
# Composer install/update
composer install
composer update

# Check outdated packages
composer outdated

# Remove cache
composer clear-cache

# Install npm dependencies
npm install

# Run dev build
npm run dev

# Run production build
npm run build

# Watch for frontend changes
npm run watch
```

---

## 🧱 15. Storage & File Management

```bash
# Create symbolic link (storage/public)
php artisan storage:link

# Clear storage cache
php artisan cache:clear
```

---

## ⚡ 16. Optimization

```bash
# Optimize app for production
php artisan optimize

# Cache routes, config, and views
php artisan route:cache
php artisan config:cache
php artisan view:cache

# Clear all caches
php artisan optimize:clear
```

---

## 📡 17. Deployment & Maintenance

```bash
# Put app in maintenance mode
php artisan down

# Put app in maintenance mode with message
php artisan down --message="Upgrading system" --retry=60

# Bring app back up
php artisan up

# Show optimized config
php artisan config:show
```

---

## 🧰 18. Debugging Tools

```bash
# Run Tinker (interactive shell)
php artisan tinker

# Check environment
php artisan env

# Display configuration values
php artisan config:get app.name
```

---

## 🌍 19. Localization (Languages)

```bash
# Publish lang files
php artisan lang:publish
```

---

## 📊 20. Logs

```bash
# View Laravel log
tail -f storage/logs/laravel.log
```

---

## 🧩 21. Miscellaneous

```bash
# List all artisan commands
php artisan list

# Show help for specific command
php artisan help migrate

# Display app environment
php artisan env
```

---

## 🐙 22. Git & GitHub Commands for Laravel Projects

```bash
# Initialize git repo
git init

# Check status
git status

# Stage changes
git add .

# Commit changes
git commit -m "Initial commit"

# Add remote GitHub repository
git remote add origin https://github.com/username/repo.git

# Push changes to GitHub
git push -u origin main

# Pull changes from GitHub
git pull origin main

# Create and switch branch
git checkout -b feature-branch

# Switch branch
git checkout main

# Merge branch
git merge feature-branch

# View git log
git log

# Fetch updates without merging
git fetch origin

# Reset local branch to remote state
git reset --hard origin/main
```

---

## ✅ Quick Start Workflow (Laravel + GitHub)

```bash
composer create-project laravel/laravel myapp
cd myapp
cp .env.example .env
php artisan key:generate
php artisan migrate
git init
git add .
git commit -m "Initial Laravel setup"
git remote add origin https://github.com/username/repo.git
git push -u origin main
php artisan serve
```

---

📘 **Note:**
All commands should be run from the root of your Laravel project (`cd myapp`).
For frontend (Vite, Tailwind, Vue, React), always use `npm run dev` or `npm run build`.

---

**💡 Tip:** Combine commands for faster setup

```bash
php artisan migrate:fresh --seed && php artisan serve
```

---

🧾 *Updated: 2025 — Complete Laravel + GitHub Command Reference*
