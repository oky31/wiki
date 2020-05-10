# Nginx

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

**comments** 
	- adalah tulisan yang akan diabaikan oleh nginx, tujuanya untuk mempermudah
 pembacaan
	- comment dimulai dengan tanda '#'

**directives**
	- adalah syntax yang digunakan untuk mengkatifkan module-module di nginx
 dan ditulis didalam configursi file
	- terbagi kedalam 2 bentuk, yaitu simple directive dan blcok directive

**simple directive**
	- terdiri dari name dan parameter dipisahkan oleh spasi dan diakhiri dengan titik koma
 `;`
	- contoh :
	```
	user nobody;
	
	access_log path;
	```
**block directive**
	-