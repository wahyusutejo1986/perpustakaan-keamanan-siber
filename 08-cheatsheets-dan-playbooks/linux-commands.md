# 📑 Cheatsheet: Perintah Esensial Linux untuk Praktisi Siber

Kumpulan perintah Linux CLI yang paling sering digunakan untuk administrasi, inspeksi sistem, dan investigasi siber.

---

## 🔍 1. Investigasi Proses & Memori

| Perintah | Deskripsi |
| :--- | :--- |
| `ps aux` | Menampilkan seluruh proses yang sedang berjalan di sistem beserta user pemiliknya. |
| `top` / `htop` | Monitor proses dan utilisasi CPU/RAM secara interaktif real-time. |
| `lsof -p <PID>` | Menampilkan daftar file dan socket jaringan yang dibuka oleh suatu nomor PID proses. |
| `kill -9 <PID>` | Menghentikan paksa (*force kill*) suatu proses berbahaya. |

---

## 🌐 2. Pemeriksaan Koneksi Jaringan

| Perintah | Deskripsi |
| :--- | :--- |
| `ss -tulpn` | Menampilkan semua port TCP/UDP yang sedang mendengarkan (*Listening*) beserta PID aplikasinya. |
| `netstat -ano` | Menampilkan koneksi jaringan aktif (alternatif klasik `ss`). |
| `ip a` / `ifconfig` | Menampilkan alamat IP dan status antarmuka jaringan. |
| `tcpdump -i eth0 -nn -s0 -w capture.pcap` | Merekam paket data jaringan langsung dari CLI ke file pcap. |

---

## 🔐 3. Hak Akses & File Permissions

| Perintah | Deskripsi |
| :--- | :--- |
| `chmod 700 file.sh` | Hanya pemilik (*owner*) yang dapat membaca, menulis, dan mengeksekusi file. |
| `chmod +x script.sh` | Memberikan izin eksekusi pada file skrip. |
| `chown user:group file` | Mengubah kepemilikan user dan grup suatu file. |
| `find / -perm -u=s -type f 2>/dev/null` | **Mencari seluruh file biner dengan SUID bit aktif** (Penting untuk Privilege Escalation audit). |

---

## 📜 4. Analisis Log Cepat (CLI Piping)

| Perintah | Deskripsi |
| :--- | :--- |
| `tail -f /var/log/auth.log` | Memantau log autentikasi SSH secara real-time. |
| `grep "Failed password" /var/log/auth.log \| awk '{print $11}' \| sort \| uniq -c \| sort -nr` | Menghitung jumlah percobaan login gagal dan mengurutkan berdasarkan IP penyerang terbanyak. |
