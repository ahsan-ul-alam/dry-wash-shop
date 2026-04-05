# Belmont Dev - Laravel & React Starter Kit

A modern, full-stack web application starter kit built with Laravel 12, React 19, and Inertia.js. This project features a robust authentication system via Laravel Fortify and a polished UI using Tailwind CSS 4 and Radix UI components.

## 🚀 Tech Stack

- **Backend:** [Laravel 12](https://laravel.com) (PHP 8.2+)
- **Frontend:** [React 19](https://react.dev), [TypeScript](https://www.typescriptlang.org)
- **Bridge:** [Inertia.js](https://inertiajs.com)
- **Authentication:** [Laravel Fortify](https://laravel.com/docs/fortify)
- **Styling:** [Tailwind CSS 4](https://tailwindcss.com), [Radix UI](https://www.radix-ui.com)
- **Build Tool:** [Vite](https://vitejs.dev)
- **Testing:** [Pest PHP](https://pestphp.com)
- **Linting/Formatting:** [Laravel Pint](https://laravel.com/docs/pint), [ESLint](https://eslint.org), [Prettier](https://prettier.io)

## 📋 Prerequisites

Ensure you have the following installed on your local machine:

- PHP 8.2 or higher
- [Composer](https://getcomposer.org)
- [Node.js & npm](https://nodejs.org)
- A local database (SQLite is used by default for quick setup)

## 🛠️ Installation & Setup

1. **Clone the repository:**

    ```bash
    git clone https://github.com/ahsan-ul-alam/dry-wash-shop.git
    cd dry-wash-shop
    ```

2. **Run the automated setup:**
   This command installs PHP/JS dependencies, sets up your `.env` file, generates an app key, and runs migrations.

    ```bash
    composer run setup
    ```

3. **Alternative Manual Setup:**
   If you prefer manual steps:
    ```bash
    composer install
    cp .env.example .env
    php artisan key:generate
    touch database/database.sqlite # If using SQLite
    php artisan migrate
    npm install
    ```

## 💻 Development

Start the development server (Backend + Frontend + Queue + Logs) concurrently:

```bash
composer run dev
```

This will run:

- `php artisan serve` (App server)
- `npm run dev` (Vite dev server)
- `php artisan queue:listen` (Queue worker)
- `php artisan pail` (Real-time log tailing)

### Additional Commands

| Command             | Description                            |
| :------------------ | :------------------------------------- |
| `npm run build`     | Build assets for production            |
| `composer run lint` | Run Laravel Pint to fix PHP code style |
| `npm run lint`      | Run ESLint to fix JS/TS code style     |
| `npm run format`    | Run Prettier to format resources       |
| `composer run test` | Run all tests (PHP & Linting)          |

## 📁 Project Structure

```text
├── app/                  # Laravel application logic
│   ├── Actions/Fortify   # Authentication logic (Registration, Password Reset, etc.)
│   ├── Http/Controllers  # Controllers handling requests
│   └── Models/           # Eloquent models (User, etc.)
├── config/               # Configuration files
├── database/             # Migrations, factories, and seeders
├── resources/js/         # React frontend source
│   ├── components/       # Reusable UI components (Radix/Shadcn)
│   ├── hooks/            # Custom React hooks
│   ├── layouts/          # Persistent layouts (App, Auth, Settings)
│   └── pages/            # Inertia page components
├── routes/               # Route definitions (web, settings, console)
└── tests/                # Pest feature and unit tests
```

## 🔐 Authentication

Authentication is handled by **Laravel Fortify**. Features included:

- Registration & Login
- Password Reset
- Email Verification
- Two-Factor Authentication (2FA)
- Profile Information Updates
- Password Management

## 🎨 UI & Components

The project uses a set of primitive components built on top of **Radix UI**, located in `resources/js/components/ui`. These are styled with **Tailwind CSS 4** and provide a solid foundation for building complex interfaces.

## 🧪 Testing

We use **Pest PHP** for testing. To run tests:

```bash
php artisan test
# or
composer run test
```

---

Built with ❤️ using Laravel and React.
