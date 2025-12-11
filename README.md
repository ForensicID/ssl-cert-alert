# 🔒 SSL Domain Certified Alert

[![Shell Script](https://img.shields.io/badge/Language-Shell%20Script-brightgreen)](https://www.gnu.org/software/bash/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Skrip Bash ringan dan otomatis untuk memantau tanggal kedaluwarsa sertifikat SSL/TLS dari daftar domain. Skrip ini akan mengirimkan notifikasi kritis ke Telegram ketika sertifikat mendekati tanggal kedaluwarsa, membantu mencegah *downtime* atau peringatan keamanan browser. 

---

## ✨ Fitur Utama

* **Pengecekan SSL/TLS:** Menggunakan `curl` untuk mengambil tanggal kedaluwarsa sertifikat SSL dari *header* koneksi.
* **Notifikasi Telegram Kritis:** Mengirimkan notifikasi peringatan pada batas waktu:
    * **30 Hari** sebelum kedaluwarsa (Peringatan Awal).
    * **1 Hari** sebelum kedaluwarsa (Peringatan Darurat).
* **Input Daftar Domain:** Membaca domain dan subdomain dari file teks untuk pemantauan massal.
* **Penggunaan Ringan:** Skrip yang mudah di-*deploy* dan dijadwalkan menggunakan Cron Job.

---

## 🛠️ Prasyarat

Pastikan Anda memiliki utilitas berikut terinstal di sistem Anda:

* **`bash`**
* **`curl`** (Untuk mengecek SSL dan mengirim pesan ke Telegram API)
* **`date`** (Untuk perhitungan sisa hari)

### Instalasi Prasyarat

```bash
# Untuk Debian/Ubuntu
sudo apt update
sudo apt install curl

# Untuk sistem berbasis RHEL/Fedora
sudo dnf install curl
