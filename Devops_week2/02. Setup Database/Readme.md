# Setup Database
## Buat instance baru untuk Backend <br>
* **1. Login ke AWS Console.**<br>
* **2. Launch new instance.**<br>
* **3. Buat instance dengan spec berikut:**<br>
* * **t2.micro**<br>
* * **8Gb SSD**<br>
* * **Security group All trafic.**<br>
* * **Private IP**<br>

## Install database <br>
**1. Login ke instance.**<br>
**2. Update dan upgrade sistem.**<br>
**3. Install mysql `sudo apt install mysql-server`.**<br>
![Gambar Setup Database - Install Ubuntu](screenshot/gambar1.png)<br>

**4. Konfigurasi keamanan database `sudo mysql_secure_installation`.**<br>
**5. Input password dan pertanyaan keamanan.**<br>
![Gambar Setup Database - Install Ubuntu](screenshot/gambar2.png)<br>
![Gambar Setup Database - Install Ubuntu](screenshot/gambar3.png)<br>
![Gambar Setup Database - Install Ubuntu](screenshot/gambar4.png)<br>

## Database dapat terkoneksi dengan klien <br>
**1. Buka folder `/etc/mysql/mysql.conf.d`. edit file `mysqld.cnf`**<br>
**2. Ubah ip address `bind address` ke ip address yang dituju/yang dibolehkan.**<br>
**3. Disini saya mencoba ubah ke `0.0.0.0` publik.**<br>
![Gambar Setup Database - Install Ubuntu](screenshot/gambar5.png)<br>
**Note: mysqlx-bind-address tidak perlu ditambahkan jika memang tidak ada, jika ditambahkan manual akan menyebabkan crash pada mysql service.**<br>
**4. Save.**<br>
**5. Restart mysql service `sudo service mysql restart`.**<br>
**6. Selanjutnya adalah grant akses host.**<br>
**7. Login ke mysql server `mysql -u ridwan -p`.**<br>
**8. Ketik command berikut `GRANT ALL PRIVILEGES ON *.* TO 'ridwan'@'%' IDENTIFIED BY 'password-user';`**<br>
![Gambar Setup Database - Install Ubuntu](screenshot/gambar6.png)<br>