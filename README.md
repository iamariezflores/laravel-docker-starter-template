# laravel-docker-template
This docker setup assumes you already have a laravel project, and these files needs to be on the root if your laravel project. It uses PHP-FPM and Nginx

# Requirements
1. Docker
2. Make

# Getting Started.
1. Clone the latest laravel ``git clone https://github.com/laravel/laravel.git . ``
2. Rename or Copy .env.example to .env ``mv .env.example .env``
3. Fill in the .env
   > DB_CONNECTION=mysql
   > 
   > DB_HOST=database
   >
   > DB_PORT=3306
   >
   > DB_DATABASE=laravel
   >
   > DB_USERNAME=laravel_user
   >
   > DB_PASSWORD=laravel_password
   >

4. Clone this repository and copy the contents to the project directory
5. Install composer dependencies
     ``docker compose run --rm app composer install``
6. In the terminal run: ``make up``
7. Open a new terminal, and then type ``make generate``
9. On the same terminal type: ``make optimize``
10. Finally open your browser to ``http://localhost``

# Make Commands
1. `` make stop `` set docker to stop
2. `` make up `` set docker to up
3. `` make generate `` php artisan key:generate
4. `` make optimize `` php artisan optimize
5. `` make build `` rebuilds the docker container
6. `` make down `` stops and removes the containers, networks and volumes

# Contributing
Pull this repository add your changes.