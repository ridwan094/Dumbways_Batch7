# AWS - Server for Application
**Requirements**<br>
* Update and upgrade the system operation. <br>
* Install node 10.x <br>
* Clone application in here `https://github.com/sgnd/dumbflix-frontend`. <br>
* Change directory to `frontend` and deploy the application. <br><br>

**Update and upgrade sistem operasi**<br>
**1. Login ke App-server**<br>
**2. Update dan upgrade system `sudo apt update && sudo apt upgrade -y`.**<br>
![Gambar AWS - Server for Application](screenshot/gambar1.png)<br><br>

**Install Node JS versi 10.x**<br>
**1. Install NVM untuk management NodeJS version `wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash`**<br>
![Gambar AWS - Server for Application](screenshot/gambar2.png)<br>
**2. Install nodejs versi 10.xx `nvm install 10` kemudian `nvm use 10`**<br>
![Gambar AWS - Server for Application](screenshot/gambar3.png)<br>
**3. NodeJS telah terinstall**<br><br>

**Clone Application**<br>
**1. Clone apps `git clone https://github.com/sgnd/dumbflix-frontend`**<br>
**2. Pindahkan/rename folder dumbflix-frontend ke folder frontend `mv dumbflix-frontend frontend`**<br>
**3. Change directory ke frontend `cd frontend`**<br>
![Gambar AWS - Server for Application](screenshot/gambar4.png)<br><br>

**Deploy Application**<br>
**1. Masuk ke directory frontend.**<br>
**2. Ketik `npm install` untuk menginstall node_modules dan dependency apps.**<br>
**3. Deploy apps, `npm run start`**<br>
**4. Buka browser, arahkan url ke `3.217.220.200:3000`**<br>
![Gambar AWS - Server for Application](screenshot/gambar5.png)<br><br>