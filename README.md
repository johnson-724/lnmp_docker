## 專案建置

`docker compose build`

`docker compose up -d`

## PHP 專案

將專案資料夾放到此專案上層

## nginx 設定 ssl

```shell
mkdir ./nginx/ssl

cd nginx/ssl

sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout ./nginx.key -out ./nginx.crt

```

## 預設 php 版本 domain

`https://{defaultDomain}/{folderPath}`

### php7.4

`php74.docker.local`

### php8.1

`php81.docker.local`

## 自行設定專案 domain

將自定 nginx.conf 加入到 `./nginx/sites-enabled`

## 修改 hosts

`sudo vim /etc/hosts`

加上
```
127.0.0.1 php74.docker.local 
127.0.0.1 php81.docker.local
```