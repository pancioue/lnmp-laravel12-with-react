安裝步驟
========
1. `docker compose up -d` 完以後進到容器
```
docker exec -it store_app bash
```

2. 建置 laravel 專案
```
composer create-project laravel/laravel store "^12.0"
```

3. 安裝 react
```
cd store
composer require laravel/breeze --dev
php artisan breeze:install react
```

4. 以下步驟省略應該不影響
```
npm install
npm run build
```

分別訪問
--------
* http://store.localhost/
* http://store.localhost:5173/