# Task 1 – Eksplorasi Docker Basic (Nginx)

## 1. Pull Image Nginx
docker pull nginx:alpine
- Mengambil image Nginx versi Alpine dari Docker Hub.
- Alpine = versi ringan, cocok untuk praktikum.

## 2. Jalankan Container dengan Nama
docker run -d --name web-praktikum -p 8080:80 nginx:alpine
- `-d` → jalankan di background
- `--name web-praktikum` → beri nama container
- `-p 8080:80` → mapping port host 8080 ke port 80 container

## 3. Akses di Browser
http://localhost:8080
- Cek apakah halaman default Nginx muncul di browser.

## 4. Lihat Logs Container
docker logs web-praktikum
- Menampilkan log container, berguna untuk debugging.

## 5. Masuk ke Dalam Container
docker exec -it web-praktikum sh
- Masuk ke shell container.

### Cek isi folder default Nginx
ls -la /usr/share/nginx/html
cat /etc/nginx/nginx.conf
- `ls -la` → melihat isi folder HTML default
- `cat nginx.conf` → melihat konfigurasi Nginx

- Keluar dari container:
exit

## 6. Stop dan Hapus Container
docker stop web-praktikum
docker rm web-praktikum
- Stop container yang berjalan
- Hapus container untuk bersih-bersih