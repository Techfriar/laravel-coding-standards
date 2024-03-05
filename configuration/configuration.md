[<<Back](../README.md)

# Laravel Configuration Guide

# Laravel Sail Configuration Guide

## Prerequisites

- Docker Desktop installed on your machine

## Getting Started

1. Clone the repository to your local machine:
   ```bash
   git clone https://github.com/your-username/your-repository.git

2. Install Laravel Sail using Composer:
   - composer require laravel/sail --dev

3. Copy the .env.example file to .env:
   - cp .env.example .env

4. Generate an application key:
   - php artisan key:generate

## Database Configuration

   - Open the .env file and configure the database connection settings:
        DB_CONNECTION=mysql
        DB_HOST=127.0.0.1
        DB_PORT=3306
        DB_DATABASE=your_database_name
        DB_USERNAME=your_database_username
        DB_PASSWORD=your_database_password

   - Migrate the database:
        php artisan migrate


## Docker Environment Setup 

    - Start the Docker containers using Sail:
        ./vendor/bin/sail up

    - Access the application in your web browser at http://localhost.

        Running Commands

        You can run various Artisan commands, Composer commands, and other tasks using Laravel Sail:

            Run Artisan commands:

        ./vendor/bin/sail artisan migrate

        Install Composer dependencies:

        ./vendor/bin/sail composer install

        Run PHPUnit tests:

        ./vendor/bin/sail test

## Additional Configuration

   - Configure other settings such as mail, cache, and session drivers in the .env file.
   - Refer to Laravel's documentation for more advanced configuration options.

## Running the Application

Once you have configured your environment and database, you can run the Laravel application:
   - php artisan serve
