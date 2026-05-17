# LexSys PMS — Project Management System

> A web-based Project Management System built for **Lexsys Technologies Incorporated**, powered by Laravel, React (Inertia.js), and PostgreSQL.

---

## Tech Stack

| Layer | Technology |
|-------|------------|
| Backend | Laravel 12 |
| Frontend | React + TypeScript (via Inertia.js) |
| Database | PostgreSQL |
| Auth | Laravel Breeze (React) |
| Build Tool | Vite |
| Package Manager | Composer + npm |

---

## Prerequisites

Make sure the following are installed on your machine:

- PHP >= 8.2
- Composer
- Node.js >= 18.x & npm
- PostgreSQL >= 14
- Git

---

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-org/lexsys-pms.git
cd lexsys-pms
```

### 2. Install PHP Dependencies

```bash
composer install
```

### 3. Install Node Dependencies

```bash
npm install
```

### 4. Environment Setup

```bash
cp .env.example .env
php artisan key:generate
```

### 5. Configure the Database

Open `.env` and update the PostgreSQL credentials:

```env
DB_CONNECTION=pgsql
DB_HOST=127.0.0.1
DB_PORT=5432
DB_DATABASE=lexsys_pms
DB_USERNAME=postgres
DB_PASSWORD=your_db_password
```

### 6. Run Migrations

```bash
php artisan migrate
```

> If you encounter a `sessions table does not exist` error, run:
> ```bash
> php artisan session:table
> php artisan migrate
> ```

### 7. (Optional) Seed the Database

```bash
php artisan db:seed
```

---

## Running the Application

You need **two terminals** running simultaneously:

**Terminal 1 — Laravel Backend**
```bash
php artisan serve
```

**Terminal 2 — Vite Frontend**
```bash
npm run dev
```

Then open your browser at: [http://localhost:8000](http://localhost:8000)

---

## Building for Production

```bash
npm run build
php artisan optimize
```

---

## Common Artisan Commands

```bash
# Clear all caches
php artisan optimize:clear

# Run migrations fresh (resets all data)
php artisan migrate:fresh --seed

# Check migration status
php artisan migrate:status
```

---

## Environment Variables Reference

| Variable | Description |
|----------|-------------|
| `APP_NAME` | Application name |
| `APP_ENV` | `local` / `production` |
| `APP_URL` | Base URL of the application |
| `DB_CONNECTION` | Set to `pgsql` |
| `DB_HOST` | PostgreSQL host |
| `DB_PORT` | PostgreSQL port (default: `5432`) |
| `DB_DATABASE` | Database name |
| `DB_USERNAME` | Database username |
| `DB_PASSWORD` | Database password |
| `SESSION_DRIVER` | Set to `database` or `file` |

---

## License

This project is proprietary software owned by **Lexsys Technologies Incorporated**. All rights reserved.
