# laravel-vue
laravel8 + vue3

## docker container 安裝指令

```
docker-compose up -d　--build
```

## 專案路徑

> 在docker-compose.yml中，將專案路徑指定在./server，php、nginx都會已這個資料夾作為起始檔進行建立

需修改的點：當你在server裡建立laravel專案，請到nignx\nignx.conf找root那行把入徑指向專案的public

> 記住 server的container名稱在docker-compose.yml裡設定為 /var/www，所以你的public路徑應該為 /var/www/{專案資料夾}/public

## 網址

- 專案進入點：localhost:8010

- phpmyadmin：localhost:8811

## laravel的env修改

```
DB_CONNECTION=mysql
DB_HOST=docker-space_db_1
DB_PORT=3306
DB_DATABASE=develop
DB_USERNAME=root
DB_PASSWORD=secret
```
DB_CONNECTION 為資料庫引擎，通常是MYSQL
DB_HOST為連接域名，以這次docker對資料庫的container_name為主
DB_PORT沒有特別修改都是3306
DB_DATABASE 資料庫名稱
DB_USERNAME 使用者名稱
DB_PASSWORD 使用者密碼
