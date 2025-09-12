# Clone X

[![Laravel](https://img.shields.io/badge/Laravel-12-red?logo=laravel)](https://laravel.com/)
[![Nuxt](https://img.shields.io/badge/Nuxt-4-green?logo=nuxt.js)](https://nuxt.com/)
[![TailwindCSS](https://img.shields.io/badge/TailwindCSS-4-blue?logo=tailwind-css)](https://tailwindcss.com/)
[![Docker](https://img.shields.io/badge/Docker-✓-2496ED?logo=docker)](https://www.docker.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A **full-stack X clone** built with **Laravel 12**, **Nuxt 4**, **TailwindCSS 4**, **MySQL**, **Redis**, and **Docker**, structured as a **monorepo**.

---

## 📂 Project Structure

CloneX/
├── laravel/ # Backend (Laravel 12 API)
├── nuxt/ # Frontend (Nuxt 4 + TailwindCSS)
└── docker/ # Docker setup (MySQL, Redis, PHP, Node)


---

## 🚀 Features
- RESTful API built with Laravel 12
- Authentication with Laravel Sanctum
- Role & Permission system (Spatie)
- Nuxt 4 frontend with TailwindCSS UI
- Pinia for state management
- Axios for API communication
- Docker Compose for local environment
- MySQL database with Redis cache
- Code linting & formatting (Pint, ESLint, Prettier)
- Unit & integration testing setup

---

## 🛠️ Tech Stack

### Backend (Laravel)
- Laravel 12
- Laravel Sanctum (API authentication)
- Spatie Laravel Permission (roles & permissions)
- Laravel Telescope (debugging)
- Laravel Horizon (queues with Redis)
- Laravel Pint (code style)
- PHPUnit (tests)

### Frontend (Nuxt)
- Nuxt 4
- Pinia (state management)
- Axios (API requests)
- TailwindCSS 4 + plugins (`forms`, `typography`, `aspect-ratio`)
- Heroicons / Lucide icons
- ESLint + Prettier (code style)
- Vitest (tests)

### Infrastructure
- Docker & Docker Compose
- MySQL (database)
- Redis (cache & queues)

---

## ⚡ Installation

Clone the repository:

```bash
git clone https://github.com/your-username/clone-x.git
cd clone-x

## ⚡ Start services with Docker Compose:

docker-compose up -d


Backend will be available at: http://localhost:8000
Frontend will be available at: http://localhost:3000

⚙️ Configuration

Copy .env.example to .env inside both /laravel and /nuxt.

Update environment variables as needed (database, API URLs).

Database credentials are defined in docker-compose.yml.

📜 License

This project is licensed under the MIT License.
