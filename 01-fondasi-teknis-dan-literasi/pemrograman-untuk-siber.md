# 💻 Fondasi Teknis: Pemrograman & Otomasi untuk Siber

Praktisi keamanan siber tidak harus menjadi software engineer murni, namun kemampuan membaca kode dan membuat skrip otomatisasi sangat membedakan praktisi pemula dengan profesional.

---

## 🐍 Bahasa Pemrograman Utama dalam Siber

### 1. Python (Bahasa Wajib untuk Pemula & Analis)
- **Fungsi Utama**: Otomasi pengujian, scraping data ancaman (threat intelligence), pembuatan PoC (Proof of Concept) exploit, dan integrasi API.
- **Pustaka (Libraries) Populer**:
  - `requests`: Mengirim dan memanipulasi request HTTP untuk pengujian web.
  - `scapy`: Membuat, membedah, dan memodifikasi paket jaringan level rendah.
  - `paramiko`: Otomasi koneksi dan eksekusi perintah via SSH.
  - `socket`: Pembuatan port scanner atau reverse shell sederhana.

### 2. Bash / Shell Scripting (Linux Administrator & Pentester)
- **Fungsi Utama**: Otomasi alur kerja command line di Linux, merangkai output antar-tool (*piping*), dan manajemen file log massal.
- **Perintah Penting**: `grep`, `awk`, `sed`, `curl`, `xargs`, `cut`, `sort`, `uniq`.

### 3. Go (Golang) (Modern Cyber Tools)
- **Fungsi Utama**: Bahasa favorit para pengembang tool siber modern (misal: tools dari ProjectDiscovery seperti Nuclei, Subfinder, Katana, serta C2 framework seperti Sliver).
- **Keunggulan**: Sangat cepat, efisien dalam konkurensi (*goroutines*), dan menghasilkan biner tunggal (*single standalone binary*) tanpa ketergantungan runtime.

### 4. PowerShell (Windows & Active Directory Pentesting / Hardening)
- **Fungsi Utama**: Otomasi administrasi Windows, ekstraksi data Active Directory, audit sistem pertahanan (*AppLocker, AMSI*), dan pembuatan playbook deteksi.
