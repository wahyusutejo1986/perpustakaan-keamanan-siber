# 🛡️ Praktik Terbaik Hardening: Kontainer, Kubernetes & Cloud

Pengerasan sistem (*hardening*) bertujuan untuk memperkecil permukaan serangan (*attack surface*) dengan menonaktifkan fitur yang tidak perlu dan menerapkan konfigurasi keamanan yang ketat.

---

## 🐳 1. Praktik Terbaik Dockerfile Hardening

1. **Jangan Jalankan Sebagai Root**:
   Secara default, kontainer berjalan sebagai user `root`. Selalu tentukan user non-root:
   ```dockerfile
   RUN groupadd -r appuser && useradd -r -g appuser appuser
   USER appuser
   ```
2. **Gunakan Minimal Image (Distroless / Alpine)**:
   Hindari image `ubuntu:latest` penuh yang memuat paket yang tidak dibutuhkan. Gunakan `cgr.dev/chainguard/static` atau `gcr.io/distroless/static`.
3. **Set File System Read-Only**:
   Jalankan kontainer dengan flag `--read-only` untuk mencegah penyerang mengunduh file atau biner berbahaya ke disk.
4. **Hapus Shell pada Lingkungan Produksi**:
   Jika kontainer aplikasi tidak memiliki `/bin/sh` atau `/bin/bash`, penyerang tidak dapat dengan mudah melakukan *spawn interactive reverse shell*.

---

## ☸️ 2. Praktik Terbaik Kubernetes (K8s) Hardening

- **Nonaktifkan Akses Automount Service Account Token**: Jika sebuah pod tidak memerlukan interaksi dengan Kubernetes API, set `automountServiceAccountToken: false`.
- **Gunakan Pod Security Standards (PSS)**: Terapkan profile `Restricted` pada namespace produksi untuk memblokir kontainer privileged.
- **Terapkan Network Policy**: Default Kubernetes mengizinkan semua pod saling berbicara. Terapkan *Default Deny All Ingress/Egress* dan izinkan hanya port yang diperlukan.

---

## ☁️ 3. Praktik Terbaik Cloud Identity (IAM)

- **Blokir Akses S3 Bucket / Cloud Storage ke Publik Secara Global**.
- **Wajibkan MFA (Multi-Factor Authentication)** untuk semua user di konsol cloud (AWS Management Console, GCP Console).
- **Gunakan IAM Roles / Service Accounts Sementara**: Jangan pernah menaruh kunci akses permanen (*Hardcoded Access Keys*) di dalam kode aplikasi.
