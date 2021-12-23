# Deployment Backend App
**1. Clone backend app `git@github.com:ridwan094/dumbflix-backend.git`**
![Gambar Deployment Backend Apps - Install Ubuntu](screenshot/gambar1.png)<br>

**2. Buka Readme file dalam backend app.**<br>
![Gambar Deployment Backend Apps - Install Ubuntu](screenshot/gambar2.png)<br>
**3. Kemudian jalankan requirementnya.**<br>
* Install nodejs <br>
* copy .env.example .env <br>
* Import database dengan sequelize. <br>

![Gambar Deployment Backend Apps - Install Ubuntu](screenshot/gambar3.png)<br>

![Gambar Deployment Backend Apps - Install Ubuntu](screenshot/gambar4.png)<br>

* Edit Config.json file sesuaikan database username, password, nama database, dan host addressnya. <br>

![Gambar Deployment Backend Apps - Install Ubuntu](screenshot/gambar5.png)<br>

**4. Login ke database instance untuk membuat databasenya dulu.**<br>
**5. Login mysql `sudo mysql -u root -p`.**<br>
**6. Masukkan password mysql.**<br>
**7. Buat database `mysql > create database dumbflix`.**<br>
![Gambar Deployment Backend Apps - Install Ubuntu](screenshot/gambar6.png)<br>

## Import Database dengan Sequelize <br>
**1. Install sequelize-cli `npm install --save-dev  -g sequelize-cli`.**<br>
![Gambar Deployment Backend Apps - Install Ubuntu](screenshot/gambar7.png)<br>

**2. Migrate database `sequelize db:migrate`**<br>

![Gambar Deployment Backend Apps - Install Ubuntu](screenshot/gambar8.png)<br>

**3. Run backend apps dengan pm2 `pm2 start ecosystem.config.js`**<br>

![Gambar Deployment Backend Apps - Install Ubuntu](screenshot/gambar9.png)<br>

