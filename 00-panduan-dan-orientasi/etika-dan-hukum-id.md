# ⚖️ Etika, Hukum, dan Riset Bertanggung Jawab di Indonesia

Keamanan siber adalah pedang bermata dua. Keterampilan yang sama yang digunakan untuk mempertahankan sistem dapat disalahgunakan untuk merusak atau mencuri data. Oleh karena itu, pemahaman etika dan hukum adalah pilar nomor satu bagi siapa saja yang ingin terjun ke dunia siber.

---

## 🏛️ Landasan Hukum Keamanan Siber di Indonesia

### 1. Undang-Undang Pelindungan Data Pribadi (UU PDP No. 27 Tahun 2022)
- **Tujuan**: Menjamin privasi warga negara serta mengatur hak dan kewajiban Pengendali dan Prosesor Data Pribadi.
- **Poin Penting Bagi Praktisi Siber**:
  - Organisasi wajib menerapkan keamanan teknis dan enkripsi yang layak untuk melindungi data pribadi.
  - Kewajiban notifikasi kebocoran data (*data breach notification*) paling lambat 3 x 24 jam kepada subjek data dan lembaga berwenang.
  - Sanksi pidana dan denda administratif hingga miliaran rupiah bagi pihak yang memperjualbelikan atau mengakses data pribadi tanpa hak.

### 2. Undang-Undang Informasi dan Transaksi Elektronik (UU ITE)
*UU No. 11 Tahun 2008 juncto UU No. 19 Tahun 2016 juncto UU No. 1 Tahun 2024:*
- **Pasal 30 (Akses Ilegal / Illegal Access)**:
  Melarang setiap orang dengan sengaja dan tanpa hak atau melawan hukum mengakses komputer dan/atau sistem elektronik milik orang lain dengan cara apa pun.
- **Pasal 31 (Intersepsi / Penyadapan Data)**:
  Melarang penyadapan transmisi data elektronik secara tidak sah.
- **Pasal 32 (Perusakan Data / Data Tampering)**:
  Melarang mengubah, merusak, memindahkan, atau menyembunyikan data/dokumen elektronik orang lain.
- **Pasal 33 (Gangguan Sistem / DoS / DDoS)**:
  Melarang tindakan apa pun yang berakibat terganggunya sistem elektronik atau membuat sistem menjadi tidak bekerja sebagaimana mestinya.

---

## 🎯 Panduan Riset Etis & Pengungkapan Celah (Responsible Disclosure)

Jika Anda secara tidak sengaja menemukan kerentanan pada sistem milik instansi atau perusahaan:
1. **Jangan Mengeksploitasi Lebih Jauh**:
   Begitu Anda membuktikan adanya celah (misal: memunculkan `alert(1)` pada XSS atau `whoami` pada RCE), segera hentikan pengujian. Jangan melihat atau menyalin data sensitif pengguna.
2. **Kirim Laporan Melalui Jalur Resmi**:
   Hubungi kontak keamanan instansi terkait (contoh: `security@perusahaan.com` atau CSIRT BSSN jika instansi pemerintah).
3. **Format Laporan yang Baik**:
   - Judul & tingkat keparahan (*Severity*)
   - Langkah reproduksi yang jelas (*Step-by-step reproduction*)
   - Dampak risiko nyata bagi bisnis/pengguna
   - Rekomendasi perbaikan teknis (*Remediation*)
4. **Berikan Waktu Remediasi (Wajar 30–90 Hari)**:
   Jangan mempublikasikan celah (*full disclosure*) ke media sosial sebelum pihak pengelola memiliki kesempatan untuk menambalnya, demi melindungi keselamatan data masyarakat umum.
