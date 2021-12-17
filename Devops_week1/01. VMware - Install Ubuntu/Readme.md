# VMware-Install-Ubuntu
**Install Ubuntu Server 20.x with VMware** <br>

**1. Download VMware, dan juga Ubuntu server iso** <br>
**2. Install VMWare, kemudian jalankan VMware**<br>
**3. Create virtual machine baru**<br>
![Gambar VMware - Install Ubuntu](screenshot/gambar1.png)<br>

**4. Pilih "Use ISO Image" Browse ubuntu server iso yang telah di download pada step 1, kemudian Next.**<br>
![Gambar VMware - Install Ubuntu](screenshot/gambar2.png)<br>

**5. Pada "Personalize Linux" input nama,username, dan password. kemudian Next**<br>
**6. Pada "Guest Operating System" pilih Linux. kemudian Next**<br>
![Gambar VMware - Install Ubuntu](screenshot/gambar3.png)<br>

**7. Kemudian beri nama pada virtual machine serta tentukan lokasi filenya. klik Next.**<br>
![Gambar VMware - Install Ubuntu](screenshot/gambar4.png)<br>

**8. Pada "Disk Size" beri sebesar 20GB (recommended size untuk ubuntu) kemudian pilih "Split virtual disk into multiple files"**<br>
![Gambar VMware - Install Ubuntu](screenshot/gambar5.png)<br>

**9. Selanjutnya Custom spec virtual machine sesuai kebutuhan, misal 2 CPU cores, memory 2048 Mb, network adapter Bridge. Klik Finish**<br>
![Gambar VMware - Install Ubuntu](screenshot/gambar6.png)<br>

**10. Masuk pada proses instalasi os ubuntu**<br>
**11. Pilih bahasa "English"**<br>
![Gambar VMware - Install Ubuntu](screenshot/gambar7.png)<br>

**12. Konfigurasi keyboard set default**<br>
![Gambar VMware - Install Ubuntu](screenshot/gambar8.png)<br>

**13. Setting network connections bisa DHCP (ip dinamis) ataupun manual (ip static), sesuai kebutuhan. Untuk sementara bisa menggunakan DHCP.**<br>
![Gambar VMware - Install Ubuntu](screenshot/gambar9.png)<br>

**14. Configure Proxy, jika ingin menggunakan proxy address bisa diisi maupun dikosongkan saja.**<br>
![Gambar VMware - Install Ubuntu](screenshot/gambar10.png)<br>

**15. Ubuntu archive mirror menggunakan yang default saja.**<br>
![Gambar VMware - Install Ubuntu](screenshot/gambar11.png)<br><br>

**Create swap memory and root partition**<br>
**Proses pembuatan swap dan root partition dilakukan saat proses instalasi ubuntu server di vmware**<br>
**1. Selanjutnya, atur storage configuration, pilih "Custom storage layout". kemudian "Done"**<br>
![Gambar VMware - Install Ubuntu](screenshot/gambar12.png)<br>

**2. Pilih device /dev/sda, kemudian Add GPT partition**<br>
![Gambar VMware - Install Ubuntu](screenshot/gambar13.png)<br>

**3. Misal akan dibuat 1GB swap, pada field Size input 1G.**<br>
**4. Pada format ubah menjadi swap, kemudian Create**<br>
![Gambar VMware - Install Ubuntu](screenshot/gambar14.png)<br>

**5. Swap sudah dibuat.**<br>
**6. Pilih /dev/sda, kemudian Add GPT partition**<br>
**7. Pada field "Size" input sisa disk yaitu 18.997G**<br>
**8. Pilih format ext4**<br>
**9. Untuk Mount pilih "/" untuk root, kemudian Create**<br>
![Gambar VMware - Install Ubuntu](screenshot/gambar15.png)<br>

![Gambar VMware - Install Ubuntu](screenshot/gambar16.png)<br>

**10. Kemudian konfirmasi pilih Continue**<br>
![Gambar VMware - Install Ubuntu](screenshot/gambar17.png)<br>

**11. Isi User profile seperti nama, nama server, username, dan password untuk sebagai informasi login ke ubuntu nanti.**<br>
![Gambar VMware - Install Ubuntu](screenshot/gambar18.png)<br>

**12. Selanjutnya install ssh, pilih atau centang install OpenSSH server.**
![Gambar VMware - Install Ubuntu](screenshot/gambar19.png)<br>

**13. Featured Server bisa dipilih sesuai kebutuhan, jika tidak ada kosongkan saja. Next**<br>
![Gambar VMware - Install Ubuntu](screenshot/gambar20.png)<br>

**14. Tunggu proses instalasi ubuntu server selesai.**<br>
![Gambar VMware - Install Ubuntu](screenshot/gambar21.png)<br>

**15. Setelah proses instalasi selesai reboot vm kemudian login menggunakan akun yang telah dibuat pada step 11.**<br>
![Gambar VMware - Install Ubuntu](screenshot/gambar22.png)<br>

**16. Ubuntu di vmware sudah dapat di operasikan.**<br>
![Gambar VMware - Install Ubuntu](screenshot/gambar23.png)<br><br>

**Local server can connect to the internet**<br>
**1. Setelah proses instalasi ubuntu di vm selesai.**<br>
**2. Login ke vm di ubuntu server**<br>
**3. Untuk mengecek apakah vm ada koneksi internet bisa dilakukan perintah ping, misal ping `www.google.com`**
![Gambar VMware - Install Ubuntu](screenshot/gambar24.png)<br>
