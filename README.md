# Clone X

[![Laravel](https://img.shields.io/badge/Laravel-12-red?logo=laravel)](https://laravel.com/)
[![Nuxt](https://img.shields.io/badge/Nuxt-4-green?logo=nuxt.js)](https://nuxt.com/)
[![TailwindCSS](https://img.shields.io/badge/TailwindCSS-4-blue?logo=tailwind-css)](https://tailwindcss.com/)
[![Docker](https://img.shields.io/badge/Docker-✓-2496ED?logo=docker)](https://www.docker.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

A **full-stack X clone** built with **Laravel 12**, **Nuxt 4**, **TailwindCSS 4**, **MySQL**, **Redis**, and **Docker**, structured as a **monorepo**.

---

```bash
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

1. Clone the Repository and Start Services

Clone the repository and navigate to the project folder. The --build command ensures the environment is built from scratch, including PHP extensions.

Bash

git clone https://github.com/your-username/clone-x.git
cd clone-x
docker-compose up -d --build

2. Configure the Backend (Laravel)
Access the Laravel container to configure the application, generate the security key, and migrate the database tables.

Bash

# Copy the configuration file
cp laravel/.env.example laravel/.env

# Configuration

Copy .env.example to .env inside both /laravel and /nuxt.
Update environment variables as needed (database, API URLs).
Database credentials are defined in docker-compose.yml.

# Generate the application key and migrate tables
docker-compose exec laravel-app php artisan key:generate
docker-compose exec laravel-app php artisan migrate

3. Configure and Start the Frontend (Nuxt)
Access the Nuxt container to install dependencies and start the development server.

Bash

# Copy the configuration file
cp nuxt/.env.example nuxt/.env

# Install NPM dependencies
docker-compose exec node-app npm install

# Start the Nuxt development server
docker-compose exec node-app npm run dev --host

4. Start the Backend Server
Start the Laravel development server so the API is available.

Bash

docker-compose exec laravel-app php artisan serve --host=0.0.0.0

💻 Access the Project

After executing the commands above, you can access the application at the following addresses:

Frontend: http://localhost:3000

Backend (API): http://localhost:8000

📜 License
This project is licensed under the MIT License.







