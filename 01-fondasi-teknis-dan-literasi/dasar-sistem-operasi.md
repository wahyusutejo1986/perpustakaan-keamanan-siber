# 🖥️ Fondasi Teknis: Dasar Sistem Operasi untuk Siber

Sistem Operasi (OS) adalah tempat seluruh proses, file, hak akses, dan memori berjalan. Menguasai arsitektur Linux dan Windows adalah syarat mutlak bagi praktisi keamanan siber.

---

## 🐧 Linux Internals & Command Line
Mayoritas server di internet, perangkat cloud, dan distribusi keamanan (seperti Kali Linux & Parrot OS) berbasis Linux.

### 1. Struktur Hirarki Direktori Linux
- `/etc/`: Berisi file konfigurasi sistem (misal: `/etc/passwd`, `/etc/shadow`, `/etc/ssh/sshd_config`).
- `/var/log/`: Pusat log sistem dan aplikasi (misal: `auth.log`, `syslog`, `nginx/access.log`).
- `/proc/`: Sistem file virtual yang merepresentasikan proses yang sedang berjalan di memori (*RAM*).
- `/dev/`: File khusus yang merepresentasikan perangkat keras (*storage, tty*).

### 2. Izin Berkas (File Permissions)
- Format: `rwx` (Read = 4, Write = 2, Execute = 1).
- Hak khusus:
  - **SUID (Set User ID)**: Jika disematkan pada biner executable, biner akan berjalan dengan izin pemilik file (biasanya `root`). Kerentanan umum jika biner memiliki celah (*SUID Abuse / Privilege Escalation*).

---

## 🪟 Windows Internals & Active Directory (AD)
Mayoritas jaringan korporasi di Indonesia dan dunia menggunakan ekosistem Microsoft Windows.

### 1. Komponen Inti Windows
- **Windows Registry**: Basis data hierarkis terpusat untuk konfigurasi OS dan aplikasi (`HKLM`, `HKCU`).
- **Windows Event Logs**: Rekam jejak aktivitas sistem yang dipantau oleh SOC:
  - `Event ID 4624`: Login berhasil
  - `Event ID 4625`: Percobaan login gagal (indikasi *Brute Force*)
  - `Event ID 4688`: Proses baru dibuat (*Process Creation*)
  - `Event ID 7045`: Layanan (*service*) baru dipasang (indikasi *Persistence malware*)

### 2. Dasar Active Directory (AD)
- **Domain Controller (DC)**: Server terpusat penyedia autentikasi via Kerberos dan LDAP.
- **Kerberos**: Protokol tiket autentikasi (*Ticket Granting Ticket / TGT*). Kerentanan umum: *Kerberoasting, AS-REP Roasting*.
