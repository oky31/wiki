# Nginx

**Daftar isi**  
1. [Cara kerja](#Cara-kerja-nginx)
2. [Konfigurasi file](#Konfigurasi-file)
3. [Syntax](#syntax)

## Cara kerja nginx 

Nginx memiliki 1 master proses, dan beberapa worker proses.  

**Kerjaan Master proses :**
- membaca dan mengevaluasi konfigurasi file
- memelihara worker proses

**Kerjaan Worker proses :**  
- menangani request


## Konfigurasi file
Nginx itu terdiri dari banyak module dimana module itu dicontrol dengan directive yang
ditulis didalam file configurasi nginx.

### comments   
- adalah tulisan yang akan diabaikan oleh nginx, tujuanya untuk mempermudah
 pembacaan
- comment dimulai dengan tanda '#'

### directives
- adalah syntax yang digunakan untuk mengkatifkan module-module di nginx
 dan ditulis didalam configursi file
- terbagi kedalam 2 bentuk, yaitu simple directive dan blcok directive

### simple directive
- terdiri dari name dan parameter dipisahkan oleh spasi dan diakhiri dengan titik koma
 `;`	
- contoh :
```
user nobody;
access_log path;
```

### block directive
- memiliki struktur yang sama dengan simple directive tetapi hanya titik kom `;` diganti 
dengan kurung kurawal `{}`
- contoh :
```
http {
	# http context
}
events {
	# events context
}
```

### context
- adalah block directive yang memiliki directive lain didalamnya
- block directive yang berada diluar directive lain disebut "main context"


## Syntax

### Install
```
$ sudo apt install nginx
```

### Daftar Semua proses yang sedang berjalan
```
$ ps -ax | grep nginx
```

### Menjalankan nginx
Mengunakan systemd
```
$ sudo systemctl start nginx 
$ sudo systemctl stop nginx 
$ sudo systemctl quit nginx
$ sudo systemctl reload nginx
$ sudo systemctl reopen nginx 
```

### Cek konfigurasi file
```
$ nginx -t
```

