# 📑 Cheatsheet: Jaringan & Perintah Pemindaian Nmap

Panduan cepat sintaks Nmap untuk audit port, enumerasi banner layanan, dan skrip keamanan otomatis.

---

## ⚡ Pemindaian Cepat (Port Scanning)

| Perintah | Fungsi | Catatan |
| :--- | :--- | :--- |
| `nmap <IP>` | Memindai 1.000 port paling umum | Cepat, profil default |
| `nmap -F <IP>` | Fast Scan: 100 port paling umum | Sangat cepat untuk inspeksi awal |
| `nmap -p- <IP>` | Memindai seluruh 65.535 port TCP | Wajib sebelum menyimpulkan target aman |
| `nmap -p 22,80,443,3389 <IP>` | Memindai daftar port spesifik | Port kritis (SSH, HTTP, HTTPS, RDP) |
| `nmap -sU -top-ports 20 <IP>` | Memindai 20 port UDP paling populer | DNS, SNMP, NTP, DHCP |

---

## 🔍 Deteksi Versi & Operating System

| Perintah | Fungsi |
| :--- | :--- |
| `nmap -sV <IP>` | Menentukan versi perangkat lunak layanan (*Service Version Detection*). |
| `nmap -O <IP>` | Mengestimasi sistem operasi target (*OS Fingerprinting*). |
| `nmap -A <IP>` | **Aggressive Mode**: Mengaktifkan `-sV`, `-O`, `-sC` (default scripts), dan traceroute sekaligus. |

---

## 📜 Nmap Scripting Engine (NSE)

| Perintah | Fungsi |
| :--- | :--- |
| `nmap -sC <IP>` | Menjalankan kumpulan skrip standar aman (*default scripts*). |
| `nmap --script=vuln <IP>` | Memeriksa apakah layanan target memiliki kerentanan CVE yang diketahui. |
| `nmap --script=ssl-cert,ssl-enum-ciphers -p 443 <IP>` | Mengaudit sertifikat SSL/TLS dan mendeteksi cipher lawas yang lemah. |

---

## 💾 Menyimpan Hasil Scan

| Format | Perintah |
| :--- | :--- |
| **Normal Text** | `nmap -oN hasil_scan.txt <IP>` |
| **XML Output** | `nmap -oX hasil_scan.xml <IP>` (Sangat cocok untuk diimpor ke Metasploit/Burp/Faraday) |
| **All Formats** | `nmap -oA hasil_lengkap <IP>` (Menyimpan .nmap, .xml, dan .gnmap sekaligus) |

---

> ⚠️ *Pengingat Etika: Jangan pernah melakukan pemindaian jaringan di luar target lab atau sistem tanpa izin resmi bertanda tangan.*
