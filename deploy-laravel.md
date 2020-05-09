# Deploy Laravel ke server

## Persiapan sistem operasi
- install web server 
- install database server
- install php
- setting firewall
- install version control

## Proses Deploy
- clone app dari repository
- arahkan root directory web server ke `/public` laravel
- install depedency mengunakan composer `composer install`
- isi .env sesuai configurasi yang di butuhkan
- generate aplication key
- migrasi schema database
