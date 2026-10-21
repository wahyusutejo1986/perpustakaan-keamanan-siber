# 🚨 Playbook Cepat: Tanggap Darurat Insiden Siber

Playbook ringkas yang dapat segera digunakan oleh staf IT atau tim tanggap darurat saat terjadi insiden keamanan siber kritis.

---

## ☣️ Skenario 1: Infeksi Ransomware

1. **ISOLASI JARINGAN SEGERA**:
   - Cabut kabel LAN fisik dari perangkat yang terindikasi terinfeksi.
   - Matikan koneksi Wi-Fi dan Bluetooth.
   - **JANGAN me-restart atau mematikan daya komputer (*Do not reboot*)** jika artefak RAM diperlukan untuk investigasi kunci enkripsi atau identifikasi proses ransomware.
2. **Identifikasi Cakupan (*Blast Radius*)**:
   - Apakah network share / NAS ikut terenkripsi? Segera putuskan akses tulis (*write permission*) ke seluruh shared storage.
   - Cek mesin lain yang berada dalam subnet yang sama.
3. **Identifikasi Varian Ransomware**:
   - Cari file catatan tebusan (*Ransom Note*, misal: `README_RECOVER.txt`).
   - Unggah sampel file terenkripsi dan ransom note ke [No More Ransom Project](https://www.nomoreransom.org/) atau [ID Ransomware](https://id-ransomware.malwarehunterteam.com/) untuk mengecek apakah kunci dekripsi publik sudah tersedia secara gratis.
4. **Pembersihan & Pemulihan**:
   - Format ulang mesin yang terinfeksi dan lakukan instalasi OS bersih.
   - Pulihkan data dari cadangan offline (*air-gapped backup*) yang diverifikasi bersih.

---

## 🕸️ Skenario 2: Peretasan Situs Web (Web Defacement / Webshell)

1. **Alihkan Situs ke Mode Pemeliharaan (*Maintenance Mode*)**:
   - Jangan biarkan halaman defacement tetap tayang karena dapat merusak reputasi instansi/perusahaan.
2. **Amankan Log Akses Web Server**:
   - Salin file log ke lokasi aman sebelum ditimpa (*rotated*):
     - Nginx: `/var/log/nginx/access.log` dan `error.log`
     - Apache: `/var/log/apache2/access.log` dan `error.log`
3. **Cari File Webshell & File Baru**:
   - Cari file PHP/ASPX yang baru dibuat atau diubah dalam 24 jam terakhir:
     ```bash
     find /var/www/html/ -type f -mtime -2 -ls
     ```
   - Cari pola berbahaya pada file source code:
     ```bash
     grep -rnw '/var/www/html/' -e 'eval(' -e 'base64_decode(' -e 'passthru(' -e 'shell_exec('
     ```
4. **Tutup Celah Masuk (*Root Cause*)**:
   - Periksa apakah celah masuk berasal dari plugin/CMS yang tidak diperbarui, celah upload file (*Unrestricted File Upload*), atau kredensial admin yang lemah.
   - Reset semua kata sandi database, user admin CMS, dan SSH key server.

---

## 📢 Kontak Insiden Siber Nasional
- **BSSN CSIRT (Gov-CSIRT / BSSN-CSIRT)**: Laporkan jika insiden melibatkan infrastruktur vital atau instansi pemerintah via situs resmi [csirt.bssn.go.id](https://csirt.bssn.go.id/).
