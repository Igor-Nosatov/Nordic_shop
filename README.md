# 🚀 Laravel 10 + Vue 3 + Docker + MySQL 8 + Pinia + Redis + RabbitMQ + Pest + Vitest

![Laravel](https://img.shields.io/badge/Laravel-10-red?style=for-the-badge&logo=laravel) ![Vue](https://img.shields.io/badge/Vue-3-green?style=for-the-badge&logo=vue.js) ![Docker](https://img.shields.io/badge/Docker-blue?style=for-the-badge&logo=docker) ![MySQL](https://img.shields.io/badge/MySQL-8-4479A1?style=for-the-badge&logo=mysql) ![Redis](https://img.shields.io/badge/Redis-red?style=for-the-badge&logo=redis) ![RabbitMQ](https://img.shields.io/badge/RabbitMQ-orange?style=for-the-badge&logo=rabbitmq) ![Pest](https://img.shields.io/badge/Pest-Testing-purple?style=for-the-badge&logo=php) ![Vitest](https://img.shields.io/badge/Vitest-Unit--Test-green?style=for-the-badge&logo=vitest)

Here’s the translated version with all symbols preserved:

---

## 📌 Description
This project uses **Laravel 10** as the backend framework and **Vue 3** for frontend development. The entire infrastructure is deployed in **Docker** and includes **MySQL 8**, **Redis**, **RabbitMQ** for queues, as well as testing with **Pest** and **Vitest**.

---

## ⚡️ Quick Start
### 📌 Requirements
Before installation, ensure you have the following installed:
- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)
- [Node.js 16+](https://nodejs.org/)
- [Composer](https://getcomposer.org/)

### 🔥 Installation and Launch

1. **Clone the repository**
```sh
 git clone https://github.com/your-repo.git
 cd your-repo
```

2. **Start the containers**
```sh
 cp .env.example .env
 docker-compose up -d --build
```

3. **Install Laravel dependencies**
```sh
 docker-compose exec app composer install
 docker-compose exec app php artisan key:generate
```

4. **Run migrations and seed data**
```sh
 docker-compose exec app php artisan migrate --seed
```

5. **Install Vue dependencies**
```sh
 cd frontend
 npm install
```

6. **Launch the frontend**
```sh
 npm run dev
```


Here’s the translated version with all symbols preserved:

---

## 📦 Project Structure
```
📦 project-root
├── 📂 app               # Core Laravel logic
├── 📂 bootstrap         # Framework bootstrap
├── 📂 config            # Configuration files
├── 📂 data              # Temporary data
├── 📂 database          # Migrations and seed files
├── 📂 docker            # Docker files
├── 📂 public            # Public files
├── 📂 resources         # Laravel resources (including Vue)
│   ├── 📂 js            # Vue source files
│   │   ├── 📂 node_modules # Installed npm packages
│   │   ├── 📂 public        # Compiled files
│   │   ├── 📂 src           # Main code
│   │   │   ├── 📂 assets       # Styles and images
│   │   │   ├── 📂 config       # Configurations
│   │   │   ├── 📂 layouts      # Shared layouts
│   │   │   ├── 📂 modules      # Logical modules
│   │   │   │   ├── 📂 auth         # Authentication
│   │   │   │   │   ├── 📂 composables  # Authentication components
│   │   │   │   │   ├── 📂 enums        # Enumerations
│   │   │   │   │   ├── 📂 pages        # Pages
│   │   │   │   │   ├── 📂 services     # Services
│   │   │   │   │   ├── 📂 store        # Store (Pinia)
│   │   │   │   │   ├── 📂 types        # Data types
│   │   │   │   │   ├── 📂 utils        # Utilities
│   │   │   │   │   ├── 📂 validation   # Validation
│   │   │   ├── 📂 routing      # Routing
│   │   │   ├── 📂 styles       # Global styles
│   │   │   ├── 📂 tests        # Tests (Vitest)
│   │   │   ├── 📄 App.vue      # Main component
│   │   │   ├── 📄 main.ts      # Vue entry point
│   │   │   ├── 📄 shims-vue.d.ts # TypeScript settings
│   │   │   ├── 📄 vite-env.d.ts  # TypeScript configuration
│   │   ├── 📄 .env           # Environment variables
├── 📂 routes           # Laravel web routes
├── 📂 storage          # Logs and cache
├── 📂 tests            # Laravel tests
├── 📂 vendor           # Composer dependencies
├── 📄 docker-compose.yml # Docker configuration
├── 📄 package.json     # npm dependencies
└── 📄 README.md        # This file 😊
```
---

## 🐳 Docker Containers
| Service      | Description          | Port  |
|-------------|----------------------|-------|
| **App**     | Laravel Backend      | 8000  |
| **Vue**     | Vue 3 Frontend       | 5173  |
| **MySQL**   | Database             | 3306  |
| **Redis**   | Caching              | 6379  |
| **RabbitMQ**| Queues               | 5672  |
| **Mailpit** | Test email           | 8025  |

---

## 🎯 Testing

### 🧪 Laravel Tests (Pest)
```sh
 docker-compose exec app php artisan test
```

### ⚡️ Vue Tests (Vitest)
```sh
 cd frontend
 npm run test
```

---

## 🚀 Useful Commands
### 🎯 Laravel
```sh
 docker-compose exec app php artisan migrate
 docker-compose exec app php artisan db:seed
 docker-compose exec app php artisan horizon
 docker-compose exec app php artisan queue:work
```

### 🛠 Docker
```sh
 docker-compose up -d --build  # Rebuild containers
 docker-compose down           # Stop all services
```

### 🌍 Launch Frontend
```sh
 cd frontend
 npm run dev
```

---

## 💡 Used Packages
### Backend (Laravel)
- **Swagger** for API documentation
- **Sanctum** for authentication
- **Horizon** for queue management
- **Telescope** for monitoring
- **RabbitMQ** for queues
- **Predis** for Redis integration
- **PayPal / Stripe** for payments

### Frontend (Vue 3)
- **Pinia + Persisted State**
- **Vue Router**
- **VeeValidate + Zod** for validation
- **Vue Chart.js** for charts
- **SweetAlert2** for notifications

---

## 📜 License
This project is distributed under the **MIT** license.
