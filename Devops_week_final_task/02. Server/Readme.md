# **Server**
## **Buat instance di multipass**<br>
**1. Buka Terminal console**<br>
**2. Setup Server seperti berikut:**<br>

#### **Server Webserver** <br>
![Gambar Final Task - Server](screenshot/gambar1.png)<br>

#### **Server Frontend** <br>
![Gambar Final Task - Server](screenshot/gambar2.png)<br>

#### **Server Backend** <br>
![Gambar Final Task - Server](screenshot/gambar3.png)<br>

#### **Server Jenkins** <br>
![Gambar Final Task - Server](screenshot/gambar4.png)<br>

#### **Server Monitoring** <br>
![Gambar Final Task - Server](screenshot/gambar5.png)<br>
![Gambar Final Task - Server](screenshot/gambar6.png)<br>

## **Setup Load balance untuk apps frontend dan backend**<br>
**1. Login webserver instance**<br>
**2. masuk ke /etc/nginx**<br>
**3. Edit file config app frontend**<br>
![Gambar Final Task - Server](screenshot/gambar7.png)<br>

**4. Save**<br>
**5. Edit file config backend**<br>
![Gambar Final Task - Server](screenshot/gambar8.png)<br>

**6. Save**<br>
**7. Test config `sudo nginx -t`**<br>
**8. Restart nginx `sudo systemctl restart nginx`**<br>