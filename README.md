安裝步驟
========
docker exec -it store_app bash
composer create-project laravel/laravel store "^12.0"

cd store
composer require laravel/breeze --dev
php artisan breeze:install react

npm install
npm run build

## 分別訪問
http://localhost/
http://localhost:5173/