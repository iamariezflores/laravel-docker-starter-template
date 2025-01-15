# Starter Template for Dockerize Laravel
Use this template to quickly have a dockerize laravel application you can use for development. 

# Requirements
1. Docker

# Getting Started.
1. Clone the latest laravel ``git clone https://github.com/laravel/laravel.git . ``
2. Open it in a code editor and on a terminal run `` composer install ``.
3. After run `` docker compose up --build ``.
4. Then run `` docker compose exec -it app sh ``.
5. Change directory like this `` cd docker/nginx/ssl/ ``.
6. Then create a SSL cert by running this command ``openssl req -x509 -sha256 -nodes -days 365 -newkey rsa:2048 -keyout self-signed.key -out self-signed.crt `` and then following the prompts.
7. Change directory to `` cd /var/www ``.
8. Then run your migration like so `` php artisan migrate ``.
9. After all that you can visit your dockerize laravel application at `` localhost `` on your browser.
10. Phpmyadmin is located at `` localhost:8080``.

# Additional Notes
1. You can go to `` .env `` and change variable relating to database to customize it for your use case.
2. Phpmyadmin will pull its username and password via .env variables.

# Contributing
Pull this repository add your changes.
