<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400" alt="Laravel Logo"></a></p>

## Laravel 11 Docker
- Laravel v11
- PHP v8.3
- MySQL v8
- phpMyAdmin

##  How To Deploy
- `git clone https://github.com/SutoIstvan/docker-laravel-phpmyadmin.git`
- `cd docker-laravel-phpmyadmin`
- `docker compose up -d --build`
- `docker compose exec phpmyadmin chmod 777 /sessions`
- `chown -R www-data:www-data /var/www/laravel/storage /var/www/laravel/bootstrap/cache`
- `chmod -R 775 /var/www/laravel/storage /var/www/laravel/bootstrap/cache`
- `exit`
- `rename .env.example to .env`
- `docker compose run composer install`
- `docker compose run artisan migrate`
- `docker compose run artisan key:generate`

## URL
`URL: http://localhost:8000/`

## phpMyAdmin
`URL: http://localhost:8080/`

## env
DB_CONNECTION=mysql
DB_HOST=mysql
DB_PORT=3306
DB_DATABASE=laravel_db
DB_USERNAME=laravel
DB_PASSWORD=root
