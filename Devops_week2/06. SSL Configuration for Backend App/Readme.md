# SSL Configuration for Backend App
## Arahkan frontend api.js ke backend app <br>
**1. Login ke frontend instance.**<br>
**2. Masuk ke folder `frontend/config`.**<br>
![Gambar SSL Configuration for Backend app](screenshot/gambar1.png)<br>

**3. Edit file `api.js` arahkan `baseURL: 'https://api.ridwan.onlinecamp.id/api/v1`**<br>
![Gambar SSL Configuration for Backend app](screenshot/gambar2.png)<br>

**4. Restart App.**<br>

## SSL Configuration
**1. Login ke instance gateway.**<br>
**2. Update dan upgrade sistem.**<br>
**3. Install certbot untuk backend**<br>
**4. Perintahnya `sudo certbot certonly -d api.ridwan.onlinecamp.id`.**<br>
![Gambar SSL Configuration for Backend app](screenshot/gambar3.png)<br>

**5. Syntax penambahan SSL dari certbot.**<br>
![Gambar SSL Configuration for Backend app](screenshot/gambar4.png)<br>

**6. Test konfigurasi `sudo nginx -t`**<br>
**7. Restart nginx `sudo service restart nginx`**<br>
**8. Buka website `ridwan.onlinecamp.id`**<br>
**9. Buat akun atau registrasi untuk testing koneksi ke backend.**<br>
![Gambar SSL Configuration for Backend app](screenshot/gambar5.png)<br>