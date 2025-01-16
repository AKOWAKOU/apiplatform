## Premiers Pas Avec Symfony

    git clone https://github.com/AKOWAKOU/apiplatform.git

    cd apiplatform

## Install Dependences
    
    composer install


## Prepare DataBase

    Go to .env or create file .env
    sqlite database if pdo_sqlite active for php
    # DATABASE_URL="sqlite:///%kernel.project_dir%/var/data.db"

    Mysql database if pdo_mysql active for php
    DATABASE_URL="mysql://root@127.0.0.1:3306/app?serverVersion=8.0.32&charset=utf8mb4"

    Mysql database if pdo_mysql active for php
    # DATABASE_URL="mysql://app:!ChangeMe!@127.0.0.1:3306/app?serverVersion=10.11.2-MariaDB&charset=utf8mb4"

    postgresql database if pdo_pgsql active for php
    #DATABASE_URL="postgresql://app:!ChangeMe!@127.0.0.1:5432/app?serverVersion=16&charset=utf8"
    ###< doctrine/doctrine-bundle ###    


## Create and Migrations Database for app

    Use command for create database to app
    php bin/console doctrine:database:create

    Use command for create  schema database to app
    php bin/console doctrine:schema:create

    Use command for create migration to app
    php bin/console make:migration
    php bin/console doctrine:migrations:migrate


## Run server to two possibilities
    One:
        symfony serve (require symfony cli installed)

    two:
        php -S localhost:{port(default 8000)} -t public/




    Go to http://localhost:8000/api          