# Install Application
### **App Frontend** <br>
**1. Disini ktia akan membuat sebuah container dengan docker compose, pertama masuk kedalam server frontend & backend.**<br>
![Gambar Docker - Install Application](screenshot/gambar1.png)<br>
![Gambar Docker - Install Application](screenshot/gambar2.png)<br>

**2. Lalu jika image tidak ada kita dapat melakukan pull image dari repo kita. dengan perintah berikut, jika image ada kita dapat memakai yang sudah ada.**
![Gambar Docker - Install Application](screenshot/gambar3.png)<br>

**3. Kemudian buat sebuah file docker-compose.yml dan ketikan perintah berikut didalamnya.**<br>
![Gambar Docker - Install Application](screenshot/gambar4.png)<br>

**4. Lalu untuk membuat sebuah container ketikan perintah berikut.**<br>
![Gambar Docker - Install Application](screenshot/gambar5.png)<br>

**5. Kita dapat melihat docker yang sudah berjalan dengan ketikan perintah `docker ps`**<br>
![Gambar Docker - Install Application](screenshot/gambar6.png)<br>

**6. Periksa di browser apakah aplikasi dapat di akses dengan memasukkan `ip:port`**<br>
![Gambar Docker - Install Application](screenshot/gambar7.png)<br>

**7. Lalu masuk ke server backend dan buat file docker-compose.yml dan ketikkan perintah berikut.**<br>
![Gambar Docker - Install Application](screenshot/gambar8.png)<br>

**8. Jika image belum ada kita dapat melaukan pull saja, jika sudah kita bisa langsung saja memakai image tersebut.**<br>
![Gambar Docker - Install Application](screenshot/gambar9.png)<br>

**9. Lalu buat container dengan docker-compose, dengan ketikan perintah berikut.**<br>
**10. Periksa apakah container sudah berjalan dengan perintah `docker ps`**
![Gambar Docker - Install Application](screenshot/gambar10.png)<br>

**11. Periksa di browser apakah apps berjalan dengan baik dengan memasukkan `ip:port`**<br>
![Gambar Docker - Install Application](screenshot/gambar11.png)<br>