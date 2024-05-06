# Laravel Artisan Commands Documentation

## `php artisan serve`

- **Use Case:** Running a local development server.
- **Description:** This command starts a development server on your local machine, typically on port 8000.
- **Example:** `php artisan serve`

## `php artisan migrate`

- **Use Case:** Running database migrations.
- **Description:** This command executes all pending migrations.
- **Example:** `php artisan migrate`

## `php artisan migrate:fresh`

- **Use Case:** Resetting and re-running all migrations.
- **Description:** This command resets the database and then re-executes all migrations.
- **Example:** `php artisan migrate:fresh`

## `php artisan make:model`

- **Use Case:** Creating a new Eloquent model.
- **Description:** This command generates a new model class in the `app/Models` directory.
- **Example:** `php artisan make:model Post`

## `php artisan make:controller`

- **Use Case:** Generating a new controller.
- **Description:** This command creates a new controller class in the `app/Http/Controllers` directory.
- **Example:** `php artisan make:controller PostController`

## `php artisan make:middleware`

- **Use Case:** Creating a new middleware.
- **Description:** This command generates a new middleware class in the `app/Http/Middleware` directory.
- **Example:** `php artisan make:middleware Authenticate`

## `php artisan make:migration`

- **Use Case:** Creating a new migration file.
- **Description:** This command generates a new migration file in the `database/migrations` directory.
- **Example:** `php artisan make:migration create_posts_table`

## `php artisan make:seeder`

- **Use Case:** Generating a new database seeder.
- **Description:** This command creates a new seeder class in the `database/seeders` directory.
- **Example:** `php artisan make:seeder PostsTableSeeder`

## `php artisan db:seed`

- **Use Case:** Running database seeders.
- **Description:** This command executes all seed classes.
- **Example:** `php artisan db:seed`

## `php artisan make:factory`

- **Use Case:** Creating a new model factory.
- **Description:** This command generates a new factory class in the `database/factories` directory.
- **Example:** `php artisan make:factory PostFactory`

## `php artisan route:list`

- **Use Case:** Listing all registered routes.
- **Description:** This command displays a list of all registered routes for the application.
- **Example:** `php artisan route:list`

## `php artisan cache:clear`

- **Use Case:** Clearing the application cache.
- **Description:** This command clears the application cache.
- **Example:** `php artisan cache:clear`

## `php artisan config:cache`

- **Use Case:** Caching the configuration.
- **Description:** This command caches the configuration files for faster loading.
- **Example:** `php artisan config:cache`

## `php artisan config:clear`

- **Use Case:** Clearing the configuration cache.
- **Description:** This command clears the configuration cache.
- **Example:** `php artisan config:clear`

## `php artisan view:clear`

- **Use Case:** Clearing compiled views.
- **Description:** This command clears all compiled view files.
- **Example:** `php artisan view:clear`

## `php artisan make:auth`

- **Use Case:** Scaffold basic login and registration views and routes.
- **Description:** This command generates login and registration views and routes.
- **Example:** `php artisan make:auth`
