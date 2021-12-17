# Create and Setup Server
**Requirements:**<br>
* Create a server with ubuntu 20.x OS.<br>
* Create two servers for reverse proxy and application with AWS.<br>
* Server for reverse proxy need a public ip address.<br>
* Setup security group and open ports 22, 80, and 443 for reverse proxy. <br>
* Setup security group and open all trafic for the application. <br><br>

**Server untuk Reverse Proxy**<br>
**1. Login ke AWS Console**<br>
**2. Masuk ke halaman dashboard atau AWS management console.**<br>
**3. Klik Launch a virtual machine EC2**
![Gambar AWS - Create dan Setup Server](screenshot/gambar1.png)<br>

**4. Pada step 1 Choose AMI cari ubuntu, kemudian pilih ubuntu versi 20.**<br>
![Gambar AWS - Create dan Setup Server](screenshot/gambar2.png)<br>

**5. Step 2 pilih instance type sesuai kebutuhan.**<br>
![Gambar AWS - Create dan Setup Server](screenshot/gambar3.png)<br>

**6. Step 3 Configure instance pilih Auto-assign public ip menjadi disable.**<br>
![Gambar AWS - Create dan Setup Server](screenshot/gambar4.png)<br>

**7. Step 4 Add storage. atur storage server yang dibutuhkan.**<br>
![Gambar AWS - Create dan Setup Server](screenshot/gambar5.png)<br>
**8. Step 5 Add Tags, Biarkan default**<br>
![Gambar AWS - Create dan Setup Server](screenshot/gambar6.png)<br>
**9. Step 6 Setup Security Group**<br>
![Gambar AWS - Create dan Setup Server](screenshot/gambar7.png)<br>
**10. Download key pair untuk digunakan pada saat login ke server nanti.**<br>
![Gambar AWS - Create dan Setup Server](screenshot/gambar8.png)<br>
**11. Launch Instance**<br><br>

**Allocate Elastic IP**<br>
**1. Masuk ke Elastic IPs yang terletak pada sidebar console bagian Network & Security.**<br>
**2. Kemudian Allocated Elastic IP address, AWS akan mengalokasikan sebuah IP yang dapat digunakan.**<br>
![Gambar AWS - Create dan Setup Server](screenshot/gambar10.png)<br>
**3. Beri nama kemudian associate elastic ip address dengan server yang dituju.**<br>
![Gambar AWS - Create dan Setup Server](screenshot/gambar11.png)<br>
**4. Masuk ke instance kemudian refresh instances.**<br>
![Gambar AWS - Create dan Setup Server](screenshot/gambar12.png)<br>
**5. Reverse proxy server yang dibuat sudah memiliki ip public.**<br>
**6. Server bisa diakses melalui SSH menggunakan ip public-nya**<br>
![Gambar AWS - Create dan Setup Server](screenshot/gambar13.png)<br><br>

**Server untuk Apps**<br>
**1. Login ke AWS Console**<br>
**2. Masuk ke halaman dashboard atau AWS management console**<br>

**3. Klik Launch a virtual machine EC2.**<br>
![Gambar AWS - Create dan Setup Server](screenshot/gambar1.png)<br>

**4. Pada step 1 choose AMI cari ubuntu, kemudian pilih ubuntu server versi 20.**<br>
![Gambar AWS - Create dan Setup Server](screenshot/gambar2.png)<br>

**5. Step 2 pilih instance type sesuai kebutuhan.**<br>
![Gambar AWS - Create dan Setup Server](screenshot/gambar3.png)<br>

**6. Step 3 Configure Instance pilih Auto-assign public ip menjadi disable.**<br>
![Gambar AWS - Create dan Setup Server](screenshot/gambar4.png)<br>

**7. Step 4 Add Storage.**<br>
![Gambar AWS - Create dan Setup Server](screenshot/gambar5.png)<br>

**8. Step 5 Tags biarkan default**<br>
![Gambar AWS - Create dan Setup Server](screenshot/gambar6.png)<br>

**9. Step 6 Setup security group**<br>
![Gambar AWS - Create dan Setup Server](screenshot/gambar14.png)<br>

**10. Gunakan key pair yang sama pada server reverse proxy.**<br>
**11. Launch instance.**<br>
**12. Allocate Elastic IP untuk server Apps.**
![Gambar AWS - Create dan Setup Server](screenshot/gambar15.png)<br>
**13. Akses server**<br>
![Gambar AWS - Create dan Setup Server](screenshot/gambar16.png)<br>