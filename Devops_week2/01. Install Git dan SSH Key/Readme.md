# Install Git dan SSH Key
==========================================<br>
## Fork repository backend apps <br>
**1. Login ke akun Github.**<br>
**2. Buka repository backend apps yang akan di fork `https://github.com/sgnd/dumbflix-backend`.**<br>
**3. Pada halaman repository backend apps, klik fork, maka akan otomatis masuk ke repository akun github kita.**<br>
![Gambar Install GIT dan SSH Key - Install Ubuntu](screenshot/gambar1.png)<br>

## Buat SSH Key untuk Git <br>
**1. Buat sebuah server/instance di AWS.**<br>
**2. Install Git `sudo apt install git`.**<br>
**3. Install SSH `sudo apt install openssh-server`.**<br>
![Gambar Install GIT dan SSH Key - Install Ubuntu](screenshot/gambar2.png)<br>

**4. Tambahkan user ke dalam config git.**<br>
**5. `git config --global user.name "username"`. kemudian ``git config --global user.email "email"``**<br>
![Gambar Install GIT dan SSH Key - Install Ubuntu](screenshot/gambar3.png)<br>

**6. Buat folder untuk menyimpan ssh key.**<br>
**7. Generate ssh key dalam folder yang telah dibuat.**<br>
**8. `ssh-keygen -t rsa -b 4096 -C "email"`.**<br>
**9. Masukkan nama file kemudian passphrase.**<br>
![Gambar Install GIT dan SSH Key - Install Ubuntu](screenshot/gambar4.png)<br>
**10. Akan menghasilkan 2 key dan yang satunya berekstensi `.pub`**<br>
![Gambar Install GIT dan SSH Key - Install Ubuntu](screenshot/gambar5.png)<br>
**11. Tambahkan ssh key yang telah di- generate tadi.**<br>
**12. Ketikkan perintah `eval "$(ssh-agent -s)"` kemudian `ssh-add .git-ssh/git-ssh`.**<br>
![Gambar Install GIT dan SSH Key - Install Ubuntu](screenshot/gambar6.png)<br>
**13. Selanjutnya masuk ke github account.**<br>
**14. Masuk ke settings, pada bagian Account settings buka SSH dan GPG keys.**<br>
**15. Buat SSH key, beri title kemudian copy-paste generated SSH key yang berekstensi `.pub` tadi.**<br>
**16. Simpan kemudian masukka password akun github.**<br>
![Gambar Install GIT dan SSH Key - Install Ubuntu](screenshot/gambar7.png)<br>
**17. Kemudian test koneksi ke github.**<br>
**18. Perintahnya `ssh -T git@github.com`**<br>
![Gambar Install GIT dan SSH Key - Install Ubuntu](screenshot/gambar8.png)<br>

## Git pull, push, dan merge pada server <br>
**1. Git clone repository backend apps `git@github.com:ridwan094/dumbflix-backend.git`.**<br>
![Gambar Install GIT dan SSH Key - Install Ubuntu](screenshot/gambar9.png)<br>
**2. Buat sebuah branch `git branch development`**<br>
**3. Kemudian arahkan ke branch development `git checkout development`.**<br>
**4. Ubah backend apps misal menambah atau menghapus file.**<br>
![Gambar Install GIT dan SSH Key - Install Ubuntu](screenshot/gambar10.png)<br>
**5. Kemudian `git add .`.**<br>
**6. Commit perubahan `git commit -m "menambah file1 file2"`.**<br>
![Gambar Install GIT dan SSH Key - Install Ubuntu](screenshot/gambar11.png)<br>
**7. Kemudian push `git push origin development`,**<br>
![Gambar Install GIT dan SSH Key - Install Ubuntu](screenshot/gambar12.png)<br>
**8. Update branch dengan pull `git pull origin development`**<br>
![Gambar Install GIT dan SSH Key - Install Ubuntu](screenshot/gambar13.png)<br>
**9. Merge branch `git merge development production`**<br>
![Gambar Install GIT dan SSH Key - Install Ubuntu](screenshot/gambar14.png)<br>