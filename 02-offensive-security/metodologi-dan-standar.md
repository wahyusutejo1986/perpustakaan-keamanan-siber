# 📐 Metodologi & Standar Pengujian Penetrasi (Pentesting Standards)

Penetration testing profesional bukan sekadar "menjalankan tool dan melihat apa yang rusak". Pengujian profesional memerlukan metodologi terstandarisasi untuk menjamin cakupan audit yang menyeluruh, aman, dan dapat dipertanggungjawabkan kepada klien.

---

## 🏛️ Metodologi Standar Industri Global

### 1. [OWASP Web Security Testing Guide (WSTG)](https://owasp.org/www-project-web-security-testing-guide/)
- **Fokus**: Keamanan Aplikasi Web
- **Cakupan**: 12 kategori pengujian (Information Gathering, Configuration Management, Identity Management, Authentication, Authorization, Session Management, Input Validation, Error Handling, Cryptography, Business Logic, Client-side Testing).

### 2. [PTES (Penetration Testing Execution Standard)](http://www.pentest-standard.org/)
- **Fokus**: Standar Pelaksanaan Pentest End-to-End
- **Tahapan**:
  1. *Pre-engagement Interactions* (Penentuan lingkup/Scope of Work & Letter of Authorization).
  2. *Intelligence Gathering* (OSINT & Reconnaissance).
  3. *Threat Modeling* (Identifikasi aset dan vektor ancaman).
  4. *Vulnerability Analysis* (Penemuan celah).
  5. *Exploitation* (Validasi celah dengan PoC terkontrol).
  6. *Post Exploitation* (Menilai nilai aset yang dapat diakses & risiko bisnis).
  7. *Reporting* (Penyusunan laporan eksekutif dan teknis).

### 3. [OSSTMM (Open Source Security Testing Methodology Manual)](https://www.isecom.org/OSSTMM.3.pdf)
- **Fokus**: Metodologi pengujian keamanan operasional yang terukur secara ilmiah (Human, Physical, Wireless, Telecommunication, Data Networks).
