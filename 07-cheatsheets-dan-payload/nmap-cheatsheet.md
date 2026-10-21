# 📑 Cheatsheet Praktis: Nmap (Network Mapper)

Nmap adalah alat pemindaian jaringan (*network exploration*) dan audit keamanan sumber terbuka yang paling umum digunakan oleh praktisi siber.

---

## ⚡ Pemindaian Cepat (Quick Scans)

| Perintah | Deskripsi |
| :--- | :--- |
| `nmap <target>` | Memindai 1.000 port paling umum (*default*). |
| `nmap -F <target>` | Fast Scan: Hanya memindai 100 port paling umum. |
| `nmap -p- <target>` | Memindai seluruh 65.535 port TCP (butuh waktu lebih lama). |
| `nmap -p 80,443,8080 <target>` | Memindai port-port tertentu saja. |

---

## 🔍 Deteksi Versi & Sistem Operasi

| Perintah | Deskripsi |
| :--- | :--- |
| `nmap -sV <target>` | Mendeteksi versi layanan (*Service Version Detection*). |
| `nmap -O <target>` | Mendeteksi estimasi Sistem Operasi target (*OS Detection*). |
| `nmap -A <target>` | **Aggressive Mode**: Kombinasi `-sV`, `-O`, `-sC` (default scripts), dan traceroute. |

---

## 📜 Nmap Scripting Engine (NSE)

| Perintah | Deskripsi |
| :--- | :--- |
| `nmap -sC <target>` | Menjalankan kumpulan skrip standar (*default scripts*). |
| `nmap --script=vuln <target>` | Menjalankan skrip pemeriksaan kerentanan umum pada target. |
| `nmap --script=http-title <target>` | Mengambil judul halaman HTTP pada layanan web target. |

---

## 💾 Menyimpan Output Hasil Pemindaian

| Perintah | Deskripsi |
| :--- | :--- |
| `nmap -oN hasil.txt <target>` | Menyimpan output dalam format teks biasa (*Normal*). |
| `nmap -oX hasil.xml <target>` | Menyimpan output dalam format XML (untuk integrasi tool lain). |
| `nmap -oA scan_result <target>` | Menyimpan dalam semua format sekaligus (.nmap, .xml, .gnmap). |

---

> ⚠️ **Catatan Penting**: Lakukan pemindaian hanya pada jaringan atau server yang Anda miliki izin resmi pengujiannya.
