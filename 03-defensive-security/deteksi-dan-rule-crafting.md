# 🎯 Rekayasa Deteksi & Pembuatan Aturan (Detection Engineering)

Detection Engineer bertugas menulis aturan deteksi otomatis agar sistem pertahanan (SIEM, EDR, IDS) dapat mendeteksi perilaku musuh secara cepat dan minim alarm palsu (*low false positive*).

---

## 📝 1. Sigma Rules (Standar Format Deteksi Log Generik)

[Sigma](https://github.com/SigmaHQ/sigma) adalah format tanda tangan berbasis YAML yang dapat dikonversi ke berbagai bahasa query SIEM (seperti Splunk SPL, Elastic Lucene, Wazuh, QRadar).

### Contoh Aturan Sigma Sederhana: Deteksi Pembersihan Log Event Windows
```yaml
title: Windows Security Log Cleared
id: 12345678-1234-1234-1234-123456789abc
status: stable
description: Mendeteksi upaya pembersihan log keamanan Windows (Teknik Defense Evasion)
references:
    - https://attack.mitre.org/techniques/T1070/001/
logsource:
    product: windows
    service: security
detection:
    selection:
        EventID:
            - 1102 # The audit log was cleared
    condition: selection
falsepositives:
    - Aktivitas maintenance resmi dari administrator sistem
level: high
```

---

## 🔬 2. YARA Rules (Identifikasi Pola Malware)

[YARA](https://virustotal.github.io/yara/) digunakan untuk mengklasifikasikan dan mengidentifikasi sampel malware berdasarkan string biner, regex, atau pola byte tertentu.

### Contoh Aturan YARA Sederhana:
```c
rule Deteksi_Webshell_PHP_Sederhana {
    meta:
        description = "Mendeteksi fungsi eksekusi perintah berbahaya pada file PHP"
        author = "Perpustakaan Keamanan Siber Indonesia"
        date = "2026-10-21"
    strings:
        $p1 = "eval($_POST[" nocase
        $p2 = "system($_GET[" nocase
        $p3 = "shell_exec(" nocase
        $p4 = "passthru(" nocase
    condition:
        2 of ($p*)
}
```
