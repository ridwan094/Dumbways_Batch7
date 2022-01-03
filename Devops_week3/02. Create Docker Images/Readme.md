# Buat Docker Images
### **Membuat docker images untuk frontend.**<br>
**1. Login ke server frontend.**<br>
**2. Download images node js, `docker pull node:14-alpine`**<br>
![Gambar Docker - Create Docker Images](screenshot/gambar1.png)<br>

**3. Clone app frontend `git clone git@github.com:ridwan094/dumbflix-frontend.git`**<br>
![Gambar Docker - Create Docker Images](screenshot/gambar2.png)<br>

**4. Masuk ke dalam folder dumbflix-frontend.**<br>
**5. Buat file Dockerfile `nano Dockerflie`**<br>
![Gambar Docker - Create Docker Images](screenshot/gambar3.png)<br>

**6. Simpan.**
**7. Lakukan build image, file `Dockerfile` yang dibuat masing-masing Apps tadi dan dijadikan sebuah image, dengan mengetikkan perintah berikut.**<br>
![Gambar Docker - Create Docker Images](screenshot/gambar4.png)<br>

**8. Kita dapat memeriksa list docker images yang ada, dengan ketikan perintah berikut.**<br>
![Gambar Docker - Create Docker Images](screenshot/gambar5.png)<br>

**9. Buatkan juga file Dockerfile untuk app backend, dan ketikkan perintah berikut di dalamnya.**<br>
![Gambar Docker - Create Docker Images](screenshot/gambar6.png)<br>

**10. Lalu lakukkan build untuk backend, dengan ketikkan perintah berikut.**<br>
![Gambar Docker - Create Docker Images](screenshot/gambar7.png)<br>

**11. Setelah membuat image frontend & backend yang kita buat tadi kita dapat melakukan push image frontend, dengan mengetikkan perintah berikut.**<br>
![Gambar Docker - Create Docker Images](screenshot/gambar8.png)<br>

**12. Lalu push juga untuk yang image backend.**<br>
![Gambar Docker - Create Docker Images](screenshot/gambar9.png)<br>

**13. Kita dapat langsung memeriksa di akun yang kita miliki. apakah image yang kita push masuk atau tidak. disini image yang saya push sudah masuk kedalam repository docker hub saya.**<br>
![Gambar Docker - Create Docker Images](screenshot/gambar10.png)<br>