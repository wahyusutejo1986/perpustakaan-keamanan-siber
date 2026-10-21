# 🌐 Fondasi Teknis: Dasar Jaringan Komputer untuk Siber

Tanpa pemahaman yang kuat tentang jaringan komputer, Anda tidak akan bisa memahami bagaimana serangan siber bergerak, bagaimana paket disadap, atau bagaimana firewall bekerja.

---

## 📚 Konsep Wajib yang Harus Dikuasai

### 1. Model Referensi: OSI Layer vs TCP/IP Model

| Layer OSI | Nama Layer | Protokol Umum | Relevansi Keamanan |
| :---: | :--- | :--- | :--- |
| **7** | **Application** | HTTP, HTTPS, DNS, SSH, FTP, SMTP | Target serangan web (XSS, SQLi), phishing email. |
| **6** | **Presentation** | SSL/TLS, JPEG, ASCII | Enkripsi data transit, mitigasi Man-in-the-Middle (MitM). |
| **5** | **Session** | RPC, NetBIOS | Pengelolaan sesi koneksi, session hijacking. |
| **4** | **Transport** | TCP (Three-Way Handshake), UDP | SYN Flood DDoS, port scanning, port filtering. |
| **3** | **Network** | IP, ICMP, IPsec, ARP | IP Spoofing, routing poisoning, ICMP tunneling. |
| **2** | **Data Link** | Ethernet, Wi-Fi (802.11), MAC | MAC flooding, ARP spoofing, Evil Twin AP. |
| **1** | **Physical** | Kabel UTP, Serat Optik, Sinyal Radio | Akses fisik langsung, penyadapan kabel optik/LAN. |

### 2. Cara Kerja TCP Three-Way Handshake
```
Klien                               Server
  | ----- [SYN] (Permintaan) ------> |
  | <---- [SYN-ACK] (Konfirmasi) --- |
  | ----- [ACK] (Siap Mengirim) ---> |
```
- **Konteks Serangan**: Jika penyerang mengirim ribuan paket `SYN` tanpa membalas `ACK`, server akan kehabisan sumber daya (*SYN Flood attack*).

### 3. Protokol Inti Internet
- **DNS (Domain Name System - Port 53)**: Menerjemahkan domain ke IP. Kerentanan: *DNS Spoofing, DNS Tunneling*.
- **HTTP (Port 80) vs HTTPS (Port 443)**: HTTPS mengenkripsi payload dengan TLS sehingga data tidak dapat dibaca di jaringan publik (anti-sniffing).
- **DHCP (Port 67/68)**: Pemberian IP otomatis. Kerentanan: *Rogue DHCP Server*.

---

## 🛠️ Praktik Analisis Jaringan dengan Wireshark
1. Unduh dan instal **[Wireshark](https://www.wireshark.org/)** (Open Source Packet Analyzer).
2. Lakukan *capture* pada interface jaringan aktif saat membuka situs web HTTP tanpa enkripsi vs HTTPS.
3. Amati perbedaan keterbacaan data kredensial (username/password) di panel paket data.
