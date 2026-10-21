# 🛡️ Fondasi & Literasi: Cyber Hygiene dan Privasi

Materi ini ditujukan bagi siapa saja—termasuk masyarakat umum, pemula, dan staf non-teknis—untuk memahami cara menjaga keamanan diri dan data pribadi di ruang digital.

---

## 📌 Topik Utama

### 1. Manajemen Kata Sandi (Password Management)
- **Prinsip Utama**: Hindari penggunaan satu kata sandi untuk banyak akun (*password reuse*). Gunakan kombinasi kata acak panjang (passphrase minimal 14–16 karakter).
- **Password Manager Rekomendasi (Open Source / Gratis)**:
  - [Bitwarden](https://bitwarden.com/) - Solusi password manager open-source terpopuler, mendukung sync lintas perangkat.
  - [KeePassXC](https://keepassxc.org/) - Password manager offline dan open-source untuk kontrol penuh tanpa cloud.

### 2. Autentikasi Multifaktor (2FA / MFA)
- Selalu aktifkan 2FA di setiap layanan penting (email, perbankan, media sosial, akun cloud).
- Utamakan aplikasi autentikator atau kunci fisik (FIDO2/U2F) dibandingkan SMS OTP yang rentan terhadap *SIM Swap Attack*.
- **Aplikasi 2FA Rekomendasi (Open Source)**:
  - [Aegis Authenticator](https://getaegis.com/) (Android - Open Source & Terenkripsi).
  - [Ente Auth](https://ente.io/auth/) (Multiplatform & Open Source dengan backup cloud terenkripsi E2EE).

### 3. Perlindungan Terhadap Rekayasa Sosial (Social Engineering & Phishing)
- **Trik Populer**: Pesan WhatsApp mengatasnamakan kurir paket (file `.apk`), undangan pernikahan palsu, tagihan listrik/pajak mendadak.
- **Prinsip Verifikasi**: Jangan pernah membuka file berekstensi `.apk` dari pesan singkat. Periksa alamat email pengirim (*sender domain*) dan URL link secara teliti.
- **Alat Pemeriksa URL / File Cepat**:
  - [VirusTotal](https://www.virustotal.com/) - Memindai file atau URL mencurigakan dengan puluhan mesin antivirus.
  - [URLScan.io](https://urlscan.io/) - Menganalisis situs web tanpa harus mengunjunginya langsung dari browser Anda.

### 4. Privasi Berselancar (Web Browsing Privacy)
- Gunakan ekstensi pemblokir pelacak dan iklan berbahaya:
  - [uBlock Origin](https://github.com/gorhill/uBlock) - Pemblokir konten dan pelacak open-source terbaik.
  - [Privacy Badger](https://privacybadger.org/) - Alat pelindung privasi dari EFF.

---

> 💡 *Ingin menambahkan tips atau panduan baru? Silakan baca [CONTRIBUTING.md](../CONTRIBUTING.md) dan ajukan Pull Request!*
