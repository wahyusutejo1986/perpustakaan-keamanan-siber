# 🛡️ Panduan Cyber Hygiene & Keamanan Digital Masyarakat

Modul ini disusun dengan bahasa yang mudah dipahami oleh siapa saja (termasuk masyarakat umum, keluarga, dan pekerja non-teknis) untuk melindungi aset digital sehari-hari dari kejahatan siber yang marak di Indonesia.

---

## 🛑 Waspada Modus Penipuan Siber Terpopuler di Indonesia

### 1. Phishing & Sniffing via File APK Palsu
- **Modus**: Pelaku mengirimkan pesan via WhatsApp atau Telegram mengatasnamakan:
  - Kurir paket pengiriman ("Cek Resi Paket.apk")
  - Undangan pernikahan digital ("Surat Undangan.apk")
  - Surat tilang kepolisian atau tagihan pajak/BPJS
- **Bahaya**: Begitu aplikasi diinstal dan diberi izin SMS, malware akan menyadap SMS OTP perbankan dan menguras rekening korban.
- **Pencegahan**:
  - **Haram hukumnya** menginstal file berakhiran `.apk` yang dikirim lewat pesan chat.
  - Aktifkan fitur *Google Play Protect* di Android dan jangan izinkan *Install from unknown sources*.

### 2. Social Engineering & SIM Swap
- **Modus**: Penipu menelepon mengaku sebagai pihak bank atau operator seluler, meminta kode OTP atau kode verifikasi dengan alasan pembaruan kartu atau undian berhadiah.
- **Aturan Emas**: Pihak bank/layanan resmi **tidak pernah** meminta kode OTP, PIN, atau password Anda.

---

## 🔑 Kebiasaan Keamanan Wajib (Cyber Hygiene Essentials)

### 1. Gunakan Pengelola Kata Sandi (Password Manager)
- Jangan gunakan kombinasi seperti `tanggal lahir`, `nama anak`, atau kata sandi yang sama di semua akun.
- Gunakan Password Manager tepercaya:
  - **[Bitwarden](https://bitwarden.com/)** (Open source, sinkronisasi gratis lintas HP & Laptop).
  - **[KeePassXC](https://keepassxc.org/)** (Open source, penyimpanan lokal tanpa internet).

### 2. Selalu Aktifkan 2FA (Two-Factor Authentication)
- Gunakan aplikasi autentikator di ponsel, bukan SMS (karena SMS rentan disadap atau terkena pembajakan kartu SIM).
- Aplikasi autentikator open-source yang aman:
  - **[Aegis Authenticator](https://getaegis.com/)** (Android).
  - **[Ente Auth](https://ente.io/auth/)** (iOS, Android, Desktop dengan enkripsi end-to-end).

### 3. Berselancar Aman di Internet Publik (Wi-Fi Publik)
- Hindari bertransaksi perbankan di Wi-Fi gratisan yang tidak memiliki sandi atau tidak jelas pengelolanya.
- Gunakan VPN terpercaya yang memiliki reputasi audit keamanan jelas (seperti Mullvad atau ProtonVPN).
