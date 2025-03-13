# 🚀 Laravel 10 + Vue 3 + Docker + MySQL 8 + Pinia + Redis + RabbitMQ + Pest + Vitest

![Laravel](https://img.shields.io/badge/Laravel-10-red?style=for-the-badge&logo=laravel) ![Vue](https://img.shields.io/badge/Vue-3-green?style=for-the-badge&logo=vue.js) ![Docker](https://img.shields.io/badge/Docker-blue?style=for-the-badge&logo=docker) ![MySQL](https://img.shields.io/badge/MySQL-8-4479A1?style=for-the-badge&logo=mysql) ![Redis](https://img.shields.io/badge/Redis-red?style=for-the-badge&logo=redis) ![RabbitMQ](https://img.shields.io/badge/RabbitMQ-orange?style=for-the-badge&logo=rabbitmq) ![Pest](https://img.shields.io/badge/Pest-Testing-purple?style=for-the-badge&logo=php) ![Vitest](https://img.shields.io/badge/Vitest-Unit--Test-green?style=for-the-badge&logo=vitest)

## 📌 Описание
Этот проект использует **Laravel 10** в качестве backend-фреймворка и **Vue 3** для frontend-разработки. Вся инфраструктура развёрнута в **Docker** и включает **MySQL 8**, **Redis**, **RabbitMQ** для очередей, а также тестирование с **Pest** и **Vitest**.

---

## ⚡️ Быстрый старт
### 📌 Требования
Перед установкой убедись, что у тебя установлены:
- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)
- [Node.js 16+](https://nodejs.org/)
- [Composer](https://getcomposer.org/)

### 🔥 Установка и запуск

1. **Клонируй репозиторий**
```sh
 git clone https://github.com/your-repo.git
 cd your-repo
```

2. **Запусти контейнеры**
```sh
 cp .env.example .env
 docker-compose up -d --build
```

3. **Установи зависимости Laravel**
```sh
 docker-compose exec app composer install
 docker-compose exec app php artisan key:generate
```

4. **Запусти миграции и посев данных**
```sh
 docker-compose exec app php artisan migrate --seed
```

5. **Установи зависимости Vue**
```sh
 cd frontend
 npm install
```

6. **Запусти фронтенд**
```sh
 npm run dev
```

---

## 📦 Структура проекта
```plaintext
📦 project-root
├── 📂 backend (Laravel API)
│   ├── 📂 app
│   ├── 📂 database
│   ├── 📂 routes
│   └── 📄 artisan
├── 📂 frontend (Vue 3 + Vite)
│   ├── 📂 src
│   ├── 📂 components
│   ├── 📂 store (Pinia)
│   ├── 📂 views
│   ├── 📄 main.js
│   └── 📄 App.vue
├── 📄 docker-compose.yml
├── 📄 package.json
└── 📄 README.md
```

---

## 🐳 Docker Контейнеры
| Сервис     | Описание          | Порт  |
|------------|------------------|-------|
| **App**    | Laravel Backend  | 8000  |
| **Vue**    | Vue 3 Frontend   | 5173  |
| **MySQL**  | База данных      | 3306  |
| **Redis**  | Кеширование      | 6379  |
| **RabbitMQ** | Очереди         | 5672  |

---

## 🎯 Тестирование

### 🧪 Тесты Laravel (Pest)
```sh
 docker-compose exec app php artisan test
```

### ⚡️ Тесты Vue (Vitest)
```sh
 cd frontend
 npm run test
```

---

## 🚀 Полезные команды
### 🎯 Laravel
```sh
 docker-compose exec app php artisan migrate
 docker-compose exec app php artisan db:seed
 docker-compose exec app php artisan queue:work
```

### 🛠 Docker
```sh
 docker-compose up -d --build  # Пересборка контейнеров
 docker-compose down           # Остановка всех сервисов
```

### 🌍 Запуск фронтенда
```sh
 cd frontend
 npm run dev
```

---

## 💡 TODO
✅ Настроить API авторизации Laravel Sanctum
✅ Настроить очереди с RabbitMQ
✅ Добавить unit-тесты
⏳ Оптимизировать Dockerfile

---

## 📜 Лицензия
Этот проект распространяется под лицензией **MIT**.

---

### 💬 Обратная связь
Если у тебя есть предложения или вопросы, открывай [Issue](https://github.com/your-repo/issues) или пиши мне! 🚀

