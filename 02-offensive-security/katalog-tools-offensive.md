# 🛠️ Katalog Tools Open Source: Offensive Security

Daftar perangkat lunak sumber terbuka (*open source*) yang digunakan untuk simulasi serangan etis, audit kerentanan, dan riset keamanan siber.

---

## 🔎 1. Reconnaissance & OSINT (Pengumpulan Informasi)

### [Subfinder](https://github.com/projectdiscovery/subfinder)
- **Kategori**: Subdomain Discovery
- **Lisensi**: MIT License
- **Fungsi**: Menemukan subdomain valid dari target dengan memanfaatkan puluhan sumber pasif tanpa menyentuh server target secara langsung.

### [Amass (OWASP)](https://github.com/owasp-amass/amass)
- **Kategori**: In-depth Attack Surface Mapping
- **Lisensi**: Apache 2.0
- **Fungsi**: Memetakan seluruh aset eksternal dan infrastruktur jaringan target menggunakan teknik scraping DNS dan analisis graf.

---

## 🌐 2. Web Application & API Security

### [OWASP ZAP (Zed Attack Proxy)](https://www.zaproxy.org/)
- **Kategori**: Web Interception Proxy & Scanner
- **Lisensi**: Apache 2.0
- **Fungsi**: Alternatif open-source terpopuler untuk Burp Suite. Digunakan untuk memanipulasi request HTTP/S dan melakukan pemindaian otomatis.

### [Nuclei](https://github.com/projectdiscovery/nuclei)
- **Kategori**: Vulnerability Scanner Berbasis Template
- **Lisensi**: MIT License
- **Fungsi**: Pemindai kerentanan berbasis template YAML yang diperbarui secara aktif oleh ribuan peneliti keamanan global untuk mendeteksi ribuan CVE.

### [Sqlmap](https://sqlmap.org/)
- **Kategori**: Database Takeover & SQL Injection
- **Lisensi**: GPLv2
- **Fungsi**: Otomasi deteksi dan eksploitasi kerentanan SQL Injection serta ekstraksi data.

### [ffuf (Fuzz Faster U Fool)](https://github.com/ffuf/ffuf)
- **Kategori**: High-Speed Web Fuzzer
- **Lisensi**: MIT License
- **Fungsi**: Fuzzing direktori, file tersembunyi, parameter URL, dan payload POST dengan performa tinggi berbasis Go.

---

## 🖥️ 3. Jaringan, Active Directory & Post-Exploitation

### [Nmap](https://nmap.org/)
- **Kategori**: Network Scanner & Port Mapper
- **Lisensi**: Nmap Public Source License
- **Fungsi**: Standar industri pemindaian jaringan, audit port terbuka, deteksi layanan (*service version*), dan skrip otomatis (NSE).

### [BloodHound (CE)](https://github.com/SpecterOps/BloodHound)
- **Kategori**: Active Directory Attack Path Analysis
- **Lisensi**: GPLv3
- **Fungsi**: Menggunakan teori graf untuk memetakan hubungan tersembunyi dalam domain Active Directory guna menemukan jalur eskalasi hak akses tercepat ke *Domain Admin*.

### [Sliver C2](https://github.com/BishopFox/sliver)
- **Kategori**: Command & Control (C2) Framework
- **Lisensi**: GPLv3
- **Fungsi**: Framework C2 lintas platform (Windows, Linux, macOS) buatan Bishop Fox yang digunakan oleh Red Team untuk emulasi penyerang secara terdistribusi.
