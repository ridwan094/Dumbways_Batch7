# AWS - Reverse Proxy
**Requirements**<br>
* Update and Upgrade the operating system/<br>
* Install webserver for reverse proxy.<br>
* Create reverse proxy from the application with port 3000 to port 80.<br><br>

**1. Login ke server reverse proxy.**<br>
**2. Update dan upgrade sistem.**
![Gambar AWS - Reverse Proxy](screenshot/gambar1.png)<br>

**3. Install nginx `sudo apt install nginx`**<br>
**4. Masuk ke dalam folder nginx `/etc/nginx`**<br>
**5. Buat folder `dumbflix` untuk menyimpan file konfigurasi.**<br>
![Gambar AWS - Reverse Proxy](screenshot/gambar2.png)<br>

**6. Masuk ke dalam folder `dumbflix`**<br>
**7. Buat file konfigurasi `nano ridwan.onlinecamp.id` kemudian buat aplikasi mengarah ke port 80.**<br>
![Gambar AWS - Reverse Proxy](screenshot/gambar3.png)<br>
**8. Kemudian include konfigurasi dumbflix tadi ke `nginx.conf`, Save perubahan.**<br>
![Gambar AWS - Reverse Proxy](screenshot/gambar4.png)<br>
**9. Test konfigurasi file, `sudo nginx -t`, untuk mengecek syntax pada konfigurasi apakah sudah ok.**<br>
![Gambar AWS - Reverse Proxy](screenshot/gambar5.png)<br>
**10. Restart nginx `sudo systemctl restart nginx`**<br>
**11. Selanjutnya arahkan domain name ke public ip reverse-proxy-server, untuk dapat berjalan di port 80, uncheck proxy status.**<br>
![Gambar AWS - Reverse Proxy](screenshot/gambar6.png)<br>
**12. Buka browser kemudian arahkan url ke `ridwan.onlinecamp.id` untuk mengakses site.**<br>
![Gambar AWS - Reverse Proxy](screenshot/gambar7.png)<br>