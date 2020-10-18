# laravel-docker

## Setup

1. Clone Laravel repo: `git clone https://github.com/laravel/laravel.git`
2. Install PHP dependencies: `docker run --rm -v $(pwd):/app composer install`
3. Run Docker containers: `docker-compose up -d`
4. Laravel setup:
    - `docker-compose exec app php artisan key:generate`
    - `docker-compose exec app php artisan config:cache`
5. Create default Laravel tables: `docker-compose exec app php artisan migrate`

## JS

- Install Node packages: `docker run -v $(pwd):/app -w /app node:14-alpine npm install`
- Watch for changes: `docker run -v $(pwd):/app -w /app node:14-alpine npm run watch-poll`
