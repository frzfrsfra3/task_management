# task_management
# Laravel Task Management Application

A clean, efficient task management system with drag-and-drop prioritization and project organization.

## Features

- Create, edit, and delete tasks  
- Drag-and-drop task reordering  
- Automatic priority management  
- Project categorization  
- Project-based task filtering  

## Requirements

- PHP 8.1+  
- Composer 2.2+  
- Node.js 16+  
- MySQL 5.7+  

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/your-repo/task-manager.git
cd task-manager
```

### 2. Install Dependencies

```bash
composer install
npm install
```

### 3. Configure Environment

```bash
cp .env.example .env
php artisan key:generate
```

### 4. Set Up the Database

- Create a MySQL database.
- Update `.env` with your database credentials.

### 5. Run Migrations

```bash
php artisan migrate
```

### 6. Build Frontend Assets

```bash
npm run build
```

### 7. Start the Development Server

```bash
php artisan serve
```

## Usage

- Access the application at: [http://localhost:8000](http://localhost:8000)  
- First, create projects from the **Projects** page.  
- Then, add tasks and assign them to projects.  
- Use drag-and-drop to reorder tasks (priority updates automatically).  
- Use the project dropdown to filter tasks.  

## Deployment

### 1. Set Production Environment

In your `.env` file:

```ini
APP_ENV=production
APP_DEBUG=false
```

### 2. Optimize the Application

```bash
php artisan config:cache
php artisan route:cache
php artisan view:cache
```

- Ensure your web server is configured to serve the `/public` directory.

## Database Schema

### `projects`

- `id` (primary key)  
- `name` (string)  
- `timestamps`

### `tasks`

- `id` (primary key)  
- `name` (string)  
- `priority` (integer)  
- `project_id` (foreign key)  
- `timestamps`

---
