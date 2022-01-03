# SETUP JENKINS ONLINE
**1. Berikut tampilan dashboard jenkins saat baru pertama masuk.**<br>
![Gambar Docker - Setup Jenkins Job](screenshot/gambar1.png)<br>

**2. Lalu kita install `Publish over ssh`**<br>
![Gambar Docker - Setup Jenkins Job](screenshot/gambar2.png)<br>

**3. Pilih Create a new job, masukkan name lalu pilih `Freestyle project`**<br>
![Gambar Docker - Setup Jenkins Job](screenshot/gambar3.png)<br>

**4. Lalu pilih `Git` dan masukkan link repo anda, pilih build trigger yang `Github hook trigger for GITscn polling`**<br>
![Gambar Docker - Setup Jenkins Job](screenshot/gambar4.png)<br>
![Gambar Docker - Setup Jenkins Job](screenshot/gambar5.png)<br>

**5. Lalu ke masuk kedalam `Configure system` dan pilih `publish over SSH`, masukkan ssh-keygen yang anda miliki.**<br>
![Gambar Docker - Setup Jenkins Job](screenshot/gambar6.png)<br>

**6. Kemudian isikan yang dibutuhkan dan gunakan password jika sudah memiliki nya di server.**<br>
![Gambar Docker - Setup Jenkins Job](screenshot/gambar7.png)<br>
![Gambar Docker - Setup Jenkins Job](screenshot/gambar8.png)<br>

**7. Lalu coba lakukan Test config, jika status success maka configure berhasil.**<br>
![Gambar Docker - Setup Jenkins Job](screenshot/gambar9.png)<br>

**8. Lalu kembali lagi ke Configure frontend dan pilih `build` dan server yang ingin digunakan, lalu pilih verbose.**<br>
![Gambar Docker - Setup Jenkins Job](screenshot/gambar10.png)<br>

**9. dan ikuti perintah berikut.**<br>
![Gambar Docker - Setup Jenkins Job](screenshot/gambar11.png)<br>
![Gambar Docker - Setup Jenkins Job](screenshot/gambar12.png)<br>

**10. Dan masukkan perintah tersebut untuk melakukan build image dan menjalankan container.**<br>
![Gambar Docker - Setup Jenkins Job](screenshot/gambar13.png)<br>

**11. Lalu klik `build now`**<br>
![Gambar Docker - Setup Jenkins Job](screenshot/gambar14.png)<br>

**12. Dan jenkins sedang memeriksa configure yang telah kita lakukan tadi.**<br>
![Gambar Docker - Setup Jenkins Job](screenshot/gambar15.png)<br>
![Gambar Docker - Setup Jenkins Job](screenshot/gambar16.png)<br>

**13. Lalu kita buat `WEBHOOK` di githubm pilih webhook**<br>
![Gambar Docker - Setup Jenkins Job](screenshot/gambar17.png)<br>

**14. Klik `Add Webhook`**<br>
**15. dan masukkan URL dari jenkins, seperti berikut.**<br>
![Gambar Docker - Setup Jenkins Job](screenshot/gambar18.png)<br>

**16. dan coba kita lakukan editing readme.md, apakah jenkins akan mengtrigger suatu perubahan.**<br>
![Gambar Docker - Setup Jenkins Job](screenshot/gambar19.png)<br>

**17. Maka akan lakukan proses di bawah kiri, dan klik saja untuk melihat.**<br>
![Gambar Docker - Setup Jenkins Job](screenshot/gambar20.png)<br>

**18. Perubahan yang dilakukan berhasil dan akan memunculkan pesan nya juga.**<br>
![Gambar Docker - Setup Jenkins Job](screenshot/gambar21.png)<br>
![Gambar Docker - Setup Jenkins Job](screenshot/gambar22.png)<br>
