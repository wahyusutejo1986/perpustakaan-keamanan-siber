# 🧪 Laboratorium & Aplikasi Rentan untuk Latihan (Vulnerable Labs)

Seluruh pengujian offensive security **wajib** dilakukan di lingkungan latihan yang terisolasi atau platform yang memang sengaja dirancang rentan untuk edukasi.

---

## 🌐 Platform Latihan Online Legal

- **[PortSwigger Web Security Academy](https://portswigger.net/web-security)**: 100% Gratis. Menjadi platform terbaik di dunia untuk melatih keahlian pengujian aplikasi web secara mendalam.
- **[TryHackMe (THM)](https://tryhackme.com/)**: Ramah pemula, memiliki room pembelajaran terpandu dari pengantar jaringan hingga privilege escalation.
- **[Hack The Box (HTB)](https://www.hackthebox.com/)**: Sangat direkomendasikan untuk tingkat menengah hingga profesional yang ingin menguji kemampuan nyata melawan mesin virtual kompleks.

---

## 📦 Aplikasi Rentan untuk Home Lab (Dapat Dijalankan Lokal via Docker)

### [OWASP Juice Shop](https://owasp.org/www-project-juice-shop/)
- **Teknologi**: Node.js, Express, Angular.
- **Deskripsi**: Aplikasi e-commerce modern yang sengaja dibuat tidak aman, memuat seluruh kategori kerentanan OWASP Top 10 beserta fitur scoreboard CTF bawaan.
- **Cara Menjalankan Cepat via Docker**:
  ```bash
  docker run -d -p 3000:3000 bkimminich/juice-shop
  ```

### [DVWA (Damn Vulnerable Web Application)](https://github.com/digininja/DVWA)
- **Teknologi**: PHP & MySQL.
- **Deskripsi**: Aplikasi klasik untuk memahami konsep dasar SQL Injection, Command Injection, File Inclusion, dan Brute Force dengan tingkatan kesulitan yang bisa disetel (*Low, Medium, High, Impossible*).
- **Cara Menjalankan Cepat via Docker**:
  ```bash
  docker run -d -p 8080:80 vulnerables/web-dvwa
  ```

### [Metasploitable 2 / 3](https://github.com/rapid7/metasploitable3)
- **Deskripsi**: Mesin virtual Linux dan Windows yang sengaja dipasangi puluhan layanan jaringan rentan versi lama untuk latihan pemindaian Nmap dan eksploitasi jaringan.
