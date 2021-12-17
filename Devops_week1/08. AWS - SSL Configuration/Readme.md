# AWS - SSL Configuration
**Generate API Key**<br>
**1. Login dan masuk ke dashboard cloudflare.**<br>
**2. Pada bagian account klik my profile.**<br>
**3. Masuk ke halaman API tokens.**<br>
![Gambar AWS - SSL Configuration](screenshot/gambar1.png)<br>
**4. Pada bagian Global API Key, klik view, muncul kotak dialog.**<br>
![Gambar AWS - SSL Configuration](screenshot/gambar2.png)<br>
**5. Masukkan password untuk mendapatkan key.**<br>
**6. Copy dan simpan api key.**<br>
**7. Login ke server.**<br>
**8. Buat folder kemudian di dalamnya buat file untuk menyimpan api key cloudflare.**<br>
**9. Di dalam file masukkan email dan api key.**<br>
![Gambar AWS - SSL Configuration](screenshot/gambar3.png)<br>
**10. Setelah itu ubah hak akses folder ke 700 dan file ke 400.**<br>
![Gambar AWS - SSL Configuration](screenshot/gambar4.png)<br><br>

**Install Certbot and the CloudFlare DNS authenticator plugin**<br>
**1. Update snapd `sudo snap install core; sudo snap refresh core`.**<br>
**2. Install certbot `sudo snap install --classic certbot`.**<br>
**3. Link certbot dari /snap/bin/certbot ke /usr/bin/certbot `sudo ln -s /snap/bin/certbot /usr/bin/certbot`**<br>
![Gambar AWS - SSL Configuration](screenshot/gambar5.png)<br>
**4. Generate SSL `sudo certbot`**<br>
**5. masukkan email address.**<br>
**6. Kemudian Agree Terms of Service.**<br>
**7. Pilih nama website yang akan dipakaikan HTTPS.**<br>
**8. Tunggu request certificate untuk website berhasil di generate.**<br>
![Gambar AWS - SSL Configuration](screenshot/gambar6.png)<br>
**9. Masuk ke folder config nginx untuk website `/etc/nginx/dumbflix`**<br>
**10. Ketikkan perintah `cat ridwan.onlinecamp.id` untuk melihat perubahannya.**<br>
**11. Kemudian test config `sudo nginx -t`**<br>
![Gambar AWS - SSL Configuration](screenshot/gambar7.png)<br>
**12. Reload nginx `sudo systemctl reload nginx`**<br>
**13. Buka browser arahkan ke alamat url `ridwan.onlinecamp.id`.**<br>
![Gambar AWS - SSL Configuration](screenshot/gambar8.png)<br>