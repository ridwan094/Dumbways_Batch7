# Setup Monitoring Server
**1. Buat instance multipass untuk monitoring.**<br>
**2. Buat docker-compose untuk node-exporter.**<br>
**3. Buat docker-compose untuk prometheus dan grafana.**<br><br>

## **Buat instance multipass monitoring**<br>
**1. jalankan perintah `multipass launch --name monitoring`. untuk membuat instance baru untuk monitoring.**<br>
![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar1.png)<br>

**2. kita bisa melihat server multipass yang telah dibuat sebelumnya, menggunakan perintah `multipass list`**<br>
![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar2.png)<br>

**3. Masuk ke dalam server, `multipass shell monitoring`**<br>
![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar3.png)<br>

**4. update dan upgrade sistem.**<br>
![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar4.png)<br><br>

## **Install Docker** <br>
**1. Jalankan perintah update system.**<br>
![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar5.png)<br>

**2. jalankan perintah berikut.**<br>
```
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```

![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar6.png)<br>

```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar7.png)<br>

```
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
```

![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar8.png)<br>

```
sudo apt update
```
```
sudo apt-get install docker-ce docker-ce-cli containerd.io
```

![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar9.png)<br>

**3. Kita bisa melihat apakah docker sudah berjalan dengan baik.**<br>
![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar10.png)<br><br>

## **Install Node Exporter**<br>
**1. Masuk ke dalam server yang ingin di install node-exporter/ingin kita monitoring.**<br>
**2. Buat direktori node-exporter**<br>
**3. Lalu buat file docker-compose di dalam direktori, dengan perintah berikut.**<br>
![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar11.png)<br>

**4. Save**<br>
**5. Lalu jalakan `docker-compose up -d`**<br>
![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar12.png)<br>

**6. Kita bisa melihat metrics dari node-exporter yang sudah dijalankan, dengan memasukkan `ip:port`**<br>
![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar13.png)<br><br>

## **Install Prometheus, Grafana, cAdvisor**<br>
**1. Masuk ke dalam server monitoring.**<br>
**2. Lalu kita pull image prometheus.**<br>
![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar14.png)<br>

**3. Kita bisa meliihat image apa saja yang sudah terinstall. dengan menjalankan `docker images`**<br>
![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar15.png)<br>

**4. Buat direktori monitoring.**<br>
**5. Masuk ke dalam direktori monitoring.Selanjutnya buat file `docker-compose.yml`**<br>
![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar19.png)<br>
![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar20.png)<br>
![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar21.png)<br>

**6. Save.**
**7. Selanjutnya buat file untuk konfigurasi `prometheus.yml`**<br>
![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar22.png)<br>

**8. Save**<br>
**9. Selanjutnya jalankan `docker-compose up -d`**<br>
![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar23.png)<br>

**10. Kita bisa melihat prometheus, dengan memasukkan `ip:port` ke web browser kita.**<br>
![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar24.png)<br>

**11. Lalu kita bisa melihat `Configuration` yang terjadi di dalam prometheus.**<br>
![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar25.png)<br>

**12. Kita juga bisa melihat targets server mana saja yang kita monitoring di dalam prometheus.**<br>
![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar26.png)<br>

**13. Selanjutnya buka `ip:port` masukkan port 8080 di dalam web browser untuk memonitoring server menggunakan cAdvisor.**<br>
![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar27.png)<br>

**14. Buka web browser, lalu arahkan `ip:port`, ke port 3000, untuk mengakses/membuka monitoring grafana.**
![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar28.png)<br><br>

## **Reverse proxy Monitoring** <br>
**1. Login ke dalam cloudflare.**<br>
**2. pilih `sugandaletters@outlokk.com`**<br>
**3. Pilih `onlinecamp.id`**<br>
**4. Masuk ke menu DNS.**<br>
**5. Selanjutnya pilih Add record, pilih `Type A`, dan masukkan name serta ip reverse proxy.**<br>
![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar29.png)<br>

**6. Masuk ke dalam server Gateway/reverse proxy.**<br>
**7. Buat file `monitoring.name.onlinecamp.id`**<br>
![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar30.png)<br>

**8. Save**<br>
**9. Selanjutnya jalankan `sudo systemctl restart nginx`**<br>
![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar31.png)<br>

**10. Masuk ke dalam web browser, dan arahkan url ke `monitoring.nama.onlinecamp.id` yang sudah dikonfigurasi sebelumnya.**<br>
**11. Masukkan username dan password.**<br>
**12. Akan masuk ke dashboard dari monitoring grafana.**<br>
![Gambar Monitoring - Setup Monitoring Server](screenshot/gambar32.png)<br>