composer install --ignore-platform-reqs

cp .env.example .env

docker-compose build

docker-compose up

docker container exec api-production composer install

docker container exec api-production php artisan key:generate

docker container exec api-production php artisan migrate

Truy cập vào đường dẫn: http://localhost:9001/

Truy cập vào đường dẫn để chạy phpMyAdmin: http://localhost:91/

Tài khoản và password phpMyAdmin:
- tk: root
- mk: 123456