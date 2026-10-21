# Panduan Berkontribusi (Contributing Guide)

Terima kasih telah tertarik untuk berkontribusi pada **Perpustakaan Keamanan Siber**! Repositori ini dibangun dari, oleh, dan untuk komunitas siber Indonesia.

Semua bentuk kontribusi sangat disambut, baik itu menambahkan tautan buku gratis, merekomendasikan tools open-source baru, memperbaiki tautan yang rusak (*broken links*), maupun memperjelas penjelasan materi.

---

## 🌟 Cara Berkontribusi

### 1. Menambahkan Materi / Tools Baru via Pull Request (PR)
1. **Fork** repositori ini ke akun GitHub Anda.
2. Buat branch baru untuk fitur atau materi yang ingin Anda tambahkan:
   ```bash
   git checkout -b tambah-materi/nama-materi-atau-tool
   ```
3. Tambahkan materi pada file dan folder yang sesuai.
4. Pastikan mematuhi **Format Standar Penulisan** di bawah ini.
5. Commit perubahan Anda dengan pesan yang jelas:
   ```bash
   git commit -m "feat(tools): menambahkan tool Nuclei pada web-application-security"
   ```
6. Push branch Anda dan buat **Pull Request (PR)** ke branch `main`.

---

## 📝 Format Standar Entri

Untuk menjaga kerapian dan konsistensi, gunakan format berikut saat menambahkan referensi:

### Format Entri Tool Open Source
```markdown
### [Nama Tool](URL_KE_REPOSITORY_ATAU_WEBSITE)
- **Kategori**: (Contoh: Web Scanner / OSINT / Log Analyzer)
- **Lisensi**: (Contoh: Open Source - MIT / Apache 2.0 / GPLv3)
- **Tingkat Kesulitan**: Pemula / Menengah / Lanjut
- **Deskripsi**: Penjelasan ringkas dalam 1-2 kalimat tentang fungsi utama tool.
- **Tutorial / Panduan**: [Judul Panduan](URL_Panduan) (diutamakan referensi berbahasa Indonesia bila ada).
```

### Format Entri Buku / E-Book
```markdown
### [Judul Buku](URL_LEGAL_BUKU)
- **Penulis**: Nama Penulis
- **Bahasa**: Indonesia / Inggris
- **Akses**: Gratis / Open Access / Berbayar
- **Tingkat**: Pemula / Menengah / Lanjut
- **Ringkasan**: Deskripsi 1-2 kalimat mengenai topik yang dibahas dan alasan mengapa buku ini direkomendasikan.
```

---

## ⚠️ Aturan Kurasi (Quality Guidelines)

1. **Hanya Tautan Legal & Etis**:
   - Dilarang keras membagikan tautan unduhan bajakan (e-book bajakan, tool *cracked*, torrent ilegal, dsb.).
   - Dilarang membagikan malware aktif, materi pencurian data, akun curian, atau hal-hal yang melanggar hukum.
2. **Prioritaskan Bahasa Indonesia**:
   - Jika tersedia dokumentasi, tutorial, atau ringkasan berbahasa Indonesia yang berkualitas, utamakan tautan tersebut agar mudah dipahami masyarakat luas.
3. **Deskripsi Jelas & Objektif**:
   - Hindari klaim berlebihan ("Tool hacking terhebat di dunia"). Berikan penjelasan teknis yang akurat dan berbasis fakta.
4. **Periksa Tautan Rusak**:
   - Pastikan URL masih aktif dan dapat diakses publik tanpa *paywall* terselubung.

---

## 💬 Diskusi dan Usulan Ide
Jika Anda memiliki ide besar atau ingin berdiskusi sebelum membuat PR, silakan buka diskusi baru melalui menu [GitHub Issues](https://github.com/wahyusutejo1986/perpustakaan-keamanan-siber/issues) dengan template yang telah disediakan.
