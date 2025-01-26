# Starter Template for Dockerize Laravel
Use this starter template to quickly have a dockerize laravel application you can use for development. It uses nginx for webserver, mysql for database, redis for your caching needs and phpmyadmin as a database viewer. 

## Includes 
1. Laravel 11x.
2. MySQL db.
3. Nginx.
4. Redis.
5. Phpmyadmin.

# Requirements
1. Must have installed docker into your system. 

# Getting Started.
1. Clone the latest laravel ``git clone https://github.com/laravel/laravel.git . ``
2. Do `` cp .env.example .env ``
3. In your `` .env `` configure the DB section changing `` DB_CONNECTION to mysql `` and `` DB_HOST `` to the mysql container name in your docker-compose.yaml.
4. Open it in a code editor and on a terminal run `` composer install ``.
5. Also do ``npm install``.
6. Do `` php artisan key:generate ``
7. After run `` docker compose up --build ``.
8. Then run `` docker compose exec -it app sh ``.
9. Change directory like this `` cd docker/nginx/ssl/ ``.
10. Then create a SSL cert by running this command ``openssl req -x509 -sha256 -nodes -days 365 -newkey rsa:2048 -keyout self-signed.key -out self-signed.crt `` and then following the prompts.
11. Change directory to `` cd /var/www ``.
12. Then run your migration like so `` php artisan migrate ``.
13. After all that you can visit your dockerize laravel application at `` localhost `` on your browser.
14. Phpmyadmin is located at `` localhost:8080``.

# Additional Notes
1. You can go to `` .env `` and change variable relating to database to customize it for your use case.
2. Build your css using ``npm run build ``.
3. Phpmyadmin will pull its username and password via .env variables.
4. There is a php.ini file in the directory `` docker/php/php.ini `` modify this file for your needs and build the docker image again.

# Contributing
Pull this repository add your changes.
