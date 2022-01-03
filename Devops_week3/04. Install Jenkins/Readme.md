# Install Jenkins
**1. Buat terlebih dahulu server multipass untuk jenkins.**<br>
![Gambar Docker - Install Jenkins](screenshot/gambar1.png)<br>

![Gambar Docker - Install Jenkins](screenshot/gambar2.png)<br>

**2. Kemudian install jenkins dari docker dengan menjalankan perintah**<br>
```
docker run --name ci-cd -p 8080:8080 -p 50000:50000 -d -v jenkins_home:/var/jenkins_home jenkins/jenkins
```

**port 8080 untuk akses gui jenkins dan 50000 untuk jenkins master/slave - perintah -v untuk membuat volume jenkins yang ada pada directory jenkins_home - jenkins/jenkins merupakan images dari dockerhub - --name untuk memberikan nama container**<br>
![Gambar Docker - Install Jenkins](screenshot/gambar3.png)<br>

**3. Kemudian lakukan reverse_proxy untuk jenkins.**<br>
![Gambar Docker - Install Jenkins](screenshot/gambar4.png)<br>

**4. Akses domain yang sudah terdaftarkan `cicd.ridwan.onlinecamp.id`**<br>
![Gambar Docker - Install Jenkins](screenshot/gambar5.png)<br>

**5. Lalu copy paste string random tersebut kedalam `unlock jenkins`, kita bisa melihat str random dengan menggunakan logs.**<br>
![Gambar Docker - Install Jenkins](screenshot/gambar6.png)<br>

**6. Lalu buat user, lalu klik save dan continue.**<br>
![Gambar Docker - Install Jenkins](screenshot/gambar7.png)<br>

**7. Pilih Customize Jenkins yang `install suggested plugins`**<br>
![Gambar Docker - Install Jenkins](screenshot/gambar8.png)<br>

**8. Lalu process install plugins -plugins.**<br>
![Gambar Docker - Install Jenkins](screenshot/gambar9.png)<br>

**9. Lalu klik save dan finish.**<br>
![Gambar Docker - Install Jenkins](screenshot/gambar10.png)<br>

**10. Jenkins is ready!, kita sudah dapat menggunakan jenkins!**<br>
