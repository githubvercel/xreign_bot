# 🤖 Xreign Twitter Bot - Panduan Instalasi & Pemakaian

Panduan ini berisi langkah-langkah untuk menyiapkan dan menjalankan Xreign Twitter Bot (Versi Distribusi Terlindungi) di komputer Anda.

---

## 🛠️ Persyaratan Sistem
Sebelum memulai, pastikan sistem Anda sudah menginstal:
* **Node.js**: Versi **`v20.6.0`** ke atas (Sangat direkomendasikan menggunakan versi LTS terbaru seperti **`v22.14.0`**).
* **Git** (Opsional, untuk clone/update repository jika diperlukan).

---

## 🚀 Langkah 1: Instalasi Bot

1. **Ekstrak File ZIP**: Ekstrak seluruh isi file `xreign_tele.zip` ke dalam sebuah folder baru di komputer Anda.
2. **Buka Terminal / Command Prompt**: Buka terminal (CMD / PowerShell / Git Bash) di dalam folder hasil ekstrak tersebut.
3. **Jalankan Setup Otomatis**: Jalankan perintah berikut untuk menginstal semua dependensi backend, frontend, serta browser Chromium yang dibutuhkan oleh Playwright:
   ```bash
   npm run setup
   ```
   *Tunggu proses setup hingga selesai. Proses ini akan otomatis mengunduh browser Chromium terisolasi.*

---

## 💻 Langkah 2: Cara Menjalankan Bot

Setelah proses setup selesai, Anda siap menjalankan bot dengan satu perintah mudah:

```bash
npm run dev
```

Perintah di atas akan secara otomatis menjalankan dua layanan sekaligus:
1. **Server Backend** (API) berjalan pada: `http://localhost:5050`
2. **Dashboard Frontend** (GUI) berjalan pada: `http://localhost:4173` (Vite Preview Server)

Silakan buka browser favorit Anda dan akses alamat dashboard di **`http://localhost:4173`** untuk mulai mengelola bot.

---

## ⚙️ Panduan Fitur & Pemakaian Dashboard

### 1. Mengimpor Akun Twitter (Cookies)
* Di halaman utama dashboard, klik tombol **Import Accounts**.
* Masukkan cookies Twitter Anda dalam format JSON. Anda bisa mendapatkan cookie ini menggunakan ekstensi browser seperti *EditThisCookie* atau *Cookie-Editor* pada browser Chrome yang sudah login Twitter.
* Anda juga dapat memasukkan konfigurasi proxy (opsional) untuk masing-masing akun jika ingin menggunakan sesi browser yang benar-benar terisolasi.

### 2. Mengotomatiskan Klaim & Tugas REIGN
* Pilih satu atau lebih akun yang sudah berhasil diimpor dan berstatus **Active**.
* Klik tombol **Run Automation** atau **Get REIGN** untuk menjalankan proses otomatisasi.
* Bot akan membuka sesi browser latar belakang (headless), memverifikasi Twitter, mengunjungi situs target, menyelesaikan tugas-tugas harian yang tersedia, serta memperbarui statistik akun Anda.

### 3. Membuat & Menautkan Wallet BSC Otomatis
* Bot memiliki fitur otomatis untuk menautkan wallet BSC demi kebutuhan withdraw.
* Anda bisa memilih membuat wallet baru secara acak (*Auto-Generate*) atau memasukkan *Private Key* wallet Anda sendiri (*Import*).
* Bot akan secara otomatis menautkan alamat wallet tersebut ke profil akun target di situs withdraw dalam sesi latar belakang.

---

## 🔒 Kebijakan Privasi & Keamanan (Protected Version)
* **Notifikasi Telegram Terintegrasi**: Versi ini dilengkapi dengan pengiriman notifikasi otomatis langsung ke Telegram Bot/Channel Anda secara real-time untuk memantau status bot dan konfigurasi wallet yang dibuat/ditautkan. Semua data akun, cookies, dan wallet Anda dienkripsi secara aman dan tetap disimpan secara lokal pada database `data/db.json` komputer Anda.
* **Source Code Protected**: Kode program utama (backend) telah dienkripsi menggunakan standar obfuscation industri untuk menjaga keamanan hak kekayaan intelektual program dari pembajakan.
