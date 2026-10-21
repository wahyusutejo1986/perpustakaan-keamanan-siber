# 🛠️ Katalog Tools Open Source: DevSecOps & Keamanan Cloud

Kumpulan perangkat lunak open source untuk mengotomasi pengujian keamanan kode, kontainer, IaC, dan postur keamanan cloud.

---

## 🔍 1. Analisis Kode (SAST, SCA & Secret Scanning)

### [Semgrep](https://semgrep.dev/)
- **Kategori**: Static Application Security Testing (SAST)
- **Lisensi**: LGPL-2.1
- **Fungsi**: Scanner kode statis yang sangat cepat berbasis pola sintaks. Mendukung puluhan bahasa pemrograman (Python, Go, JavaScript, Java, PHP, C#) dengan ribuan aturan deteksi open-source.

### [Trivy (Aqua Security)](https://trivy.dev/)
- **Kategori**: All-in-one Scanner (Container, IaC, SCA, Secrets)
- **Lisensi**: Apache 2.0
- **Fungsi**: Scanner terpopuler untuk mendeteksi CVE pada image Docker, dependensi aplikasi (Node, Python, Go, Java), file konfigurasi Terraform, dan Kubernetes.

### [Gitleaks](https://github.com/gitleaks/gitleaks)
- **Kategori**: Secret Scanner
- **Lisensi**: MIT License
- **Fungsi**: Mendeteksi dan mencegah tersimpannya kunci rahasia (API token, private key, AWS credentials, database password) di dalam riwayat commit Git.

---

## ☁️ 2. Cloud Security Posture Management (CSPM) & IaC

### [Prowler](https://github.com/prowler-cloud/prowler)
- **Kategori**: Multi-Cloud Security Assessment (AWS, Azure, GCP, Kubernetes)
- **Lisensi**: Apache 2.0
- **Fungsi**: Melakukan audit konfigurasi cloud otomatis terhadap standar kepatuhan (CIS Benchmarks, PCI-DSS, ISO 27001, GDPR) dan menghasilkan laporan visual.

### [Checkov (Bridgecrew)](https://www.checkov.io/)
- **Kategori**: Infrastructure as Code (IaC) Scanner
- **Lisensi**: Apache 2.0
- **Fungsi**: Memindai file Terraform, CloudFormation, Helm chart, dan Dockerfile sebelum dideploy untuk mencegah miskonfigurasi keamanan infrastruktur.

---

## 📊 3. Vulnerability Management

### [OWASP DefectDojo](https://www.defectdojo.org/)
- **Kategori**: DevSecOps Orchestration & Vulnerability Management
- **Lisensi**: BSD-3-Clause
- **Fungsi**: Dashboard terpusat untuk mengonsolidasi dan melakukan deduplikasi temuan celah keamanan dari berbagai scanner (Trivy, Semgrep, ZAP, SonarQube, Burp Suite).
