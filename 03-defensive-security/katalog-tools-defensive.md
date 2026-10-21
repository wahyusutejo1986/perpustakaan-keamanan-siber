# 🛠️ Katalog Tools Open Source: Defensive Security

Kumpulan perangkat lunak sumber terbuka terbaik untuk pertahanan jaringan, pemantauan SOC, deteksi intrusi, dan visibilitas endpoint.

---

## 📊 1. SIEM & XDR (Security Information and Event Management)

### [Wazuh](https://wazuh.com/)
- **Kategori**: Open Source SIEM & XDR Platform
- **Lisensi**: GPLv2 / Apache 2.0
- **Fungsi**: Platform deteksi ancaman, pemantauan integritas berkas (FIM), respons insiden, dan audit kepatuhan terpadu. Sangat populer untuk implementasi SOC open source.

### [Elastic Security (ELK Stack)](https://www.elastic.co/security)
- **Kategori**: Log Management, SIEM, & Endpoint Security
- **Fungsi**: Mengumpulkan, mengindeks, dan menganalisis log berskala besar dengan visualisasi dashboard Kibana yang sangat fleksibel.

---

## 📡 2. Network Security Monitoring (NSM) & IDS/IPS

### [Suricata](https://suricata.io/)
- **Kategori**: Network Threat Detection Engine (IDS/IPS/NSM)
- **Lisensi**: GPLv2
- **Fungsi**: Mesin deteksi intrusi jaringan berkecepatan tinggi yang mampu memproses paket multi-gigabit dan mencatat log transaksi HTTP, TLS, DNS dalam format JSON.

### [Zeek (dahulu Bro)](https://zeek.org/)
- **Kategori**: Network Security Monitoring & Behavioral Analysis
- **Lisensi**: BSD
- **Fungsi**: Bukan sekadar IDS berbasis tanda tangan, Zeek mengubah paket lalu lintas mentah menjadi log terstruktur yang kaya konteks semantik untuk analisis forensik jaringan.

---

## 🔍 3. Visibilitas Endpoint & Threat Intelligence

### [Sysmon (System Monitor - Sysinternals)](https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon)
- **Kategori**: Windows Endpoint Monitoring
- **Fungsi**: Layanan sistem Windows yang mencatat aktivitas proses mendalam, koneksi jaringan, dan perubahan pembuatan file ke dalam Windows Event Log.

### [MISP (Malware Information Sharing Platform)](https://www.misp-project.org/)
- **Kategori**: Threat Intelligence Platform (TIP)
- **Lisensi**: AGPL-3.0
- **Fungsi**: Platform berbagi indikator kompromi (*Indicator of Compromise / IoC*) dan informasi ancaman siber antarorganisasi dan komunitas CSIRT.
